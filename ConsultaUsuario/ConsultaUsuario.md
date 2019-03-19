
# Introdução

A API usada para consultar usuarios

### Solicitação Get
> 201.39.92.60/api_hmg/v3/api/person/search
  

## Parâmetros

|Campo |Descricao| Tipo
|----------------|----------------|----------------
|NomePessoa|Nome do Usuario|String|
|situacao|0 = Inativo<br>1 = Ativo <br> 2 = Todos|Numeric|


  
  

### Códigos de erro

  Nenhum campo informado (erro 400)

```JS

{
    "errors": {
        "geral": [
            "campos vazios"
        ]
    }
}

```
erros inesperados (erro 500)
```JS

{
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
		"idPessoa":436,  
		"Nome":"DENIS SOUZA PEREIRA",  
		"NomeGrupo":"OPERA\u00c7\u00c3O - OPERADORES",  
		"NomeBase":"CARRIERS-MATRIZ",  
		"FoneCelular":"11111111111",  
		"Email":"",  
		"Bairro":"JARDIM MARACA",  
		"Cidade":"SAO PAULO",  
		"Cep":"05861400"  
	},  
	{  
		"idPessoa":4489,  
		"Nome":"Editado",  
		"NomeGrupo":"BACKOFFICE - COORDENA\u00c7\u00c3O",  
		"NomeBase":"CARRIERS-MATRIZ",  
		"FoneCelular":"000",  
		"Email":"ibhvjdvgjkvjds@dffdfd.com",  
		"Bairro":"iiiiii",  
		"Cidade":"popopopp",  
		"Cep":"11111111"  
	},  
	...
]

```

# Resposta
|Campo |Descricao| Tipo
|----------------|----------------|----------------|
|idPessoa|Chave identificadora do usuario|Numeric
|Nome|Nome do Usuario|String|required
|Cep|Numero do cep|Numeric|required
|NomeBase|Nome da base|String|required
|Bairro|Nome do bairro|String|required
|Cidade|Nome da cidade|String|required
|Email|E-mail de contato|String
|FoneCelular|Numero de celular|Numeric
|NomeGrupo|Nome do grupo de acesso|Numeric|required|
