
# Introdução
A API para cancelamento de viagem


### Solicitação POST
> 201.39.92.60/api_hmg/v3/trip/cancelTrip



## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|--------------|
|idViagem|Chave identificadora da Viagem|Numeric|required




### Códigos de erro 

Erros de sintaxe ou inesperados (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "servidor": [
            "Erro no servidor"
        ]
    }
}
```

Viagem não pode ser cancelada (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "Viagem": [
            "Viagem não pode ser cancelada"
        ]
    }
}
```
idViagem invalido ou  não encontrado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "idViagem": [
            "Erro ao pesquisar Viagem"
        ]
    }
}
```


## Resposta

```JS
{
    "status": "ok",
    "sucesso": {
        "Viagem": [
            "Viagem cancelada"
        ]
    }
}
```
