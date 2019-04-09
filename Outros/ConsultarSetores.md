
# Introdução
A API para consultar setores


### Solicitação POST
> 201.39.92.60/api_hmg/v3/setor/search


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



## Resposta

```JS
[
    {
        "idMacroRegiao": 1,
        "idSetor": 2,
        "NomeSetor": "0100",
        "ApelidoSetor": "CENTRO"
    },
    {
        "idMacroRegiao": 1,
        "idSetor": 152,
        "NomeSetor": "0101",
        "ApelidoSetor": "TESTE A"
    },
    ...
 ]  
```
