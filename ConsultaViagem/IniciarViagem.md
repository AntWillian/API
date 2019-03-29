
# Introdução
A API para iniciar viagens


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/trip/startTrip

## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|----------------|
|idViagem|Chave identificadora da viagem|Numeric|required


### Códigos de erro 

Campos inválidos (erro 422)
```JS

{
	"status": "erro",
	"errors": {
		"idViagem": [
			"O campo idViagem tem que ser numerico",
			"O campo idViagem é requerido!"
		]
	}
}
```
Viagem sem nenhum volume adicionado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Não pode iniciar a viagem porque não tem volumes a entregar!"
        ]
    }
}
```

Erro ao iniciar viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Não pode iniciar a viagem"
        ]
    }
}
```

## Resposta
sucesso (200)
```JS
{
    "status": "ok",
    "sucesso": {
        "viagem": [
            "Viagem iniciada"
        ]
    }
}
```