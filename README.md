# todolist-java
#### Projeto desenvolvido com a ajuda da Rocketseat no Curso Online Gratuito de Java Spring Boot.

## Sobre
- O curso foi dividido em 5 aulas:
  - **Aula 01 - Construção back-end de uma aplicação de To-Do List**
    - Na primeira aula demos primeiros passos em Java e na construção da aplicação. Vimos os conceitos essenciais do Spring Boot e configuramos o ambiente de desenvolvimento com Java e Maven, instalando extensões e criando a estrutura do projeto.
  - **Aula 02 - Integração com Banco de Dados**
    - Na segunda aula aprendermos mais sobre desenvolvimento em Java, Spring Framework e interações com banco de dados e seguimos na construção do projeto usando as ferramentas mais modernas.
  - **Aula 03 - Implementando segurança nos dados do usuário**
    - Na terceira aprendemos aspectos cruciais de segurança e estruturação para garantir um acesso seguro à sua aplicação.
  - **Aula 04 - Atualizando tarefas e validação de rotas**
    - Nessa aula implementamos melhorias e funcionalidades e enriquecemos a interatividade do usuário com a nossa aplicação.
  - **Aula 05 - Deploy do Back-End**

  ### Recursos da API

  - **Criação de Usuários:** Crie um novo usuário fornecendo seu nome, nome de usuário e senha:

```http
POST http://localhost:8080/users/
{
    "name": "Katia Souza",
    "username": "katiasouza",
    "password": "12345"
}
```

- **Criação de Tarefas:** Crie uma nova tarefa especificando a descrição, título, prioridade, data de início e término. Você deve fornecer o ID do usuário no parâmetro `idUser`:

```http
POST http://localhost:8080/tasks/
{
    "description": "Tarefa para gravar aula de Tasks do curso de Spring Boot",
    "title": "Gravação de aula",
    "priority": "ALTA",
    "startAt": "2023-10-11T10:00:00",
    "endAt": "2023-10-11T14:00:00",
    "idUser": "750cd181-dd27-414d-bc72-e09197b1a341"
}
```

- **Acesso as tarefas já criadas**: Acesse as tarefas já criadas para o seu usuário. 

```
GET http://localhost:8080/tasks/

Ultilize Autênticação Básica com os dados do seu usuário...
```

- ***Atualizar uma tarefa***: Atualize algum campo já existente da tarefa especificando a descrição, título, prioridade, data de início ou término.
 
``` 
PUT https://localhost:8080/tasks/

{
    "Campo que você deseja alterar" = "Novo valor"
}
```

### Utilização do Spring Boot DevTools

Esta API utiliza o Spring Boot DevTools, uma ferramenta útil para auxiliar no desenvolvimento de aplicativos Spring Boot. Ele oferece recursos que facilitam o processo de desenvolvimento, incluindo a reinicialização automática do serviço toda vez que a aplicação sofre uma alteração no código-fonte.

### Use a API você mesmo!

No seu Framework de teste de API, ultilize a URL
> https://todolist-nop.onrender.com

Coloque uma "/" após a url e ultilize os paths citados acima em [Recursos da API](https://github.com/Nop-Dev/todolist-java/tree/main#recursos-da-api).