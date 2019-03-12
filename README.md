
<<<<<<< HEAD
# Introdução 
API's que serão usadas no projeto de sistema do Redespacho 

* Item 1
* Item 2
* Item 3
  
+ Item 1
+ Item 2
+ Item 3
  
- Item 1
- Item 2
- Item 3
=======
# Introdução [create an anchor](#anchors-in-markdown)  
A API de consulta de pedidos traz os pedidos de acordo com o filtro pre definido 

# Visão global
A API por defaut tem que receber no minimo um parametro para poder realizar os filtros
[Consulta de Pedidos](ConsultaPedidos/teste.md)
# Códigos de erro
Caso nao seja informado nada a API retornara 
```JS
[  
   {  
      "erro":"Campos vazios"
   }
]
```
Campos invalidos (#some-markdown-heading)
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

# Resposta da API

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
>>>>>>> ad54f3abc4a1b6b80e7afdbcba2e8ca491f224e9
