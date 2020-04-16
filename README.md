![Wallpaper GoStack](https://user-images.githubusercontent.com/58411170/79023960-f326d100-7b57-11ea-9a3b-d3fd0d6bf6bd.png)

<h2 align="center">
  Desafio 05: Primeiro projeto Node.js
</h2> 

<p align="center">
  Criado durante o bootcamp GoStack 11.
</p>

<p align="center">
 
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/gabriel-antero/challenge05-nodeJS">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/gabriel-antero/challenge05-nodeJS"> 
  <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/gabriel-antero/challenge05-nodeJS">
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/gabriel-antero/challenge05-nodeJS">
  
</p>

<p align="center">
  <a href="">Sobre o desafio<a/> |
  <a href="">Objetivos a realizar<a/> |
  <a href="">LICENÇA<a/>
</p>

## :information_source: Sobre o desafio

Aplicação que deve armazenar transações financeiras de entrada e saída, deve permitir o cadastro e a listagem dessas transações.

Feito utilizando testes automatizados.

## :dart: Objetivos realizados

<h3 align="center">Funcionalidades da aplicação</h3>

- [X] **`POST /transactions`**: A rota deve receber `title`, `value` e `type` dentro do corpo da requisição, sendo `type` o tipo da transação, que deve ser `income` para entradas (depósitos) e `outcome` para saidas (retiradas). Ao cadastrar uma nova transação, ela deve ser armazenada dentro de um objeto com o formato como o seguinte:

```json
{
  "id": "uuid",
  "title": "Salário",
  "value": 3000,
  "type": "income"
}
```

- [X] **`GET /transactions`**: Essa rota deve retornar uma listagem com todas as transações que você cadastrou até agora, junto com o valor de soma de entradas, retiradas e total de crédito. Essa rota deve retornar um objeto com o formato a seguir:

```json
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```

<h3 align="center">Específicação dos testes</h3>
<p align="center">Necessário realizar os seguintes testes:</p>

- [X] **`should be able to create a new transaction`**: Para que esse teste passe, sua aplicação deve permitir que uma transação seja criada, e retorne um json com a transação criado.

- [X] **`should be able to list the transactions`**: Para que esse teste passe, sua aplicação deve permitir que seja retornado um objeto contendo todas as transações junto ao balanço de income, outcome e total das transações que foram criadas até o momento.

- [X] **`should not be able to create outcome transaction without a valid balance`**: Para que esse teste passe, sua aplicação não deve permitir que uma transação do tipo `outcome` extrapole o valor total que o usuário tem em caixa, retornando uma resposta com código HTTP 400 e uma mensagem de erro no seguinte formato: `{ error: string }`

## :memo: LICENÇA

Projeto sobre licença MIT. Mais informações em [LICENÇA]().

---

Trechos desse conteúdo copiado do arquivo do desafio.
