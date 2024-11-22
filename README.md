Backend:
npm init

package name: (backend) dashboardcarros
version: (1.0.0) <enter>
description: <enter>
entry point: (index.js) src/server.js
test command: <enter>
git repository: <enter>
keywords: react, node, postgresql, dashboard
author: <teuNomeAqui>
license: (ISC) MIT
depois: yes e <enter>

npm install


Frontend:

npm start


Backend:
Mas se tu tá criando do zero, segue o fio do tio.

Instalar as dependências manualmente:

Nodemon para facilitar a rodação e o atualizamento do server:

npm i nodemon --save-dev
Express pra facilitar tua vida criando o server

npm i express
Biblioteca pg porque ela sabe conversar com um banco PostgreSQL melhor que tu

npm i pg
Biblioteca cors pra teu front depois poder conversar com o back

npm i cors
Aproveita e já coloca no package.json o script pra rodar o server. Lá no objetinho de scripts deve ter um chamado 'tests'. Arranca ele fora o põe o seguinte no lugar:

"start": "nodemon src/index.js"
O arquivo 'package.json' deve estar mais ou menos como isso aqui:

{
  "name": "dashboardcarros",
  "version": "1.0.0",
  "description": "",
  "main": "src/server.js",
  "scripts": {
    "start": "nodemon src/index.js"
  },
  "keywords": [
    "react",
    "node",
    "postgresql",
    "dashboard"
  ],
  "author": "Rafael",
  "license": "MIT",
  "devDependencies": {
    "nodemon": "^3.1.7"
  },
  "dependencies": {
    "cors": "^2.8.5",
    "express": "^4.21.1",
    "pg": "^8.13.0"
  }
}


Requisitos funcionais:


 Cadastro de Usuários:
O sistema deve permitir o cadastro de usuários com os campos: ID, nome e e-mail.
Deve validar se o e-mail informado é único.

Gerenciamento de Tarefas:
Permitir que usuários criem tarefas com os seguintes dados:
ID da tarefa.
ID do usuário (que cadastrou a tarefa).
Descrição da tarefa.
Nome do setor.
Prioridade (baixa, média, alta).
Data de cadastro (gerada automaticamente).
Status (padrão: "a fazer").

Atualização de Tarefas:
Permitir a atualização do status da tarefa ("a fazer", "fazendo", "pronto").
Permitir a atualização da prioridade da tarefa.

Visualização de Tarefas:
Permitir a visualização de todas as tarefas cadastradas, podendo ser filtradas por:
Nome do setor.
Prioridade.
Status.

Exclusão de Tarefas:
Permitir que usuários excluam tarefas cadastradas por eles.






Requisitos NÃO funcionais:

Portabilidade:
A aplicação deve ser executável em qualquer servidor web que suporte Node.js e MySQL.

Compatibilidade:
A aplicação deve funcionar nos navegadores modernos (Chrome, Firefox, Edge, etc.).

Usabilidade:
Interface simples e intuitiva para facilitar o uso por qualquer usuário, mesmo com conhecimentos básicos de tecnologia.


