# PROVA UCSBR

Criar um usuário utilizando o metodo abaixo:

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

Fazer Login Utilizando este Método 

POST /api/authenticate HTTP/1.1
Host: hom.onelegacychurch.com
Content-Type: application/json
Content-Length: 84

{
	"username": "salusou@icloud.com",
	"password": "@Sp1r3@12",
	"rememberMe": true
}



