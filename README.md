# PROVA UCSBR

## Criar um usuário utilizando o metodo abaixo:

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

## Fazer Login Utilizando este Método 

POST /api/authenticate HTTP/1.1
Host: hom.onelegacychurch.com
Content-Type: application/json
Content-Length: 84

{
	"username": "salusou@icloud.com",
	"password": "@Sp1r3@12",
	"rememberMe": true
}

Ao fazer o login vc receberá um token que deve ser colocado no HEAD dos métodos. 
 
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

```
{
    "id": 21052,
    "login": "salusou",
    "firstName": "Samuel",
    "lastName": "Souza",
    "cellphone": "37999615374",
    "email": "salusou@icloud.com",
    "imageUrl": null,
    "activated": true,
    "langKey": "pt-br",
    "createdBy": "anonymousUser",
    "createdDate": "2020-05-08T10:19:08.779Z",
    "lastModifiedBy": "salusou",
    "lastModifiedDate": "2022-06-03T19:16:12.138611Z",
    "userAddress": {
        "id": 21052,
        "addressData": null
    },
    "authorities": [
        "ROLE_FINANCIAL",
        "ROLE_USER",
        "ROLE_ADMIN"
    ],
    "churchList": [],
    "religionId": null,
    "religionFilter": true,
    "memberChurchId": null,
    "churchName": null,
    "memberChurchDate": null,
    "enableTransmissionNotifications": true,
    "enableEventNotifications": true,
    "enableLiturgyItemNotifications": true,
    "enablePodcastNotifications": true,
    "fullName": "Samuel Souza",
    "cpfCnpj": "00000000000"
}
```





