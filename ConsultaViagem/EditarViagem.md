
# Introdução
A API para atualizar cadastro de viagens


### Solicitação Put
> 201.39.92.60/api_hmg/v3/api/trip/updateTrip



## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|----------------|
|idSetor|Chave identificadora do setor|Numeric|
|dtViagem|Data que ocorrera a viagem|Date|required
|idMotorista|Chave identificadora do motorista|Numeric|required
|idViagem|Chave identificadora do Motorista|Numeric|required


### Códigos de erro 

Campos inválidos (erro 422)
```JS
{
    "message": "The given data was invalid.",
    "errors": {
	    "idViagem": [
            "O campo idViagem é requerido!",
            "O campo idViagem tem que ser numerico"
        ],
        "dtViagem": [
            "O campo dtViagem tem que ser do tipo Data DD/MM/YYYY",
            "O campo dtViagem é requerido!"
        ],
        "idMotorista": [
            "O campo idMotorista é requerido!",
            "O campo idMotorista  tem que ser numerico"
        ],
        "idSetor": [
            "O campo idSetor tem que ser numerico!"
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

```JS
{
    "status": "ok",
    "sucesso": {
        "sucesso": [
            "Viagem Editada"
        ]
    }
}
```
