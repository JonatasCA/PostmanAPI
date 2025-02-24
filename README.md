# 📌 Automação de Testes de API com Postman e Newman

Este projeto demonstra técnicas de automação de testes de API utilizando **Postman** e **Newman CLI**, além de integração com **GitHub Actions** para execução automática dos testes e publicação de relatórios via **GitHub Pages**.

## 🚀 Tecnologias Utilizadas

- **Postman** → Criação e execução de testes de API  
- **Newman CLI** → Execução dos testes via linha de comando  
- **GitHub Actions** → Automação dos testes a cada commit  
- **GitHub Pages** → Publicação de relatórios de testes  

## 👤 Estrutura do Projeto

```
💟 MeuProjetoAPITests  
│── 📂 .github/workflows/    # Configuração do GitHub Actions  
│── 📂 reports/              # Relatórios gerados pelo Newman  
│── PDIProjectCollection.json    # Collection de testes  
│── PDIProjectEnviromentDEV.json # Ambiente de testes  
│── README.md                # Documentação do projeto  
```

## ▶️ Como Executar os Testes Localmente

### 1️⃣ Instalar o Node.js e o Newman

Antes de rodar os testes, você precisa ter o **Node.js** instalado. Depois, instale o **Newman** globalmente:

```sh
npm install -g newman
```

### 2️⃣ Clonar o Repositório

```sh
git clone https://github.com/JonatasCA/PostmanAPI.git
cd PostmanAPI
```

### 3️⃣ Executar os Testes com o Newman

Para rodar os testes da collection:

```sh
newman run PDIProjectCollection.json -e PDIProjectEnviromentDEV.json
```

Se quiser gerar um relatório HTML dos testes:

```sh
newman run PDIProjectCollection.json -e PDIProjectEnviromentDEV.json -r cli,html --reporter-html-export reports/newman-report.html
```

## 🤖 Execução Automática no GitHub Actions

Toda vez que um commit for feito, os testes serão executados automaticamente via **GitHub Actions**.

### 📌 O que o Workflow faz?

- Instala o **Node.js** e o **Newman**.  
- Executa os testes da collection do **Postman**.  
- Gera um relatório HTML dos testes.  
- Publica o relatório no **GitHub Pages**.  

### 📌 Como visualizar os testes no GitHub Actions?

1. Vá até a aba **"Actions"** no repositório do GitHub.  
2. Clique no workflow **"Testes do Postman e Publicação no GitHub Pages"**.  
3. Veja os logs da execução e os testes realizados.  

## 🌍 Acessar os Relatórios no GitHub Pages

Após a execução do workflow, o relatório HTML estará disponível em:

[https://JonatasCA.github.io/PostmanAPI/newman-report.html](https://JonatasCA.github.io/PostmanAPI/newman-report.html)

## 🛠️ Principais Funcionalidades

✅ Automação completa dos testes de API via **Postman** e **Newman**  
✅ Execução local e remota via **GitHub Actions**  
✅ Publicação automática dos relatórios no **GitHub Pages**  
✅ Validação de **status code**, **response time** e **resposta da API**  
✅ Uso de **variáveis dinâmicas** e **ambientes** no Postman  

## 📝 Licença

Este projeto é livre para estudo e uso, sinta-se à vontade para contribuir! 😃
