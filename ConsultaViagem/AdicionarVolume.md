
# Introdução
A API adicionar volumes na viagenm


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/trip/addVolume

## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|----------------|
|codigoBarras|código da etiqueta carriers|Numeric|required
|idViagem|Chave identificadora da viagem|Numeric|required


### Códigos de erro 

Campos inválidos (erro 422)
```JS
{
    "status": "erro",
    "errors": {
        "CodigoBarras": [
            "O campo Codigo de Barras é requerido!",
            "O Codigo de Barras deve ter formato EAN13!",
            "O Codigo de Barras deve ser numerico!"
        ],
         "idViagem": [
            "O campo idViagem  tem que ser numerico",
            "O campo idViagem é requerido!"
        ]
    }
}
```
código de barras invalido (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "CodigoBarras": [
            "Codigo de barras invalido"
        ]
    }
}
```


Viagens que estejam em status inválidos (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Esta viagem não pode ser roteirizada! Verifique o Status da viagem!"
        ]
    }
}
```


Erros de sintaxe na alteração do status da viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Ocorreu erro um erro durante alteração de status da viagem! Tente novamente"
        ]
    }
}
```

Volume não cadastrado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Volume não encontrado"
        ]
    }
}
```

Volume já lido na viagem (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Este volume já foi lido nesta viagem"
        ]
    }
}
```

Volume já lido em outra viagem (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Este volume já foi roteirizado para a viagem: {dados da viagem}"
        ]
    }
}
```

Volume com entrega barrada (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Entrega barrada"
        ]
    }
}
```

Volume com ocorrencia (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Este volume está com ocorrência de: {dados ocorrencia}"
        ]
    }
}
```
Volume não etiquetado (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Volume não etiquetado!"
        ]
    }
}
```

Tipo de Operação Incoerentes (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "O Tipo de Operação do pedido é diferente da viagem !"
        ]
    }
}
```

Tipo de Operação Incoerentes (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "O Tipo de Operação do pedido é diferente da viagem !"
        ]
    }
}
```
Erro ao Pesquisar dados do volume (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Erro ao pesquisar dados do volume"
        ]
    }
}
```

Erro ao Pesquisar tipo de viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Erro ao pesquisar Tipo de viagem"
        ]
    }
}
```

Erro ao Pesquisar dados do ultimo volume da viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "volume": [
            "Erro ao pesquisar Ultimo volume"
        ]
    }
}
```

Erro ao Pesquisar dados do modelo da base (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "base": [
            "Erro ao pesquisar Modelo da base"
        ]
    }
}
```
Erro ao Pesquisar valores da viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Erro ao pesquisar valores da Viagem"
        ]
    }
}
```
Valor máximo da viagem atingido (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Valor máximo da viagem já foi atingido!"
        ]
    }
}
```

Quantidade máxima da viagem atingido (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Quantidade de volumes máxima da viagem já foi atingida!"
        ]
    }
}
```
Erro ao pesquisar dados da viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "Viagem": [
            "Erro ao pesquisar dados da Viagem"
        ]
    }
}
```
Erro de sintaxe (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "servidor": [
            "erro ao conectar-se ao servidor"
        ]
    }
}
```

## Resposta
```JS
{
    "status": "ok",
    "sucesso": {
        "volume": [
            "Volume adicionado com sucesso!"
        ]
    }
}
```