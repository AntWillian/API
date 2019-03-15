# Introdução
A API para consultar motoristas

### Solicitação  Get

> 201.39.92.60/api_hmg/v3/api/driver/searchId

## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|----------------|
|idMotorista|Chave identificadora do motorista|Int|required



### Códigos de erro 

id não informado ou invalido (erro 400)
```JS
{
    "errors": {
        "erro": [
            "Id invalido"
        ]
    }
}
```

## Resposta
|Campo |Descricao| Tipo
|----------------|----------------|----------------
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


Sucesso (200)
```JS
[  
	{  
		"idPessoa":4488,  
		"Login":"fulano.bertano",  
		"Senha":"fulano.bertano",  
		"Nome":"FULANO BERTANO",  
		"RazaoSocial":null,  
		"TipoPessoa":"F",  
		"CPF":"76467349776",  
		"RG":"0124578963",  
		"CNPJ":"",  
		"IE":"888888888888",  
		"Endereco":"RUA BORGES DE BARROS",  
		"Numero":"09",  
		"Complemento":null,  
		"Bairro":"SUMAREZINHO",  
		"Cidade":"SAO PAULO",  
		"UF":"SP",  
		"Cep":"05413011",  
		"FoneCelular":"",  
		"FoneComercial":"",  
		"FoneResidencial":"",  
		"Email":"ibhvjdvgjkvjds@dffdfd.com",  
		"idTipo":3,  
		"Tipo":"MOTORISTA",  
		"idBase":2,  
		"CNH":"00000",  
		"CNH_Vencto":"2020-10-12",  
		"GRIS_Codigo":"000",  
		"GRIS_Vencto":"2015-10-10",  
		"ContaPropria":"N",  
		"FormaPagto":null,  
		"CodBanco":null,  
		"NomeBanco":null,  
		"CodAgencia":null,  
		"ContaCorrente":null,  
		"ContaPoupanca":"N",  
		"Ter_Nome":null,  
		"Ter_CPF":null,  
		"Ter_GrauParentesco":null,  
		"NomeBase":"S\u00c3O PAULO",  
		"idSituacao":1,  
		"Situacao":"ATIVO",  
		"idGrupoAcesso":0,  
		"NomeGrupo":null,  
		"dtEmissao":"2019-03-14 19:52:27",  
		"idNivel":1,  
		"NomeNivel":"TESTE",  
		"dtNascimento":"2020-10-12",  
		"PIS":"888888888888"  
	}  
]
```

