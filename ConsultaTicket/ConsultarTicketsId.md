
# Introdução
A API para pesquisar Ticket por id


### Solicitação GET
> 201.39.92.60/api_hmg/v3/api/ticket/selectTicketId/{idTicket}



## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|--------------|
|idTicket|Chave identificadora do Ticket|Numeric|required




### Códigos de erro 
Campos inválidos (erro 422)

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

Ticket  não criado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "Ticket ": [
            "'Nenhum Ticket encontrado"
        ]
    }
}
```
idTicket invalido ou  não encontrado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "idTicket": [
            "idTicket invalido"
        ]
    }
}
```


## Resposta

```JS
{
    "dadosTicket": [
        {
            "idPedido": 254,
            "Tipo": "BASE",
            "Solicitante": "Carriers",
            "Nome_Categoria": "Acareação",
            "Evento": "Em atendimento",
            "Nome_Criticidade": "Audiência",
            "Nome": "ANTONIO WILLIAN BARROS LIMA",
            "ultimaInteracao": "2019-04-05 18:16:11",
            "dataFinalizacao": "2019-04-05 18:16:11"
        }
    ],
    "dadosTicketInteracao": [
        {
            "Interacao": "kikikikikikikikikikikikikiki",
            "Log": "Abriu o ticket",
            "Nome": "ANTONIO.LIMA",
            "idTipo": 1,
            "dtEmissao": "2019-04-02 17:14:30",
            "Arquivo": ""
        },
        {
            "Interacao": null,
            "Log": "Interagiu no ticket",
            "Nome": "ANTONIO.LIMA",
            "idTipo": 1,
            "dtEmissao": "2019-04-05 16:30:24",
            "Arquivo": "2_base_Reembolso de Despesas.xlsx"
        },
        {
            "Interacao": "",
            "Log": "Finalizou o ticket",
            "Nome": "ANTONIO.LIMA",
            "idTipo": 1,
            "dtEmissao": "2019-04-05 16:35:53",
            "Arquivo": ""
        },
        {
            "Interacao": "teste",
            "Log": "Interagiu no ticket",
            "Nome": "ANTONIO.LIMA",
            "idTipo": 1,
            "dtEmissao": "2019-04-05 17:38:11",
            "Arquivo": ""
        },
        {
            "Interacao": "teste",
            "Log": "Interagiu no ticket",
            "Nome": "ANTONIO.LIMA",
            "idTipo": 1,
            "dtEmissao": "2019-04-05 17:38:18",
            "Arquivo": "2_base_Reembolso de Despesas.xlsx"
        },
        {
            "Interacao": "teste",
            "Log": "Interagiu no ticket",
            "Nome": "ANTONIO.LIMA",
            "idTipo": 1,
            "dtEmissao": "2019-04-05 17:58:49",
            "Arquivo": ""
        },
        {
            "Interacao": "teste",
            "Log": "Interagiu no ticket",
            "Nome": "ANTONIO.LIMA",
            "idTipo": 1,
            "dtEmissao": "2019-04-05 17:58:52",
            "Arquivo": "2_base_Reembolso de Despesas.xlsx"
        },
        {
            "Interacao": "",
            "Log": "Reabriu o ticket",
            "Nome": "ANTONIO.LIMA",
            "idTipo": 1,
            "dtEmissao": "2019-04-05 18:16:11",
            "Arquivo": ""
        }
    ],
    "dadosTicketPedido": [
        {
            "idPedido": 254,
            "idCliente": 39,
            "NomeCliente": "VIA VAREJO",
            "PedidoCliente": "16294023901",
            "NomeDest": "FERNANDO PEREIRA DE OLIVEIRA",
            "Fone": "11992514702",
            "idColeta": 0,
            "QtdVolumes": 1
        }
    ]
}
```
