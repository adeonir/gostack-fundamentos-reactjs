<h1 align="center">
  <img src="./assets/logo-gostack.svg" atl="GoStack Bootcamp" />
</h1>

<h3 align="center">
  Desafio 7: Aplicação web do GoFinances com ReactJS
</h3>

<p align="center">
  Desafio desenvolvido durante o <a href="https://rocketseat.com.br/gostack">Bootcamp GoStack</a> da Rocketseat.
  <br />
  <br />
  <a href="#tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#instalação-e-execução">Instalação e execução</a>
</p>

## Tecnologias

- [ReactJS](https://reactjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Axios](https://github.com/axios/axios)
- [Date-fns](https://github.com/date-fns/date-fns)
- [Styled-Components](https://styled-components.com/)
- [Polished](https://polished.js.org/)
- [React-Dropzone](https://github.com/react-dropzone/react-dropzone)
- [Filesize](https://filesizejs.com/)
- [ESLint](https://eslint.org/)
- [Prettier](https://prettier.io/)

## Sobre o desafio

Nesse desafio, eu continuei desenvolvendo a aplicação de gestão de transações, agora chamada de GoFinances. Irei praticar o que aprendi com ReactJS, utilizando TypeSript, rotas e envio de arquivos por formulário.

Essa aplicação irá se conectar ao backend do [Desafio 6](https://github.com/adeonir/gostack-database-upload-arquivo), irá exibir as transações criadas e permitir a importação de um arquivo CSV, gerando novos registros no banco de dados.

```bash
# Entre na pasta do desafio 6
$ cd database-upload-arquivo

# Rode a aplicação
$ yarn server
```

Tenha certeza que as informações da categoria, estão sendo retornadas junto com a transação do backend no seguinte formato:

```json
{
  "id": "c0512e43-6589-4dc8-bd0c-2a3f71b347aa",
  "title": "Loan",
  "type": "income",
  "value": "1500.00",
  "category_id": "d93eccc7-64bb-4268-b825-9200103f3a8b",
  "created_at": "2020-04-20T00:00:49.620Z",
  "updated_at": "2020-04-20T00:00:49.620Z",
  "category": {
    "id": "d93eccc7-64bb-4268-b825-9200103f3a8b",
    "title": "Others",
    "created_at": "2020-04-20T00:00:49.594Z",
    "updated_at": "2020-04-20T00:00:49.594Z"
  }
}
```

### Funcionalidades da aplicação

- **`Listar as transações da API`**: A página `Dashboard` deve ser capaz de exibir uma listagem através de uma tabela, com o campo `title`, `value`, `type` e `category` de todas as transações que estão cadastradas na API.

- **`Exibir o balance da API`**: A página `Dashboard` deve exibir o balance, que é retornado do backend, contendo o total geral, junto ao total de entradas e saídas.

- **`Importar arquivos CSV`**: A página `Import` deve permitir o envio de um arquivo no formato `csv` para o backend, que irá fazer a importação das transações para o banco de dados. O arquivo csv deve seguir o seguinte [modelo](./assets/file.csv).

### Específicação dos testes

Para esse desafio, temos os seguintes testes:

- **`should be able to list the total balance inside the cards`**: Para que esse teste passe, a aplicação deve permitir que seja exibido na Dashboard, cards contendo o total de `income`, `outcome` e o total da subtração de `income - outcome` que são retornados pelo balance do backend.

* **`should be able to list the transactions`**: Para que esse teste passe, a aplicação deve permitir que sejam listados dentro de uma tabela, todas as transações que são retornadas do backend.

- **`should be able to navigate to the import page`**: Para que esse teste passe, a aplicação deve permitir a troca de página através do Header, pelo botão que contém o nome `Importar`.

- **`should be able to upload a file`**: Para que esse teste passe, a aplicação deve permitir que um arquivo seja enviado através do componente de drag-n-drop na página de `import`, e que seja possível exibir o nome do arquivo enviado para o input.

## Instalação e execução

```bash
# Clone esse repositório
$ git clone https://github.com/adeonir/gostack-fundamentos-reactjs fundamentos-reactjs

# Entre no diretório
$ cd fundamentos-reactjs

# Instale as dependências
$ yarn

# Rode a aplicação
$ yarn start

# Rode os testes
$ yarn test
```

## Licença

Esse projeto está sob a licença MIT.

---

Made with ♥️ by Adeonir Kohl
