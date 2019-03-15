# Introdução
A API para consultar setores por motoristas

### Solicitação  Get

> 201.39.92.60/api_hmg/v3/api/driver/setor/search

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
|Campo                    |Descricao|     
|----------------|----------------|
|idMacroRegiao|Chave identificadora da regiao|
|idSetor|Chave identificadora do setor|
|NomeSetor|nome do setor|
|ApelidoSetor|Apelido identificador do setor|
|Atende|S=sim <br> N=nao|


Sucesso (200)
```JS
[  
	{  
		"idMacroRegiao":1,  
		"idSetor":2,  
		"NomeSetor":"0100",  
		"ApelidoSetor":"CENTRO",  
		"Atende":"N"  
	},  
	{  
		"idMacroRegiao":1,  
		"idSetor":3,  
		"NomeSetor":"0110",  
		"ApelidoSetor":"BARRA FUNDA",  
		"Atende":"N"  
	},  
	... 
]
```

