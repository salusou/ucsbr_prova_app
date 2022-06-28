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
```



### Exemplo do BODY do Usuário

```
{
    "id": number,
    "login": string,
    "firstName": string,
    "email": "salusou@icloud.com",
}

```

### Exemplo do GetConnect; 

```
Future<Response<User>> registerUser(User user) => post('$restURL/register', user, contentType: 'application/json');
	
Future<Response<String>> loginUser(Map<String, dynamic> login) => post('$restURL/authenticate', login, contentType: 'application/json');

Future<Response<User>> getAccount(String token) => get('$restURL/api', headers: {'Authorization': 'Bearer $token'}, contentType: 'application/json');



