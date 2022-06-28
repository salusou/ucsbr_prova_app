# PROVA UCSBR

## Criar um usuário utilizando o metodo abaixo:

```
POST /api/register HTTP/1.1
Host: hom.onelegacychurch.com
Content-Type: application/json
Content-Length: 77

{
    "login": "",
    "email": "",
    "firstName": "",
    "password": ""
}
```

## Fazer Login Utilizando este Método 

```
POST /api/authenticate HTTP/1.1
Host: hom.onelegacychurch.com
Content-Type: application/json
Content-Length: 84

{
	"username": "salusou@icloud.com",
	"password": "@Sp1r3@12",
	"rememberMe": true
}

```

**Ao fazer o login vc receberá um token que deve ser colocado no HEAD dos métodos.** 
 
## Após fazer a authenticação incluir o token no cabeçalho do método

```
GET /api/account HTTP/1.1
Host: hom.onelegacychurch.com
Authorization: Bearer TOKEN
Content-Type: application/json
Content-Length: 84

{
	"username": "salusou@icloud.com",
	"password": "@Sp1r3@12",
	"rememberMe": true
}




### Exemplo do BODY do Usuário


{
    "id": number,
    "login": string,
    "firstName": string,
    "email": "salusou@icloud.com",
}





