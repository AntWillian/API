
# Introdução
A API para selecionar todos os ticket


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/ticket/selectAll



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

Nenhum Ticket  encontrado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "Ticket ": [
            "Nenhum Ticket encontrado"
        ]
    }
}
```


## Resposta

```JS
[
    {
        "Id Ticket": 3,
        "Id Pedido": 348,
        "Pedido Cliente": "16299021101",
        "Solicitante": "Carriers",
        "Situacao": "Não atendido",
        "Categoria": "Acareação",
        "Criticidade": "Audiência",
        "Data Solicitacao": "2019-04-02 17:47:51",
        "Ultima Interacao": null,
        "Embarcador": "VIA VAREJO",
        "Destinatario": "KARINA PAULA DE SOUSA"
    },
    ...
]
```
