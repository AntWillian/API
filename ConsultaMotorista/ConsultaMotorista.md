# Introdução
A API que traz dados de motorista por filtros

 
# Visão global
A API recebe parametros e atraves deles filtra os motorista 


### Solicitação Get

> 201.39.92.60/api_hmg/v3/api/driver/search?situacao=&placa=&NomeMotorista=

## Parâmetros
|Campo                    |Descricao|               
|----------------|----------------|
|NomeMotorista|Nome do motorista|
|situacao|0 = Inativo<br>1 = Ativo|
|placa|Placa do carro do motorista|


### Códigos de erro 

Caso não seja informado nenhum parametro na requisção (erro 400)
```JS
{
	"status": "erro",
    "errors": {
        "erro": [
            "campos vazios"
        ]
    }
}
```

Caso o parametro `Placa`  seja informado mas não possua cadastro  (erro 400)
```JS
{
	"status": "erro",
    "errors": {
        "placa": [
            "Placa não cadastrada"
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
## Resposta

```JS
[  
	{  
		"idPessoa":181,  
		"Nome":"ADEILTON OLIVEIRA DE SANTANA",  
		"Cidade":"S\u00c3O BERNARDO DO CAMPO",  
		"Cep":"09850550",  
		"FoneCelular":"11912349999",  
		"FoneComercial":"",  
		"FoneResidencial":"",  
		"Email":"",  
		"Placas":"XXX0000"  
	}  
]
```
