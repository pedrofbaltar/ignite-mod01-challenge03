<img alt="Ignite" src="https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fad01ee79-762a-4775-bbb6-354f2f42879a%2Fcover-node.js.png?table=block&id=59ccb235-aecd-43a6-a06b-f09a24e7ede8&width=3840&userId=2851198d-6d7e-47d6-b66a-5928d7b96353&cache=v2" />

<h3 align="center">
  Desafio 1-3: Corrigindo o código
</h3>

<p align="center">
  🧠 Aplicação de gerenciamento de tarefas - (ToDo).
</p>

---

## 🚀 Sobre o desafio

Nesse desafio havia uma aplicação Node.js que estava em processo de desenvolvimento mas que já possuáa os testes necessários para fazer toda a validação dos requisitos.

Essa aplicação realiza o CRUD (**C**reate, **R**ead, **U**pdate, **D**elete) de repositórios de projetos. Além disso, é possível dar likes em repositórios cadastrados, aumentando a quantidade de likes em 1 a cada vez que a rota é chamada.

A estrutura de um repositório ao ser criado é a seguinte:

```js
  {
    id: uuid(),
    title,
    url,
    techs,
    likes: 0
  }
```

Descrição de cada propriedade:

- **id** deve ser um uuid válido;
- **title** é o título do repositório (por exemplo "unform");
- **url** é a URL que aponta para o repositório (por exemplo "[https://github.com/unform/unform](https://github.com/unform/unform)");
- **techs** é um array onde cada elemento deve ser uma string com o nome de uma tecnologia relacionada ao repositório (por exemplo: ["react", "react-native", "form"]);
- **likes** é a quantidade de likes que o repositório recebeu (e que vai ser incrementada de 1 em 1 a cada chamada na rota de likes).

Note que a quantidade de likes deve sempre ser zero no momento de criação.

---

### 💻 Instalação e Execução do Projeto

- Clone este repositório

```
$ git clone https://github.com/pedrofbaltar/ignite-challenge03
```

- Navegue até o diretório principal do projeto

```
$ cd ignite-challenge03
```

- Instale as dependências com o Yarn

```
$ yarn
```

- Rode a suite de testes

```
$ yarn test
```

- Execute o projeto

```
$ yarn dev
```

---

### 🗺️ Rotas da aplicação

Aqui teremos uma breve descrição de cada rota.

### GET `/repositories`

A rota deve retornar uma lista contendo todos os repositórios cadastrados.

### POST `/repositories`

A rota deve receber `title`, `url` e `techs` pelo corpo da requisição e retornar um objeto com as informações do repositório criado e um status `204`.

### PUT `/repositories/:id`

A rota deve receber `title`, `url` e `techs` pelo corpo da requisição e o `id` do repositório que deve ser atualizado pelo parâmetro da rota. Deve alterar apenas as informações recebidas pelo corpo da requisição e retornar esse repositório atualizado.

### DELETE `/repositories/:id`

A rota deve receber, pelo parâmetro da rota, o `id` do repositório que deve ser excluído e retornar um status `204` após a exclusão.

### POST `/repositories/:id/like`

A rota deve receber, pelo parâmetro da rota, o `id` do repositório que deve receber o like e retornar o repositório com a quantidade de likes atualizada.

---

### 🤨 Observações

Você pode ter acesso à documentação no Notion sobre as rotas e testes clicando [aqui](\https://www.notion.so/Desafio-03-Corrigindo-o-c-digo-c15c8a2e212846039a367cc7b763c6dd).

---

### 📜 LIcença

Esse projeto está sob a licença do MIT. Veja o arquivo [LICENSE](./LICENSE).

---

Feito com 💜 por <a href="https://www.linkedin.com/in/pedro-felipe-baltar-2a26a31ab/">Pedro Felipe Baltar</a>
