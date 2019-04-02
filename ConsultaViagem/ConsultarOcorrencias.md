
# Introdução
A API para listar ocorrências


### Solicitação GET
> 201.39.92.60/api_hmg/v3/api/trip/getOccurrences


### Códigos de erro 

Erros de sintaxe (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "ocorrências": [
            "Erro ao pesquisar ocorrências"
        ]
    }
}
```

## Resposta

```JS
[
    {
        "idOcorrencia": 0,
        "Ocorrencia": "ENTREGAR"
    },
    {
        "idOcorrencia": 101,
        "Ocorrencia": "REALIZADA"
    },
    ...
]
```
