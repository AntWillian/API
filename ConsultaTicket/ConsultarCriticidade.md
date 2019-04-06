
# Introdução
A API para criticidades de ticket


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/ticket/criticality



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


## Resposta

```JS
[
    {
        "idCriticidade": 1,
        "Nome_Criticidade": "Mídias Sociais"
    },
    {
        "idCriticidade": 2,
        "Nome_Criticidade": "Procon"
    },
    {
        "idCriticidade": 3,
        "Nome_Criticidade": "Reclame Aqui"
    },
    {
        "idCriticidade": 4,
        "Nome_Criticidade": "Audiência"
    },
    {
        "idCriticidade": 5,
        "Nome_Criticidade": "Outras Midias"
    },
    ...
]
```
