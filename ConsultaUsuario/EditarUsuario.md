
# Introdução

A API usada para editar usuarios

### Solicitação Put
> 201.39.92.60/api_hmg/v3/api/person/update

  

## Parâmetros

|Campo |Descricao| Tipo| Requeridos
|----------------|----------------|----------------|----------------|
|idPessoa|Chave identificadora do Usuario|Numeric|required
|nome|Nome do Usuario|String|required
|cep|Numero do cep|Int|required
|endereco|Nome da rua|String|required
|numero|Numero da casa | String|required
|bairro|Nome do bairro|String|required
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
|senha|Senha de login|String|required
|idGrupoAcesso|Chave identificadora do grupo de acesso|Numeric|required|


  
  

### Códigos de erro

  idPessoa invalido ou nao informado (erro 400)

```JS

{
	"status": "erro",
	"errors": {
		"idPessoa ": [
			"idPessoa não informado"
		]
	}
}

```

Campos invalidos (erro 400)

```JS

{

	"message": "The given data was invalid.",
	"errors": {
		"nome": [
			"O campo nome é requerido!",
			"O nome deve ter pelo menos 3 caracteres"
		],
		"cep": [
			"O campo CPF é requerido!",
			"O CEP deve ter 8 dígitos!",
			"O CEP deve ser numerico!"
		],

		"endereco": [
			"O campo endereco é requerido!",
			"O endereco deve ter pelo menos 3 caracteres!"
		],

		"numero": [
			"O campo numero é requerido!"
		],

		"bairro": [
			"O campo bairro é requerido!",
			"O campo bairro deve ter pelo menos 3 caracteres!",
			"O campo bairro deve ter no maximo 50 caracteres!"
		],

		"cidade": [
			"O campo cidade é requerido!",
			"O campo cidade deve ter pelo menos 3 caracteres!",
			"O campo cidade deve ter no maximo 50 caracteres!"
		],

		"uf": [
			"O campo uf é requerido!",
			"O campo uf deve ter 2 caracteres!",
			"O campo uf deve ter no maximo 2 caracteres!"
		],

		"situacao": [
			"O campo situacao é requerido!"
		],
		
		"dtNasc": [
			"O campo dtNasc tem que ser do tipo Data DD/MM/YYYY"
		],

		"rg": [
			"O campo rg é requerido!",
			"O campo rg Tem que ser Numerico!"
		],

		"email": [
			"Email invalido"
		],

		"celular": [
			"O campo celular Tem que ser Numerico!"
		],

		"cpf": [
			"O campo cpf é requerido!",
			"O campo cpf Tem que ser Numerico!"
		],

		"login": [
			"O campo login é requerido!",
			"O campo login deve ter pelo menos 3 caracteres!",
			"O campo login deve ter no maximo 30 caracteres!"
		],

		"senha": [
			"O campo senha é requerido!",
			"O campo senha deve ter pelo menos 3 caracteres!",
			"O campo senha deve ter no maximo 8 caracteres!"
		],
		
		"idGrupoAcesso": [
			"O campo idGrupoAcesso é requerido!",
			"O campo idGrupoAcesso Tem que ser Numerico!"
		],

	}

}

```

  
  

Validacao de CPF (erro 400)

```JS

{
	"status": "erro",
	"errors": {
		"cpf": [
			"CPF invalido"
		]
	}
}

```

  

```JS

{
	"status": "erro",
	"errors": {
		"cpf": [
			"Cpf já cadastrado"
		]
	}
}

```

## Resposta

  

Sucesso (200)

```JS

{
	"status": "ok",
	"sucesso": {
		"sucesso": [
			"Usuario editado"
		]
	}
}

```

  

erro (500)

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
