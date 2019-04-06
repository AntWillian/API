
# Introdução
A API para finalizar Ticket


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/ticket/finishTicket



## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|--------------|
|idTicket|Chave identificadora do Ticket|Numeric|required




### Códigos de erro 
Campos inválidos (erro 422)

```JS

{
	"message": "The given data was invalid.",
	"errors": {
		"idTicket": [
			"O campo idTicket é requerido!",
			"O campo idTicket tem que ser numerico"
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

Ticket  não criado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "Ticket ": [
            "Ticket não encontrado"
        ]
    }
}
```


## Resposta

```JS
{
    "status": "ok",
    "sucesso": {
        "Ticket": [
            "Ticket finalizado!"
        ]
    }
}
```
