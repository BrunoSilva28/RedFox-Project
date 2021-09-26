## PROJETO REDFOX - BACKEND CASE

- Este é um projeto básico de Backend, utilizando Typescript, MySQL, além das bibliotecas knexJs e expressJs, desenvolvido para atender aos modelos REST API.

---
## DESCRIÇÃO DO PROJETO

- O projeto consiste em simular a metodologia CRUD na estruturação de Plataforma de captura de informações de Pokemons, através de endpoints `GET` para alimentar as demandas.

---
### LINK DA DOCUMENTAÇÃO NO POSTMAN: `https://documenter.getpostman.com/view/15825773/UUxxgoME`

---
### `GET` AllParticipants

`https://cubo-projeto.herokuapp.com/participants`

- Este endpoint retorna todos os participantes do projeto.
- São exibidos dos colaboradores seus `firstName`,`lastName` e respectivos `participation` como resposta.

### Body
- `No Content`

### Headers
- `No Content`

### Path Variables
- `No Content`

### Response Example
```
{
  "participants": [
    {
      "id": "1",
      "firstName": "Carlos",
      "lastName": "Moura",
      "participation": 5
    },
    {
      "id": "2",
      "firstName": "Fernanda",
      "lastName": "Oliveira",
      "participation": 15
    },
    {
      "id": "3",
      "firstName": "Hugo",
      "lastName": "Silva",
      "participation": 20
    },
    {
      "id": "4",
      "firstName": "Eliza",
      "lastName": "Souza",
      "participation": 20
    },
    {
      "id": "5",
      "firstName": "Anderson",
      "lastName": "Santos",
      "participation": 40
    }
  ]
}
```
### Validation Restrictions
- Não há restrições.

---
### `POST` Create Participant

`https://cubo-projeto.herokuapp.com/participants`

- Este endpoint registra um novo participante do projeto.

### Body
```
{
    "firstName": "Gabriel",
    "lastName": "Silva",
    "participation": 10
}
```

### Headers
- `No Content`

### Path Variables
- `No Content`

### Response Example
```
{
  "message": "Participant created successfully!"
}
```
### Validation Restrictions
- `firstName` e `lastName` são informações obrigatórias, do tipo `string`.
- `participation` é um campo obrigatório, que deve ser um valor numérico, não-negativo e menor que 100.

---