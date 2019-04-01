
# Introdução
A API para criar novas viagens


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/trip/new

## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|----------------|
|idSetor|Chave identificadora do setor|Numeric|
|dtViagem|Data que ocorrera a viagem|Date|required
|idMotorista|Chave identificadora do motorista|required
|ignorarViagens|ignorar = 1|Numeric|


### Códigos de erro 

Campos invalidos (erro 422)
```JS
{
    "message": "The given data was invalid.",
    "errors": {
        "dtViagem": [
            "O campo dtViagem tem que ser do tipo Data DD/MM/YYYY",
            "O campo dtViagem é requerido!"
        ],
        "idMotorista": [
            "O campo idMotorista é requerido!",
            "O campo idMotorista  tem que ser numerico"
        ],
         "ignorarViagens": [
            "O campo ignorarViagens tem que ser numerico!"
        ],
        "idSetor": [
            "O campo idSetor tem que ser numerico!"
        ]
    }
}
```
Erros ao pesquisar dados da base (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "erro": [
            "Erro ao pesquisar dados da base"
        ]
    }
}
```
Erros ao pesquisar dados do setor (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "erro": [
            "Erro ao pesquisar dados do setor"
        ]
    }
}
```
Erros de sintaxe (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "erro": [
            "Erro no servidor"
        ]
    }
}
```

## Resposta

caso o parâmetro `ignorarViagens` não seja informado a Api retorna as viagem que o motorista tem para a data informada, caso nao possua nenhuma viagem ele cadastra a viagem.
```JS
{
    "status": "warning",
    "viagens": [
        {
            "idViagem": 38,
            "NomeViagem": "VGN_VL_AZEVEDO_002",
            "dtViagem": "2019-04-01",
            "idBase": 2,
            "Base": "SAO PAULO",
            "idSetor": 30,
            "Setor": "VL AZEVEDO",
            "Motorista": "ALEXSANDER MONTEIRO DA SILVA",
            "Situacao": "INICIADA"
        }
    ]
}
```

caso o parâmetro `ignorarViagens` seja informado a Api cadastra uma nova viagem para o motorista

```JS
{
    "status": "ok",
    "sucesso": {
        "sucesso": [
            "Viagem criada"
        ]
    }
}
```

