
# Introdução
A API de consulta de pedidos traz os pedidos de acordo com o filtro pre definido 

# Visão global
A API por defaut tem que receber no minimo um parametro para poder realizar os filtros

### Solicitação Get 
> 201.39.92.60/api_hmg/v3/api/order?idgrupo=&idCliente=&destinatario=&endereco=&idPedido=&pedidoCliente=&notaFiscal=&codigoBarras=&dataColeta=&dataCadastro=&cpf=

# Parâmetros
|Campo                  |Descricao             
|----------------|-------------------------------|
|idgrupo|`Grupo do cliente`|
|idCliente|`Chave de identificacao do cliente`|
|destinatario|`Nome do destinatario final`|
|endereco|`Endereco de entrega do pedido`|
|idPedido|`Chave de identificacao principal do pedido`|
|pedidoCliente|`Chave de identificacao do pedido do cliente`|
|notaFiscal|`numero da nota `|
|codigoBarras|`Codigo de barras da etiqueta do cliente`|
|dataColeta|`Data que o pedido foi coletado na loja`|
|dataCadastro|`Data que o pedido foi cadastrado no sistema`|
|cpf|`CPF do destinatario`|


# Códigos de erro
Caso nao seja informado nada a API retornara (erro 400): 
```JS
{
    "status": "erro",
    "errors": {
        "geral": [
            "Campos vazios"
        ]
    }
}
```
Campos invalidos (erro 400): 
```JS
{
    "message": "The given data was invalid.",
    "errors": {
        "idgrupo": [
            "O campo idgrupo tem que ser numerico"
        ],
        "idCliente": [
            "O campo idCliente tem que ser numerico"
        ],
        "idPedido": [
            "O campo idPedido tem que ser numerico"
        ],
        "notaFiscal": [
            "O campo notaFiscal tem que ser numerico"
        ],
        "dataColeta": [
            "O campo dataColeta tem que ser do tipo Data DD/MM/YYYY"
        ],
        "dataCadastro": [
            "O campo dataCadastro tem que ser do tipo Data DD/MM/YYYY"
        ]
    }
}
```

# Resposta da API (sucesso 200): 

```JS
[  
   {  
      "Tipo":"ENTREGA",
      "Embarcador":"RICARDO ELETRO",
      "Pedido Cliente":"3224829501",
      "Id Pedido":100,
      "Volumes":1,
      "Destinatario":"DIOGO SILVA ALMEIDA",
      "Endereco":"RUA PADRE JOAO ANTONIO ANDREONI 87",
      "Cidade":"SAO PAULO",
      "Data Coleta":"2017-08-16",
      "Status":"ENTREGA REALIZADA",
      "Processo":"ENTREGA",
      "Status Processo":"ENTREGA REALIZADA"
   }
]
```

