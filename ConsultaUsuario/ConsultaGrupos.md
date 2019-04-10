
# Introdução

A API usada para consultar grupos de acesso

### Solicitação Get
> 201.39.92.60/api_hmg/v3/api/person/group
  

### Códigos de erro

 
erros inesperados (erro 500)
```JS

{
    "status": "erro",
    "errors": {
        "erro": [
            "Erro no servidor"
        ]
    }
}

```

## Resposta

  

Sucesso (200)

```JS

[
    {
        "idGrupo": 27,
        "NomeGrupo": "REDESPACHO - COORDENAÇÃO"
    },
    {
        "idGrupo": 28,
        "NomeGrupo": "REDESPACHO - LIDERES"
    },
    {
        "idGrupo": 29,
        "NomeGrupo": "REDESPACHO - OPERADORES"
    }
]

```

# Resposta
|Campo |Descricao| Tipo
|----------------|----------------|----------------|
|idGrupo|Chave identificadora do grupo|Numeric|required
|NomeGrupo|Nome do Grupo|String|required

