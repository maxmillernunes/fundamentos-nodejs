# Fundamentos-de-nodejs
## Segundo desafio de nodejs do bootcamp GoStack.
Nesse desafio foi criado uma aplicação com o armazenamento em memória.
Essa será uma aplicação para armazenar transações financeiras de entrada e saída, que deve permitir o cadastro e a listagem dessas transações.

## Como usar?
- Assim que abrir o projeto no editor de codigo execulte um `yarn` para instalar as dependência do projeto.
- Após isso, pode rodar um `yarn dev:server` para rodar a aplicação que ficará disponível no endereço `http://localhost:3333`.
- Está disponível também os teste, para execultar, basta rodar `yarn test` e `jest` e `supertest` ira rodar a rotina de teste.

## Rotas da aplicação

- POST `/transactions:` A rota deve receber title, value e type dentro do corpo da requisição, sendo type o tipo da transação, que deve ser income para entradas (depósitos) e outcome para saídas (retiradas);

- GET `/transactions:` Rota que lista todos os transações;

## Rotas da aplicação

Aqui temos os teste realziados pela aplicação.

Para esse desafio temos os seguintes testes:

- `should be able to create a new transaction:` Para que esse teste passe, sua aplicação deve permitir que uma transação seja criada, e retorne um json com a transação criada.

- `should be able to list the transactions:` Para que esse teste passe, sua aplicação deve permitir que seja retornado um objeto contendo todas as transações junto ao balanço de income, outcome e total das transações que foram criadas até o momento.

- `should not be able to create outcome transaction without a valid balance:` Para que esse teste passe, sua aplicação não deve permitir que uma transação do tipo outcome extrapole o valor total que o usuário tem em caixa, retornando uma resposta com código HTTP 400 e uma mensagem de erro no seguinte formato: { error: string }
