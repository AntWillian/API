
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

caso o parâmetro `ignorarViagens` não seja informado a Api retorna as viagem que o motorista tem para a data informada
```JS
[
    {
        "idViagem": 33,
        "NomeViagem": "VGN_SAO PAULO_001",
        "idPlan": 0,
        "dtViagem": "2019-03-30",
        "idTipoOperacao": 1,
        "TipoViagem": "A",
        "OrdemViagem": 1,
        "idBase": 2,
        "idSetor": 0,
        "idMotorista": 2531,
        "QtdeMinima": 1,
        "QtdeMaxima": 50,
        "ValorMaximo": 10000,
        "QtdePrev": 0,
        "QtdeViagem": 0,
        "MotConfPres": "S",
        "hrPrevInicio": "2019-03-30 08:00:00",
        "hrPrevFim": "2019-03-30 18:00:00",
        "dtIniRoteirizacao": null,
        "dtFimRoteirizacao": null,
        "psRoteirizacao": null,
        "dtIniConfDespacho": "2019-03-26 15:49:12",
        "dtFimConfDespacho": null,
        "psConfDespacho": 2520,
        "hrIniViagem": "2019-03-27 11:02:11",
        "hrFimViagem": "2019-03-27 11:02:11",
        "psIniViagem": null,
        "Obs": "",
        "ConfSep_Obrigatoria": "N",
        "ConfSep_Realizada": "N",
        "BolaPreta": "N",
        "Filtrada": "N",
        "idStatusProcesso": 670,
        "Situacao": "VIAGEM INICIADA",
        "idPessoa": 2520,
        "dtEmissao": "2019-03-26 11:17:10",
        "dtImpRomaneio": null,
        "dtFimConfViagem": null,
        "psConfViagem": null,
        "psALT": null,
        "dtALT": null
    },
    ...
]
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

