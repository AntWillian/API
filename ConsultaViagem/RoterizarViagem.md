
# Introdução
A API para criar novas viagens


### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/trip/new

## Parâmetros
|Campo                    |Descricao| Tipo|  Requeridos            
|----------------|----------------|----------------|----------------|
|idViagem|Chave identificadora da viagem|Numeric|required
|roterizacao|1=Menor distancia<br>2=Cep<br>3=Ordem de leitura<br>4=Ordem alfabética<br>|Numeric|required


### Códigos de erro 

Campos inválidos (erro 422)
```JS
{
    "status": "erro",
    "errors": {
        "roterizacao": [
            "O campo roterizacao é requerido!",
            "O campo roterizacao  tem que ser numerico"
        ],
         "idViagem": [
            "O campo idViagem  tem que ser numerico",
            "O campo idViagem é requerido!"
        ]
    }
}
```
Viagem com status divergente (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Esta viagem não pode ser salva! Verifique a Situação da viagem."
        ]
    }
}
```

Erro ao pesquisar dados da viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Erro ao pesquisar dados da Viagem"
        ]
    }
}
```

Pedidos múltiplos que não foram adicionado todos os volumes (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "O(s) pedido(s) {pedidos} são múltiplos e nem todos os volumes foram adicionados a viagem. Adicione seus pares ou remova os volumes adicionados"
        ]
    }
}
```

erro ao pesquisar Pedidos múltiplos que não foram adicionado todos os volumes (erro 400)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Erro ao pesquisar multiplos Volumes da Viagem"
        ]
    }
}
```

erro ao roteirizar viagem (erro 500)
```JS
{
    "status": "erro",
    "errors": {
        "viagem": [
            "Erro ao roterizar viagem"
        ]
    }
}
```



## Resposta
sucesso (200)
```JS
{
    "status": "ok",
    "sucesso": {
        "viagem": [
            "Viagem salva com sucesso!"
        ]
    }
}
```