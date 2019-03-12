
# Introdução
A API que traz dados detalhado do pedido

# Visão global
A API recebe apenas um parametro, o id do Pedido

### Solicitação Get
> 201.39.92.60/api_hmg/v3/api/order?idPedido=100


### Códigos de erro
Caso a API nao reconheca a requisisao retorna 'erro'


### Resposta
```JS
{  
   "pedido":{  
      "idCliente":27,
      "NomeCliente":"MARISA",
      "idPedido":5746894,
      "idTipoOperacao":1,
      "idModalidade":1,
      "NomeModalidade":"NORMAL",
      "PedidoCliente":"240794046",
      "QtdVolumes":1,
      "NomeBaseOrigem":"SAO PAULO",
      "NomeBaseDestino":"FORTALEZA",
      "NomeLocalTipo":"VIAGEM DE ENTREGA",
      "idLocal":100890,
      "idSetor":725,
      "idDropPoint":0,
      "NomeSetor":"600",
      "EntregaBarrada":"",
      "EntregaEmBuscas":"",
      "NomeLocal":"VA - ALBERTO",
      "dtPrevEntregaOriginal":"29\/11\/2018",
      "dtPrevEntrega":"29\/11\/2018",
      "idStatus":101,
      "Status":"ENTREGA REALIZADA",
      "Ocorrencia":"REALIZADA",
      "mvIntegro":"S",
      "Processo":"ENTREGA",
      "StatusProcesso":"ENTREGA REALIZADA",
      "Destinatario":"CRISTINA RIBEIRO DE OLIVEIRA",
      "Endereco":"CEL CARVALHO, 2421",
      "Complemento":"ALTOS",
      "Bairro":"JARDIM IRACEMA",
      "Cidade":"FORTALEZA",
      "UF":"CE",
      "Cep":"60341641",
      "Numero":"2421",
      "Referencia":"",
      "Fone":"85 988355350",
      "Email":"",
      "Latitude":"-3.720527",
      "Longitude":"-38.587086",
      "idColeta":14348,
      "dtColeta":"16\/11\/2018",
      "TipoColeta":"AGENDADA",
      "dtRecebimento":"2018-11-19 23:25:31",
      "idViagem":6153,
      "NomeViagem":"GUARULHOS_01",
      "NomeMotorista":"RODRIGO SOARES SILVA",
      "PackList":"16112018161230",
      "dtRecArq":"2018-11-16 17:38:22",
      "NotaFiscal":"3942609",
      "SerieNF":"001",
      "Peso_Cli":1,
      "Cub_Cli":0,
      "ValorNF":195.97,
      "dtEmissaoNF":"14\/11\/2018",
      "NFe":"42181161189288030509550010039426091331951250",
      "Replay":"N",
      "TipoOperacao":"ENTREGA",
      "Garantida":"N"
   },
   "volumes":[  
      {  
         "idVolume":4013762,
         "idStatus":101,
         "Status":"ENTREGA REALIZADA",
         "idOcorrencia":101,
         "Ocorrencia":"REALIZADA",
         "idSetor":725,
         "NomeSetor":"600",
         "dtPrevEntrega":"2018-11-29",
         "dtPrevExpedicao":"2018-11-29",
         "dtPrevRecBase":"2018-11-29",
         "dtPrevEntregaOriginal":"2018-11-29",
         "CodigoBarras":"240794046",
         "NomeBase":"FORTALEZA",
         "idLocal":100890,
         "NomeLocal":"VA - ALBERTO",
         "dtEmissao":"26\/12\/2018 17:18:42",
         "Solucao":"TOTAL",
         "ArqProtocolo":null
      }
   ],
   "ckss":[  
      {  
         "Mensagem":"SCC",
         "AvisarMotorista":"N",
         "dtEmissao":"2019-01-14 13:30:27",
         "idTipo":1,
         "Usuario":"CARLOS ALBERTO IRES DE JESUS JUNIOR",
         "IdMsg":99358
      },
      {  
         "Mensagem":"SCC",
         "AvisarMotorista":"N",
         "dtEmissao":"2019-01-24 12:30:33",
         "idTipo":1,
         "Usuario":"CARLOS ALBERTO IRES DE JESUS JUNIOR",
         "IdMsg":101374
      },
      {  
         "Mensagem":"CNR",
         "AvisarMotorista":"N",
         "dtEmissao":"2019-01-30 14:04:16",
         "idTipo":1,
         "Usuario":"CARLOS ALBERTO IRES DE JESUS JUNIOR",
         "IdMsg":102677
      }
   ],
   "tickets":[  
      {  
         "idTicket":44461,
         "Solicitante":"Cliente",
         "Nome_Categoria":"Acarea\u00e7\u00e3o",
         "Nome_Criticidade":"Audi\u00eancia",
         "dtCadastro":"2018-12-26 17:46:44",
         "UltimaAlteracao":"2019-01-07 07:35:45",
         "Evento":"Em atendimento",
         "UltimaInteracao":"Alterou a categoria do Ticket de: DADOS DE RECEBEDOR para: ACAREA\u00c7\u00c3O"
      },
      {  
         "idTicket":35663,
         "Solicitante":"Cliente",
         "Nome_Categoria":"Informa\u00e7\u00f5es de Entrega",
         "Nome_Criticidade":"Audi\u00eancia",
         "dtCadastro":"2018-12-03 15:26:10",
         "UltimaAlteracao":"2018-12-04 08:35:19",
         "Evento":"Finalizado",
         "UltimaInteracao":"O pedido encontra-se em processo de transfer\u00eancia para a nossa filial respons\u00e1vel, estamos no aguardo da chegada do pedido em nosso cd, para que possamos realizar a entrega.\r\n"
      }
   ],
   "volumesHistorico":[  
      {  
         "dtEmissao":"16\/11\/2018 17:38:39",
         "Processo":"IMPORTA\u00c7\u00c3O DE ARQUIVO",
         "Log":"ARQUIVO RECEBIDO: 83158",
         "NomePessoa":"ARTHUR ANDRADE",
         "Tipo":"COLABORADOR",
         "NomeBase":"CARRIERS-MATRIZ",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"16\/11\/2018 17:52:00",
         "Processo":"0457709.xml",
         "Log":"ARQUIVO ASSOCIADO \u00c0 COLETA: 14348",
         "NomePessoa":"FELIPE SANTOS SOUZA",
         "Tipo":"COLABORADOR",
         "NomeBase":"CARRIERS-MATRIZ",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"19\/11\/2018 23:29:59",
         "Processo":"COLETA",
         "Log":"COLETADO - ENVIADO PARA BUFFER \/ NAO ETIQUETADO. ID LOTE 57691",
         "NomePessoa":"ALAN BRIAN VALENTE ANDRADE",
         "Tipo":"COLABORADOR",
         "NomeBase":"SAO PAULO",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"20\/11\/2018 17:23:58",
         "Processo":"SEPARA\u00c7\u00c3O",
         "Log":"VOLUME LIBERADO PARA SEPARA\u00c7\u00c3O",
         "NomePessoa":"RAFAEL SOARES SANTOS",
         "Tipo":"COLABORADOR",
         "NomeBase":"SAO PAULO",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"20\/11\/2018 17:38:14",
         "Processo":"ETIQUETAGEM",
         "Log":"VOLUME ETIQUETADO DE REDESPACHO PARA BASE: FORTALEZA ENDERE\u00c7O: FOR-39",
         "NomePessoa":"GISIANI GON\u00c7ALVES DA SILVA",
         "Tipo":"COLABORADOR",
         "NomeBase":"CARRIERS-MATRIZ",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"20\/11\/2018 18:48:02",
         "Processo":"TRANSFER\u00caNCIA",
         "Log":"VOLUME INSERIDO NO LOTE DE TRANSFER\u00caNCIA: 17495",
         "NomePessoa":"FLAVIO MORAES NUNES",
         "Tipo":"COLABORADOR",
         "NomeBase":"SAO PAULO",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"22\/11\/2018 16:37:01",
         "Processo":"TRANSFER\u00caNCIA",
         "Log":"VOLUME EM TRANSFER\u00caNCIA NA VIAGEM: 6242 PARA A DATA DE: 21\/11\/2018 COM O MOTORISTA: ERIK TOLEDO",
         "NomePessoa":"DANILO DOS SANTOS SILVA",
         "Tipo":"COLABORADOR",
         "NomeBase":"SAO PAULO",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"17\/12\/2018 16:51:58",
         "Processo":"TRANSFER\u00caNCIA",
         "Log":"RECEBIDO NA BASE DE DESTINO: FORTALEZA",
         "NomePessoa":"FRANCILENI DA COSTA FEITOSA",
         "Tipo":"COLABORADOR",
         "NomeBase":"FORTALEZA",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"18\/12\/2018 16:31:54",
         "Processo":"ROTEIRIZA\u00c7\u00c3O",
         "Log":"VOLUME ROTEIRIZADO POR SCANNER PARA A VIAGEM: 100890",
         "NomePessoa":"FRANCILENI DA COSTA FEITOSA",
         "Tipo":"COLABORADOR",
         "NomeBase":"FORTALEZA",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"18\/12\/2018 18:20:58",
         "Processo":"CONFER\u00caNCIA DE DESPACHO",
         "Log":"IN\u00cdCIO DA VIAGEM: 100890 DATA: 18\/12\/2018 COM O MOTORISTA: JOSE ALBERTO SABINO BORGES",
         "NomePessoa":"FRANCILENI DA COSTA FEITOSA",
         "Tipo":"COLABORADOR",
         "NomeBase":"FORTALEZA",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"26\/12\/2018 17:18:09",
         "Processo":"ENTREGA",
         "Log":"BAIXA DE ENTREGA (MANUAL): REALIZADA",
         "NomePessoa":"FRANCILENI DA COSTA FEITOSA",
         "Tipo":"COLABORADOR",
         "NomeBase":"FORTALEZA",
         "idVolume":4013762
      },
      {  
         "dtEmissao":"26\/12\/2018 17:18:42",
         "Processo":"CONFER\u00caNCIA DE VIAGEM",
         "Log":"CONFERENCIA DE VIAGEM. STATUS: CONFIRMA\u00c7\u00c3O DE ENTREGA REALIZADA",
         "NomePessoa":"FRANCILENI DA COSTA FEITOSA",
         "Tipo":"COLABORADOR",
         "NomeBase":"FORTALEZA",
         "idVolume":4013762
      }
   ],
   "viagemId":[  
      {  
         "idVolume":4013762,
         "idViagem":100890,
         "Status":"ENTREGA REALIZADA",
         "Observacao":""
      }
   ],
   "dadosProduto":[  
      {  
         "Produto":"MARISA"
      }
   ],
   "ultimaViagem":[  
      {  
         "idViagem":100890,
         "dtViagem":"2018-12-18",
         "NomeViagem":"VA - ALBERTO",
         "StatusProcesso":"CONFERIDA",
         "ordem":4
      }
   ]
}
```


## Descricao da resposta



|Campo                    |Quantidade parametros|Descricao| Tipo                 
|----------------|-------------------------------|-----------------------------|-----------------------------|
|Pedido|`58`|Dados geral do pedido consultado|Único|
|volumes|`19`|Dados de cada volume que contem no pedido|Múltiplo|
|ckss|`6`|Avivo para o motorista ou interno|Múltiplo|
|tickets|`8`|Comunicacao entre a carriers e os clientes|Múltiplo|
|volumesHistorico|`7`|Historico de movimentacao de cada volume|Múltiplo|
|viagemId|`4`|Cada viagem de tentativa de entrega que o pedido teve|Múltiplo|
|dadosProduto|`1`|Produtos do pedido|Múltiplo|
|ultimaViagem|`6`|Dados da ultima viagem q teve para o pedido|Único|

#

|                |Campo                         |Descrição   |Tipo                      |
|----------------|-------------------------------|-----------------------------|-----------------------------|
|Pedido|`idCliente`            |Chave identificadora do cliente            |int|
|Pedido|`NomeCliente`            |Nome do Cliente            |String|
|Pedido|`idPedido`|Chave identificadora principal do pedido|Int|
|Pedido|`idTipoOperacao`|chave identificadora do tipo de entrega  |
|Pedido|`idModalidade`|1:normal <br> 2: entrega|Int|
|Pedido|`NomeModalidade`|nome do tipo de modalidade|String|
|Pedido|`PedidoCliente`|chave identificadora para o cliente|String|
|Pedido|`QtdVolumes`|Informa quantos volumes tem o pedido|Int|
|Pedido|`NomeBaseOrigem`|Base de onde o pedido chegou|String|
|Pedido|`NomeBaseDestino`|Base de destino do pedido|String|
|Pedido|`NomeLocalTipo`|Onde o pedido esta no momento <br> 1: Cliente <br> 2: Base <br> 3: Viagem de entrega <br> 4: Viagem de tranferencia|String|
|Pedido|`idLocal`|chave de identificação do local <br>  1: Id Cliente<br> 2:Id base <br> 3: id Viagem entrega <br> 4:id Viagem de tranferencia|Int|
|Pedido|`idSetor`|chave identificadora do setor|Int|
|Pedido|`idDropPoint`|chave identificadora do drop q o pedido sera entregue|Int|
|Pedido|`NomeSetor`|nome do setor do pedido|
|Pedido|`EntregaBarrada`|caso o pedido seja impedido de ser entregue esse campo vem preenchido com '1'|Int|
|Pedido|`EntregaEmBuscas`|caso o pedido esteja sendo procurado esse campo vem preenchido com '1'|Int|
|Pedido|`NomeLocal`|descricao do local|String|
|Pedido|`dtPrevEntregaOriginal`|Data de previsao de entrega prevista|Date|
|Pedido|`dtPrevEntrega`|Data de entrega ajustada|Date|
|Pedido|`idStatus`|Chave identificadora do status|Int|
|Pedido|`Status`|Nome do status|String|
|Pedido|`Ocorrencia`|Nome da ocorrencia|String|
|Pedido|`mvIntegro`|S: sim <br> N: não|
|Pedido|`Processo`|descricao do processo onde se encontra o pedido|String|
|Pedido|`StatusProcesso`|status do processo|String|
|Pedido|`Destinatario`|Nome do destinatario |String|
|Pedido|`Endereco`|Endereço de entrega|String|
Pedido|`Complemento`|Complemento do endereço|String|
Pedido|`Bairro`|Bairro de entrega|String|
Pedido|`Cidade`|Cidade de entrega|String|
Pedido|`UF`|Estado de entrega|String|
Pedido|`Cep`|Cep de entrega|String|
Pedido|`Numero`|Numero do local de entrega|String|
Pedido|`Referencia`|referencia do endereço de entrega|String|
Pedido|`Fone`|telefone de contato do destinatario|String|
Pedido|`Email`|email de contato do destinatario|String|
Pedido|`Latitude`|latitude do endereco de entrega|String|
Pedido|`Longitude`|longitude do endereco de entrega|String|
Pedido|`idColeta`|chave identificadora da coleta|int
Pedido|`dtColeta`|data que ocorreu a coleta|Date
Pedido|`TipoColeta`|1: Agendada<br> 2: Avulsa<br> 3: Adicionada|String
Pedido|`dtRecebimento`|data de recebimento da coleta|Date Time|
Pedido|`idViagem`|Chave identificadora da viagem de coleta|Int|
Pedido|`NomeViagem`|Nome da viagem de coleta|String|
Pedido|`NomeMotorista`|Nome do motorista reponsavel pela viagem|String|
Pedido|`PackList`|identificado do arquivo|String|
Pedido|`dtRecArq`|Data que o arquivo foi inportado no sistema|Date Time|
Pedido|`NotaFiscal`|Numero da nota fiscal|String|
Pedido|`SerieNF`|numero de serie da nota fiscal|String|
Pedido|`Peso_Cli`|peso real do cliente|Double
Pedido|`Cub_Cli`|cubagem do pedido|Double
Pedido|`ValorNF`|valor da nota fiscal|Float
Pedido|`dtEmissaoNF`|data de emissao da nota|Date
Pedido|`NFe`|chave da nota fiscal|String
Pedido|`Replay`|S: sim <br> N: não|String|
Pedido|`TipoOperacao`|nome da operacao do pedido|String
Pedido|`Garantida`|S: sim <br> N: não|String|
Volumes|`idVolume`|Chave identificadora do volume|Int|
Volumes|`idStatus`|Chave identificadora do status|Int|
Volumes|`Status`|Nome do status|String|
Volumes|`idOcorrencia`|Chave identificadora da ocorrencia|Int|
Volumes|`idSetor`|Chave identificadora do setor|Int|
Volumes|`NomeSetor`|Nome do setor|String|
Volumes|`dtPrevEntrega`|Data de previsao de entrega|Date|
Volumes|`dtPrevExpedicao`|Data de previsao de viagem de entrega|Date|
Volumes|`dtPrevRecBase`|data de previsao de chegar a base de destino|Date|
Volumes|`dtPrevEntregaOriginal`|data ajustada de entrega|Date|
Volumes|`CodigoBarras`|Codigo de barras do volume da etiqueta do cliente|String|
Volumes|`NomeBase`|Base em que o pedido está|String|
Volumes|`idLocal`|chave de identificação do local <br>  1: Id Cliente<br> 2:Id base <br> 3: id Viagem entrega <br> 4:id Viagem de tranferencia|Int|
Volumes|`NomeLocal`|Onde o pedido esta no momento <br> 1: Cliente <br> 2: Base <br> 3: Viagem de entrega <br> 4: Viagem de tranferencia|String|
Volumes|`dtEmissao`|Data de criação deste volume|Date Time
Volumes|`Solucao`|P: parcial<br> T: total|String
Volumes|`ArqProtocolo`|dado de recebedor dos produtos|String
ckss|`Mensagem`|texto informativo|String
ckss|`AvisarMotorista`|S: sim<br> N: não|String
ckss|`dtEmissao`|data de cadastro|Date Time
ckss|`idTipo`||
ckss|`Usuario`|Nome do usuario que cadastrou|String
ckss|`IdMsg`|chave identificadora|Int
tickets|`idTicket`|chave identificadora|Int
tickets|`Solicitante`|1: carriers<br>2: embarcador <br> 3: base|String|
tickets|`Nome_Categoria`|nome da categorioa do ticket|String
tickets|`Nome_Criticidade`|nome da criticidade do ticket|String
tickets|`dtCadastro`|data de cadastro do ticket|Date Time
tickets|`UltimaAlteracao`|data da ultima alteracao do ticket|Date Time
tickets|`Evento`|estado que o ticket está|String
tickets|`UltimaInteracao`|ultima auteracao do ticket|String|
volumesHistorico|`dtEmissao`|data de cadastro|Date Time
volumesHistorico|`Processo`|processo do log|String
volumesHistorico|`Log`|mensagem do log (ação)|String
volumesHistorico|`NomePessoa`|nome do usuario do log|String
volumesHistorico|`Tipo`|tipo do usuario|String
volumesHistorico|`NomeBase`|nome da base do usuario|String
volumesHistorico|`idVolume`|chave identificadora do volume|Int
viagemId|`idVolume`|chave identificadora do volume|Int
viagemId|`idViagem`|chave identificadora da viagem|Int
viagemId|`Status`|status do volume na viagem|String
viagemId|`Observacao`|mensagem complementar|String
dadosProduto|`Produto`|nome do produto|String
ultimaViagem|`idViagem`|chave identificadora da viagem|Int
ultimaViagem|`dtViagem`|data que ocorreu a viagem|Date
ultimaViagem|`NomeViagem`|nome da viagem|String
ultimaViagem|`StatusProcesso`|nome do status que da viagem|String
ultimaViagem|`ordem`|ordem de entrefa dessa viagem|Int




