# 🚀 JSON API Tester

Uma ferramenta web interativa e leve para testar requisições HTTP (GET/POST) a APIs RESTful, permitindo enviar variáveis dinâmicas com suporte a diferentes tipos de dados (string, número, booleano). Desenvolvida em HTML/CSS/JS puro, sem dependências externas — basta abrir o arquivo no navegador e começar a testar.

![Demonstração](https://img.shields.io/badge/status-estável-brightgreen) ![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow) ![Licença](https://img.shields.io/badge/licença-MIT-blue)

---

## ✨ Funcionalidades

- 🔗 **Requisições GET e POST** – escolha o método HTTP diretamente na interface.
- 📦 **Gerenciamento dinâmico de variáveis**:
  - Adicione quantas variáveis desejar.
  - Para cada variável, defina **nome**, **valor** e **tipo** (String, Número, Booleano).
  - Remova variáveis individualmente com um clique.
- 🔄 **Comportamento inteligente**:
  - **POST**: as variáveis são enviadas como JSON no corpo da requisição (`Content-Type: application/json`).
  - **GET**: as variáveis são automaticamente convertidas em **query string** e anexadas à URL.
- 📊 **Resposta detalhada**:
  - Exibe status HTTP, tempo de resposta (ms), URL final chamada.
  - Mostra o payload enviado e o corpo da resposta formatado (JSON ou texto).
- 🎨 **Interface moderna e responsiva** – funciona em desktop, tablet e mobile.
- ⚡ **Sem configuração** – 100% client-side, nenhum servidor ou instalação necessária.

---

## 🖥️ Como usar

### 1. Baixar o arquivo
Copie o conteúdo do arquivo `index.html` (gerado anteriormente) para um arquivo local com o mesmo nome.

### 2. Abrir no navegador
Clique duas vezes no arquivo ou arraste-o para uma janela do navegador (Chrome, Edge, Firefox, Safari).

### 3. Testar uma API
- **URL**: insira o endpoint desejado (ex: `https://jsonplaceholder.typicode.com/posts`).
- **Método**: escolha `GET` ou `POST`.
- **Variáveis**: adicione pares chave/valor que serão enviados.
  - Exemplo: `userId` (número `1`), `title` (string `"Meu post"`).
- Clique em **Enviar requisição** e veja a resposta em tempo real.

---

## 🧪 Exemplos de uso

### 🔹 Exemplo 1: GET com query string
- **URL**: `https://jsonplaceholder.typicode.com/comments`
- **Método**: `GET`
- **Variáveis**:
  | Nome      | Valor | Tipo   |
  |-----------|-------|--------|
  | postId    | 3     | Número |
  | _limit    | 2     | Número |

- **Resultado**: a ferramenta chamará `https://jsonplaceholder.typicode.com/comments?postId=3&_limit=2`.

### 🔹 Exemplo 2: POST com JSON
- **URL**: `https://jsonplaceholder.typicode.com/posts`
- **Método**: `POST`
- **Variáveis**:
  | Nome     | Valor                | Tipo   |
  |----------|----------------------|--------|
  | title    | Meu título incrível  | String |
  | body     | Conteúdo do post     | String |
  | userId   | 42                   | Número |

- **Corpo enviado**:
```json
{
  "title": "Meu título incrível",
  "body": "Conteúdo do post",
  "userId": 42
}
---

### 💡 Como usar o README

1. Crie um arquivo chamado `README.md` na mesma pasta do seu `index.html`.
2. Copie todo o conteúdo acima e cole no arquivo.
3. Se desejar, adicione um **screenshot** do projeto em funcionamento, substituindo o texto `![Demonstração]` por:
   ```markdown
   ![Screenshot do JSON API Tester](./screenshot.png)
