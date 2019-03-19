
# Introdução

A API usada para consultar usuarios por id

### Solicitação Get
> 201.39.92.60/api_hmg/v3/api/searchId?idPessoa=
  

## Parâmetros

|Campo |Descricao| Tipo
|----------------|----------------|----------------|----------------|
|idPessoa|Chave identificadora do usuario|Numeric

### Códigos de erro

  idPessoa nao informado ou invaldo (erro 400)

```JS

{
    "errors": {
        "idPessoa": [
            "idPessoa invalido"
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
        "idPessoa": 436,
        "Login": "DENIS.SOUZA",
        "Nome": "DENIS SOUZA PEREIRA",
        "CPF": "33099924890",
        "RG": "335353848",
        "OrgExpedidor": "SP1",
        "Endereco": "RUA SIMON DE COLONIA",
        "Numero": "45",
        "Complemento": "",
        "Bairro": "JARDIM MARACA",
        "Cidade": "SAO PAULO",
        "UF": "SP",
        "Cep": "05861400",
        "FoneCelular": "11111111111",
        "Email": "",
        "idSituacao": 1,
        "idGrupoAcesso": 6,
        "dtNascimento": null
    }
]

```

# Resposta
|Campo |Descricao| Tipo
|----------------|----------------|----------------|
|idPessoa|Chave identificadora do Usuario|Numeric|required
|nome|Nome do Usuario|String|required
|cep|Numero do cep|Numeric|require
|endereco|Nome da rua|String|required
|numero|Numero da casa | String|reuired
|bairro|Nome do bairro|String|require
|cidade|Nome da cidade|String|required
|uf|Sigla do estado|String|required
|situacao|0 = Inativo<br>1 = Ativo|Int|required|
|email|E-mail de contato|String
|dtNasc|Data de nascimento|Date
|cpf|Numero do cpf|Numeric|required|
|OrgExpedidor|Órgão Expedidor|String
|complemento|Complemento do endereco|String
|celular|Numero de celular|Numeric
|login|Nome de login|String|required
|idGrupoAcesso|Chave identificadora do grupo de acesso|Numeric|required|
