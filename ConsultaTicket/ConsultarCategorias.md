
# Introdução
A API para categorias de ticket


### Solicitação GET
> 201.39.92.60/api_hmg/v3/api/ticket/category



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
        "idCategoria": 1,
        "Nome_Categoria": "Dados de Recebedor"
    },
    {
        "idCategoria": 2,
        "Nome_Categoria": "Interação no Pedido"
    },
    {
        "idCategoria": 3,
        "Nome_Categoria": "Informações de Entrega"
    },
	 ...
]
```
