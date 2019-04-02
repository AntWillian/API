
# Introdução
A API para da baixa de volumes manual das viagem


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/trip/manualEntry



## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|--------------|
|idOcorrencia|Chave identificadora da Ocorrencia|Numeric|required
|idVolume|Chave identificadora do Volume|Numeric|required
|idViagem|Chave identificadora do Viagem|Numeric|required


### Códigos de erro 

Campos inválidos (erro 422)
```JS
{
    "message": "The given data was invalid.",
    "errors": {
	    "idOcorrencia": [
            "O campo idOcorrencia é requerido!",
            "O campo idOcorrencia tem que ser numerico"
        ],
        "idVolume": [
            "O campo idVolume tem que ser do tipo Data DD/MM/YYYY",
            "O campo idVolume é requerido!"
        ],
        "idViagem": [
            "O campo idViagem é requerido!",
            "O campo idViagem tem que ser numerico"
        ]
    }
}
```


Erros de sintaxe ou inesperados (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Erro ao tentar dar baixa no volume"
        ]
    }
}
```

## Resposta

```JS
{
    "status": "ok",
    "sucesso": {
        "Volume": [
            "Status do Volume atualizado"
        ]
    }
}
```
