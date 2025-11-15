# Projeto Móvel (ConectaFé) 

Projeto da disciplina de programação de dispositivos móveis com ReactNative + Expo (Android)

Orientador: Prof. Luiz Gustavo Turatti

A solução compartilhada neste repositório consiste no desenvolvimento de uma plataforma para ...

## Equipe do projeto

202503832251 - Fabricio Luis Costa Barreto Soares  

202302378961 - Isabella Martins de Souza 

202308508261 - Matheus Barros Souza

## Sumário

1. Requisitos
2. Configuração de acesso aos dados
3. Estrutura do projeto
4. Instale os requisitos do projeto
5. Executando o projeto
6. Telas do projeto

A ordem dos itens do sumário pode e deve ser ajustada para melhor entendimento sobre o seu projeto

Lembre-se que todas as instruções presentes neste arquivo devem permitir que outra pessoa seja capaz de clonar o repositório público e seguir os passos para utilizar o projeto


## 🔧 Requisitos:

- NodeJS LTS versão v22.18.0

- React Native versão 10.9.3

- ExpoGo (link googlePlayStore) / (link applePlayStore)

- Banco de dados: Firebase Firestore (NoSQL – Document Database)
O Firestore é um banco orientado a documentos, onde dados são armazenados em coleções e documentos.
No projeto utilizamos as seguintes coleções:

1. users – Armazena os dados de cada usuário (nome, e-mail, tipo de conta, documento, admin etc.).
2. donationRequests – Armazena todas as campanhas de doação, com título, descrição, categoria, cidade, prazo e autor da campanha.

Cada documento dentro de uma coleção funciona como um registro contendo seus campos individuais.

### 🗃️ Tabela 'usuarios' com os seguintes campos:
Como o projeto utiliza Firebase Firestore (banco NoSQL), segue o equivalente das coleções em formato de tabelas SQL:
id            : UUID (PRIMARY KEY)
timestamp     : TIMESTAMP
nomeCompleto  : TEXT
telefone      : TEXT
email         : TEXT
tipoConta     : TEXT          -- ('doador' | 'igreja' | 'admin')
documento     : TEXT          -- CPF ou CNPJ
isAdmin       : BOOLEAN       -- apenas administradores

## 🔐 Configuração de acesso ao banco de dados
O aplicativo utiliza Firebase Firestore (banco NoSQL em nuvem).
A configuração equivalente ao padrão solicitado:

DATABASE_URL=https://firestore.googleapis.com/v1/projects/meuapp-8a35f/databases/(default)/documents
DATABASE_KEY=AIzaSyB0qK1St8cBpWEHqVTIND8IX3AEnhYo

## 📁 Estrutura do projeto:
meuappConectafe/
├── apresentacao
│   ├── apresentacao.pdf
│   └── apresentacao.pptx
├── backend
│   ├── .cursor
│   ├── .expo
│   ├── .vscode 
│   ├── app
│   ├── node_modules
│   ├── scripts
│   ├── .gitignore
│   ├── app.json
│   ├── eslint.config.js
│   ├── expo.env.d.ts
│   ├── package-lock.json
│   ├── package.json
│   ├── readme.md
│   └── tsconfig.json
├── dist
│   ├── _expo
│   ├── (tabs)
│   ├── assets
│   ├── src
│   ├── _sitemap.html
│   ├── +not-found.html
│   ├── assetmap.json
│   ├── donation-details.html
│   ├── donation-requests.html
│   ├── explore.html
│   ├── favicon.icon
│   ├── forgot-password.html
│   ├── index.html
│   ├── metadata.json
│   ├── modal.html
│   ├── new-donation-request.html
│   ├── profile.html
│   └── register.html
├── documentacao
│   ├── 01_cartaDeApresentacao.pdf
│   ├── 02_cartaDeAutorizacao.pdf
│   ├── 03_declaracaoDeUsoDeDadosPublicos.pdf
│   ├── 04_roteiroDeExtensao.pdf
│   └── documentacao.md
├── frontend
│   ├── assets
│   ├── componentes
│   ├── constants
│   ├── contexts
│   ├── hooks
│   └── scripts
├── video
│   ├── apresentacao.gif
│   ├── apresentacao.mkv
│   ├── apresentacao.mp4
│   └── video.txt  
└── readme.md

## 📦 Instale os requisitos do projeto:

Instruções para instalação em um computador com Windows 11

Caso não tenha o chocolatey instalado, inicie o preparo do sistema abrindo um terminar do powershell com privilégio de administrador

```
PS> Set-ExecutionPolicy AllSigned

PS> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

PS> choco --version
```

Com o chocolatey instalado, continuamos com a instalação dos requisitos do projeto

```
PS> choco install nodejs-lts -y

PS> choco install openjdk17 -y

PS> choco install nvm -y
```

## 🚀 Execute o projeto:

```
npx expo start
```

## Telas do projeto

Capture todas as telas do projeto e identifique-as

Tela 1: login

Tela 2: criacao de usuario

Tela 3: recuperacao de senha

Tela 4: tela inicial 

Tela 5: campanhas em aberto

Tela 6: Igreja edita ou exclui campanha

Tela 7: igreja cria nova campanha

Tela 8: doador escolhe campanha para doação
