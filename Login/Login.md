
# Introdução
O endpoint que realiza Login

# Visão global
API que realiza o login e gera token para validação, o token deve ser usado no header de todas as Requisições

```JS
headers: 
   { 
     Authorization: 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC8yMDEuMzkuOTIuNjBcL2FwaV9obWdcL3YzXC9hcGlcL2xvZ2luIiwiaWF0IjoxNTUyNDI0NDU5LCJleHAiOjE1NTI0MjgwNTksIm5iZiI6MTU1MjQyNDQ1OSwianRpIjoiWXhtYUlqR0VpVFppRDdTUyIsInN1YiI6MjUyMCwicHJ2IjoiODdlMGFmMWVmOWZkMTU4MTJmZGVjOTcxNTNhMTRlMGIwNDc1NDZhYSIsImlkQmFzZSI6MiwibmFtZSI6IkFOVE9OSU8gV0lMTElBTiBCQVJST1MgTElNQSIsInVzZXJuYW1lIjoiQU5UT05JTy5MSU1BIn0.O_xX5M6SUIKTnJMdhMTvdgFtQ8N_cXZcHbgHn3LaUh0'
     }
```
### Solicitação Post
> 201.39.92.60/api_hmg/v3/api/login

### Parametros
```JS
   {
    "username":"Fulano.bertano",
    "password":"123456789"
}
```

### Resposta (sucesso 200)
```JS
  {
    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC8yMDEuMzkuOTIuNjBcL2FwaV9obWdcL3YzXC9hcGlcL2xvZ2luIiwiaWF0IjoxNTUyNDI0NDU5LCJleHAiOjE1NTI0MjgwNTksIm5iZiI6MTU1MjQyNDQ1OSwianRpIjoiWXhtYUlqR0VpVFppRDdTUyIsInN1YiI6MjUyMCwicHJ2IjoiODdlMGFmMWVmOWZkMTU4MTJmZGVjOTcxNTNhMTRlMGIwNDc1NDZhYSIsImlkQmFzZSI6MiwibmFtZSI6IkFOVE9OSU8gV0lMTElBTiBCQVJST1MgTElNQSIsInVzZXJuYW1lIjoiQU5UT05JTy5MSU1BIn0.O_xX5M6SUIKTnJMdhMTvdgFtQ8N_cXZcHbgHn3LaUh0"
   }
```

### Resposta Erro (erro 400)
```JS
{
    "error": "invalid_credentials"
}
```



   




