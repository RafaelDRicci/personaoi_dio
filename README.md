# Sistema de gerenciamento de pessoas em API REST com Spring Boot
Projeto desenvolvido para o Desafio de Projetos " [Desenvolvendo um sistema de gerenciamento de pessoas em API REST com Spring Boot](https://web.dio.me/lab/desenvolvendo-um-sistema-de-gerenciamento-de-pessoas-em-api-rest-com-spring-boot/learning/59e5edaa-470d-44a3-8519-c082d765c71d) " da [Digital Innovation One](https://digitalinnovation.one) ministrado por [Rodrigo Peleias](https://github.com/rpeleias).

O Projeto trata-se de uma API Rest para cadastro de pessoas com Spring Boot.

# O que foi desenvolvido?

Foi desenvolvido operações básicas da arquitetura REST para pessoa:

- GET - Faz uma busca por todas as pessoas ou uma pelo Id 
- POST - Cria uma nova instância de pessoa
- PUT - Atualiza uma pessoa
- DELETE - Delete uma pessoa

O Projeto disponibilizada na nuvem pelo [Heroku](https://dashboard.heroku.com/apps).

As requisições de pessoa podem ser acessadas em https://personapidio1.herokuapp.com/api/v1/poeple, em operações GET retorna todas as pessoas registradas em banco por um JSON, caso queria uma específica adicionar /[Id]. Operações de POST são enviadas em um JSON com os campos de pessoa e também com o telefone. PUT necessitam, além dos campos de pessoa e telefone, o id de ambos no JSON e o id no endereço. DELETE é necessário apenas o id no endereço.

JSON Exemplo com todos os campos(PUT):

~~~JSON
{
    "id" : 4,
    "firstName" : "Rafael",
    "lastName" : "Ricci",
    "cpf" : "555.555.555-555",
    "birthDate" : "11-03-1994",
    "phones" : [
        {
            "id": 2,
            "type" : "MOBILE",
            "number" : "(11)999999999"
        }
    ]
}
~~~

Obs; o sistema faz validação de cpf.

## Tecnologias Utilizadas:
- Maven
- Spring boot DevTools
- Lombok
- Spring Web
- Spring Data JPA
- Spring Boot Actutor
- H2 Database
- MapStructor

