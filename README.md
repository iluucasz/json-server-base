# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Projetos Front-end.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.


### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"


regras de uso:

As regras de roteamento que você forneceu parecem definir permissões de acesso para recursos específicos com base nos padrões de URL. Vou explicar cada regra:

    /664/*: Nessa configuração, os recursos correspondentes a URLs que começam com "/664/" têm as seguintes permissões:
        Usuários devem estar logados para escrever no recurso.
        Qualquer pessoa pode ler (visualizar) o recurso.

    /660/*: Recursos correspondentes a URLs que começam com "/660/" têm as seguintes permissões:
        Usuários devem estar logados para escrever ou ler o recurso.

    /644/*: Recursos correspondentes a URLs que começam com "/644/" têm as seguintes permissões:
        Os usuários devem ser proprietários do recurso para escrever nele.
        Qualquer pessoa pode ler o recurso.

    /640/*: Recursos correspondentes a URLs que começam com "/640/" têm as seguintes permissões:
        Os usuários devem ser proprietários do recurso para escrever nele.
        Os usuários devem estar logados para ler o recurso.

    /600/*: Recursos correspondentes a URLs que começam com "/600/" têm as seguintes permissões:
        Os usuários devem ser proprietários do recurso para escrever ou ler o recurso.

    /444/*: Nessa configuração, recursos correspondentes a URLs que começam com "/444/" têm as seguintes permissões:
        Ninguém pode escrever (modificar) o recurso.
        Qualquer pessoa pode ler o recurso.

    /440/*: Recursos correspondentes a URLs que começam com "/440/" têm as seguintes permissões:
        Ninguém pode escrever no recurso.
        Os usuários devem estar logados para ler o recurso.

    /400/*: Nessa configuração, recursos correspondentes a URLs que começam com "/400/" têm as seguintes permissões:
        Ninguém pode escrever no recurso.
        Os usuários devem ser proprietários do recurso para ler o recurso.

Essas regras definem restrições de acesso com base nos padrões de URL. Elas especificam quem pode escrever, ler e em que circunstâncias. Por exemplo, em "/644/*", os usuários devem ser proprietários para escrever, mas qualquer pessoa pode ler. Certifique-se de que essas regras correspondam às necessidades do seu aplicativo e do seu modelo de segurança.
