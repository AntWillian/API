
# Introdução
A API para abrir Ticket


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/ticket/new



## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|--------------|
|idPedido|Chave identificadora do pedido|Numeric|required
|idCategoria|Chave identificadora da categoria|Numeric|required
|idCriticidade|Chave identificadora da criticidade|Numeric|required
|Interacao|mensagem referente ao ticket|String|required





### Códigos de erro 

Campos inválidos (erro 422)
```JS
{
    "message": "The given data was invalid.",
    "errors": {
	    "idPedido": [
            "O campo idPedido é requerido!",
            "O campo idPedido tem que ser numerico"
        ],
        "idPedido": [
            "O campo idCategoria é requerido!",
            "O campo idCategoria tem que ser numerico"
        ],
        "idCriticidade": [
            "O campo idCriticidade é requerido!",
            "O campo idCriticidade tem que ser numerico"
        ],
        "Interacao": [
            "O campo Interacao é requerido!"
        ]
        
    }
}
```


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

já existe ticket (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "pedido": [
            "Já possui um ticket para esse pedido!"
        ]
    }
}
```

## Resposta

```JS
{
    "status": "ok",
    "sucesso": {
        "pedido": [
            "Foi aberto um ticket para este pedido!"
        ]
    }
}
```
