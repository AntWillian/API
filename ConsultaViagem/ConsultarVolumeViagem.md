
# Introdução
A API para pesquisar volumes da viagem


### Solicitação GET
> 201.39.92.60/api_hmg/v3/api/trip/getVolumeTrip/{idViagem}



## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|--------------|
|idViagem|Chave identificadora da Viagem|Numeric|required




### Códigos de erro 
Campos inválidos (erro 422)

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

Viagem não encontrada (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "Viagem": [
            "'Nenhuma Viagem encontrada"
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
            "idViagem invalido"
        ]
    }
}
```


## Resposta

```JS
[
    {
        "Ordem": 10,
        "NomeCliente": "VIA VAREJO",
        "idPedido": 407,
        "idVolume": 465,
        "Destinatario": "ELIDA MIRANDA",
        "Endereco": "RUA XV DE NOVEMBRO 113",
        "Cidade": "CRAVINHOS",
        "CEP": "14140000"
    },
    {
        "Ordem": 9,
        "NomeCliente": "VIA VAREJO",
        "idPedido": 406,
        "idVolume": 464,
        "Destinatario": "CAMILA BELEM TONIATTI",
        "Endereco": "AVENIDA JOSE PAULINO 1741",
        "Cidade": "PAULINIA",
        "CEP": "13140256"
    },
    ...
]

```
