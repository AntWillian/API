
# Introdução
A API remover volume da viagem


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/trip/removeVolume

## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|----------------|
|codigoBarras|código da etiqueta carriers|Numeric|required
|idViagem|Chave identificadora da viagem|Numeric|required


### Códigos de erro 

Campos inválidos (erro 422)
```JS
{
    "status": "erro",
    "errors": {
        "CodigoBarras": [
            "O campo Codigo de Barras é requerido!",
            "O Codigo de Barras deve ter formato EAN13!",
            "O Codigo de Barras deve ser numerico!"
        ],
         "idViagem": [
            "O campo idViagem  tem que ser numerico",
            "O campo idViagem é requerido!"
        ]
    }
}
```
código de barras invalido (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "CodigoBarras": [
            "Codigo de barras invalido"
        ]
    }
}
```


Viagens que estejam em status inválidos (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Esta viagem não pode ser roteirizada! Verifique o Status da viagem!"
        ]
    }
}
```
  

Erros de sintaxe na alteração do status da viagem (erro 500)

```JS
{
	"status": "erro",
	"errors": {
		"viagem": [
			"Ocorreu erro um erro durante alteração de status da viagem! Tente novamente"
		]
	}
}

```

Volume não cadastrado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Volume não encontrado"
        ]
    }
}
```

Volume  não pertence a viagem (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Este volume não pertence a esta viagem"
        ]
    }
}
```

Erro ao Pesquisar dados do volume (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Erro ao pesquisar dados do volume"
        ]
    }
}
```

Erro ao pesquisar dados da viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "Viagem": [
            "Erro ao pesquisar dados da Viagem"
        ]
    }
}
```

Erro ao pesquisar dados da viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "servidor": [
            "Erro ao remover volume"
        ]
    }
}
```

## Resposta
```JS
{
    "status": "ok",
    "sucesso": {
        "volume": [
            "Volume removido com sucesso!"
        ]
    }
}
```