# Introdução
A API de consulta de viagem


### Solicitação Get 
> 201.39.92.60/api_hmg/v3/api/trip/search?dtViagem=&idViagem=&nomeViagem=&nomeMotorista=

# Parâmetros
|Campo                  |Descricao  |Tipo           
|----------------|-------------------------------|-------------------------------|
|dtViagem|`Data que a viagem entrara em rota `|Date
|idViagem|`Chave de identificacao da Viagem`|Numeric
|nomeViagem|`Nome da Viagem`|String
|nomeMotorista|`Nome do motorista`|String



# Códigos de erro
Caso nao seja informado dtViagem (erro 422): 
```JS
{
    "message": "The given data was invalid.",
    "errors": {
        "dtViagem": [
            "O campo dtViagem é requerido!",
            "O campo dtViagem tem que ser do tipo Data DD/MM/YYYY"
        ]
    }
}
```

# Resposta da API (sucesso 200): 

```JS
[
    {
        "idViagem": 33,
        "NomeViagem": "VGN_SAO PAULO_001",
        "idMotorista": 2531,
        "NomeMotorista": "ALEXSANDER MONTEIRO DA SILVA",
        "QtdeMinima": 1,
        "QtdeMaxima": 50,
        "ValorMaximo": 10000,
        "QtdeViagem": 0,
        "idStatusProcesso": 670,
        "StatusProcesso": "INICIADA",
        "Obs": "",
        "Rot": 10
    },
    {
        "idViagem": 34,
        "NomeViagem": "VGN_SAO PAULO_002",
        "idMotorista": 2531,
        "NomeMotorista": "ALEXSANDER MONTEIRO DA SILVA",
        "QtdeMinima": 1,
        "QtdeMaxima": 50,
        "ValorMaximo": 10000,
        "QtdeViagem": 0,
        "idStatusProcesso": 620,
        "StatusProcesso": "ROTEIRIZADA",
        "Obs": "",
        "Rot": 21
    },
    ...
]
```

