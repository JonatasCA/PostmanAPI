# 📌 Automação de Testes de API com Postman e Newman

Este projeto demonstra técnicas de automação de testes de API utilizando **Postman** e **Newman CLI**, além de integração com **GitHub Actions** para execução automática dos testes.

## 🚀 Tecnologias Utilizadas

- **Postman** → Criação e execução de testes de API  
- **Newman CLI** → Execução dos testes via linha de comando  
- **GitHub Actions** → Automação dos testes a cada commit   

## 👤 Estrutura do Projeto

```
💟 PostmanAPI  
│── 📂 .github/workflows/    # Configuração do GitHub Actions  
│── 📂 reports/              # Relatórios gerados pelo Newman  
│── PDIProjectCollection.json    # Collection de testes  
│── PDIProjectEnviromentDEV.json # Ambiente de testes  
│── README.md                # Documentação do projeto  
```

## ▶️ Como Executar os Testes Localmente

### 1️⃣ Instalar o Newman e o Newman Reporter

Para executar os testes, é necessário ter o **Node.js** instalado. 
Agora instale o **Newman** e **Newman Reporter** globalmente:

```sh
npm install -g newman
```
```sh
npm install -g newman-reporter-html
```

### 2️⃣ Clonar o Repositório

```sh
git clone https://github.com/JonatasCA/PostmanAPI.git
cd PostmanAPI
```

### 3️⃣ Executar os Testes com o Newman

Para executar os testes da collection:

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

- Instala o **Node.js**.  
- Instala o **Newman**.  
- Executa os testes da collection do **Postman**.    

### 📌 Como visualizar os testes no GitHub Actions?

1. Vá até a aba **"Actions"** no repositório do GitHub.  
2. Clique no workflow **"Testes do Postman**.  
3. Veja os logs da execução e os testes realizados.  

## 🛠️ Principais Funcionalidades

✅ Automação completa dos testes de API via **Postman** e **Newman**  
✅ Execução local e remota via **GitHub Actions**  
✅ Validação de **status code**, **response time** e **resposta da API**  
✅ Uso de **variáveis dinâmicas** e **ambientes** no Postman  

## 📝 Licença

Este projeto é livre para estudo e uso, sinta-se à vontade para contribuir! 😃
