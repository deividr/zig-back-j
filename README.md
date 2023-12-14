# Desafio técnico

Temos aqui uma API já pré-configurada usando o [Express](https://expressjs.com/pt-br/) para encapsulamento dos recursos HTTP.
Já temos configurado também o Typescript, Eslint e Prettier.

## Proposta de implementação:

### 1. Crie um endpoint `POST` chamado `/create-book` que vai receber um objeto JSON com a seguinte estrutura:

```
{
  "title": string,
  "author": string,
  "pages": number,
  "value": number
}
```

- Consistir se já não existe uma ocorrência com esse mesmo Título. Se sim, retornar uma mensagem de erro com HTTP response 400 (badRequest);
- Acrescentar a esse objeto um ID (numérico) gerado de forma randômica para ser um identificador único para cada novo `book` que for criado;
- Armazenar esse objeto em uma nova ocorrência num Array em memória;
- Retornar o objeto criado com a informação de Id e o código HTTP correto;

### 2. Crie um endpoint `GET` chamado `/get-book/:id`:

- Irá receber um `param` que será o Id do Book;
- Consultar no Array por esse id;
- Retonar o resultado se encontrado, ou retornar `not-found` usando o código HTTP correto;

### 3. Crie um endpoint `GET` chamado `/get-books?name=NameOfBook`:

- Irá receber um `query param` chamado `name`;
- Consultar no Array por qualquer elemento que contenha no nome uma `parte` dessa informação. Ex.: Se informado `eDoBo`, o livro que tenha o nome "Nom<b>eDoBo</b>ok" tem que ser selecionado;
- Retornar o resultado encontrado, se não encontrado retornar `null` e o código HTTP correto;
