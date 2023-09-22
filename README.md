### Documentação da API
## URL Base: https://us-central1-your-project-id.cloudfunctions.net/app

## Hello World 
Endpoint: http://127.0.0.1:5001/fir-crud-restapi-e30db/us-central1/app/hello-world

Descrição: Este endpoint simplesmente retorna uma mensagem "Hello World!" para verificar se o servidor está funcionando corretamente.

Método HTTP: GET

Resposta de exemplo: Hello World!

## Criar um novo usuário
Endpoint: http://127.0.0.1:5001/fir-crud-restapi-e30db/us-central1/app/api/create

Descrição: Este endpoint permite criar um novo usuário com as informações fornecidas no corpo da solicitação. 

O usuário é armazenado no banco de dados Firestore.

Método HTTP: POST

Corpo da solicitação:

{
  "id": "1",
  "name": "Nome do Usuário",
  "email": "usuario@email.com",
  "password": "senha123"
}

Resposta de exemplo: A resposta será vazia com um código de status HTTP 200 se a operação for bem-sucedida.

## Ler um usuário pelo ID
Endpoint: http://127.0.0.1:5001/fir-crud-restapi-e30db/us-central1/app/api/read/{id}

Descrição: Este endpoint permite ler as informações de um usuário específico com base no ID fornecido na URL.

Método HTTP: GET

Parâmetro da URL: Substitua {id} pelo ID do usuário que deseja ler.

Resposta de exemplo:

{
  "id": "1",
  "name": "Nome do Usuário",
  "email": "usuario@email.com",
  "password": "senha123"
}

## Ler todos os usuários
Endpoint: http://127.0.0.1:5001/fir-crud-restapi-e30db/us-central1/app/api/read

Descrição: Este endpoint permite ler todas as informações de todos os usuários armazenados no banco de dados 
Firestore.

Método HTTP: GET

Resposta de exemplo:

[
  {
    "id": "1",
    "name": "Nome do Usuário",
    "email": "usuario@email.com",
    "password": "senha123"
  },
  {
    "id": "2",
    "name": "Outro Usuário",
    "email": "outro@email.com",
    "password": "outrasenha"
  }
  // Outros usuários
]

## Atualizar informações do usuário
Endpoint: http://127.0.0.1:5001/fir-crud-restapi-e30db/us-central1/app/api/update/{id}

Descrição: Este endpoint permite atualizar as informações de um usuário específico com base no ID fornecido na URL. As informações atualizadas devem ser fornecidas no corpo da solicitação.

Método HTTP: PUT

Parâmetro da URL: Substitua {id} pelo ID do usuário que deseja atualizar.

Corpo da solicitação:
{
  "name": "Novo Nome do Usuário",
  "email": "novousuario@email.com",
  "password": "novasenha"
}

Resposta de exemplo: A resposta será vazia com um código de status HTTP 200 se a operação for bem-sucedida.

## Excluir um usuário
Endpoint: http://127.0.0.1:5001/fir-crud-restapi-e30db/us-central1/app/api/delete/{id}

Descrição: Este endpoint permite excluir um usuário específico com base no ID fornecido na URL.

Método HTTP: DELETE

Parâmetro da URL: Substitua {id} pelo ID do usuário que deseja excluir.


