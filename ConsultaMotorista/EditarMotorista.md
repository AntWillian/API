# Introdução
A API usada para editar motoristas

### Solicitação  Put

> 201.39.92.60/api_hmg/v3/api/driver/update

## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|----------------|
|idMotorista|Chave identificadora do motorista|Int|required
|nome|Nome do motorista|String|required
|cep|Numero do cep|Int|required
|endereco|Nome da rua|String|required
|numero|Numero da casa | String|required
|bairro|Nome do bairro|String|required
|cidade|Nome da cidade|String|required
|uf|Sigla do estado|String|required
|situacao|0 = Inativo<br>1 = Ativo|Int|required|
|cnh|numero da carteira de motorista|Numeric
|cnhVencto|data de vencimento cnh|Date
|tipoPessoa|F=fisica <br> J=juridico|String
|email|E-mail de contato|String
|dtNasc|Data de nascimento|Date
|razaoSocial|Nome da razao social|String
|cpf|Numero do cpf|Numeric|required|
|rg|Numero do rg|Numeric
|cnpj|Numero do cnpj|Numeric
|IE|Numero da inscrição estadual|Numeric
|pis|Numero do pis|Numeric
|complemento|Complemento do endereco|String
|celular|Numero de celular|Numeric
|fone|Telefone fixo|Numeric
|residencial|Numero residencial|Numeric
|gris|Numero do gris|Numeric
|grisVencto|Data de vencimento do gris|Date
|login|Nome de login|String|required
|senha|Senha de login|String|required


### Códigos de erro 
idMotorista invalido ou nao informado (erro 400)
```JS
{
	"status": "erro",
    "errors": {
        "idMotorista": [
            "Id invalido"
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
        "cnh": [
            "O campo cnh é requerido!",
            "O campo cnh Tem que ser Numerico!"
        ],
        "cnhVencto": [
            "O campo cnhVencto é requerido!",
            "O campo cnhVencto tem que ser do tipo Data DD/MM/YYYY"
        ],
        "tipoPessoa": [
            "O campo tipoPessoa é requerido!"
        ],
        "dtNasc": [
            "O campo dtNasc é requerido!",
            "O campo dtNasc tem que ser do tipo Data DD/MM/YYYY"
        ],
        "rg": [
            "O campo rg é requerido!",
            "O campo rg Tem que ser Numerico!"
        ],
        "IE": [
            "O campo IE é requerido!",
            "O campo IE Tem que ser Numerico!"
        ],
        "PIS": [
            "O PIS é requerido!",
            "O campo PIS Tem que ser Numerico!"
        ],
        "email": [
            "Email invalido"
        ],
        "celular": [
            "O campo celular Tem que ser Numerico!"
        ],
        "fone": [
            "O campo fone Tem que ser Numerico!"
        ],
        "residencial": [
            "O campo residencial Tem que ser Numerico!"
        ],
        "gris": [
            "O campo gris Tem que ser Numerico!"
        ],
        "grisVencto": [
            "O campo grisVencto tem que ser do tipo Data DD/MM/YYYY"
        ],
        "cpf": [
            "O campo cpf Tem que ser Numerico!"
        ],
        "cnpj": [
            "O campo cnpj Tem que ser Numerico!"
        ]
    }
}
```

Validacao de CPF  (erro 400)
```JS
{
    "errors": {
        "cpf": [
            "CPF invalido"
        ]
    }
}
```

Validacao de CPF  (erro 400)
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


Erros não inesperados (erro 500)
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

Validacao de CNPJ(erro 400)
```JS
{
	"status": "erro",
    "errors": {
        "cnpj": [
            "CNPJ invalido"
        ]
    }
}
```

```JS
{
	"status": "erro",
    "errors": {
        "cnpj": [
            "CNPJ invalido"
        ]
    }
}
```
Erros inesperados (erro 500)
```JS
{
	"status": "erro",
    "errors": {
        "documento": [
            "preencher CPF ou CNPJ"
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
            "Motorista editado"
        ]
    }
}
```

