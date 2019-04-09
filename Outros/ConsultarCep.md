
# Introdução
A API para consultar endereço por cep


### Solicitação GET
> 201.39.92.60/api_hmg/v3/cep/search?cep=



## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|--------------|
|cep|numero do cep|Numeric|required




### Códigos de erro 

Erros de sintaxe ou inesperados (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "servidor": [
            "Erro no servidor"
        ]
    }
}
```
cep invalido ou  não encontrado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "cep": [
            "Nenhum cep encontrado"
        ]
    }
}
```


## Resposta

```JS
{
    "Endereco": "RUA MARIUCHA",
    "NomeBairro": "MOINHO VELHO",
    "NomeCidade": "SAO PAULO",
    "SiglaUF": "SP"
}
```
