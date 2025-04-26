
# Teste-Tecnico

Sistema de Gestão de Associados e Empresas
Este sistema foi desenvolvido para gerenciar associados e empresas de forma eficiente, utilizando Node.js, MySQL e Express.js.. Ele oferece funcionalidades de cadastro, edição, remoção e listagem de dados, além de integração com Bootstrap para design e Handlebars para renderização dinâmica.

Principais Funcionalidades
Cadastro de Associados:

Permite cadastrar associados com informações como Nome, CPF e Data de Nascimento.

Associados podem ter vínculo com empresas.

Cadastro de Empresas:

Empresas podem ser cadastradas com Nome e CNPJ.

Listagem com Filtros:

Busca associada a filtros como Nome, CPF e Data de Nascimento para associados.

Filtros como Nome e CNPJ para empresas.

Edição de Dados:

Permite a edição de informações de associados e empresas através de formulários.

Remoção de Registros:

Possibilita remover associados e empresas. Ao remover um associado ou empresa, os vínculos relacionados também são eliminados.

Interface Dinâmica:

Utilização de Bootstrap para um design responsivo.

Handlebars para geração dinâmica de páginas.

Tecnologias Utilizadas
Node.js: Framework para construir o backend.

Express.js: Gerenciamento de rotas e middleware.

MySQL: Banco de dados relacional para armazenamento das informações.

Express-Handlebars: Template engine para renderizar páginas web dinamicamente.

Bootstrap: Framework CSS para estilização.

File Upload: Middleware para manipulação de uploads.

Configuração do Ambiente
1. Requisitos
Certifique-se de que você tem as seguintes ferramentas instaladas:

Node.js

MySQL

2. Instalação
Clone este repositório:

bash
git clone <URL_DO_REPOSITORIO>
cd <PASTA_DO_PROJETO>
Instale as dependências do Node.js:

bash
npm install
Configure o banco de dados MySQL:

Crie o banco de dados chamado TesteTecnico.

Execute os scripts SQL para criar as tabelas associados, empresas e associadosempresas.

Configure as credenciais do banco de dados no arquivo do código:

javascript
const conexao = mysql.createConnection({
    host: 'localhost',
    user: 'root',
    password: '',
    database: 'TesteTecnico'
});
3. Execução
Inicie o servidor com o comando:

bash
node app.js
Acesse o sistema no navegador:

URL: http://localhost:8080

Estrutura de Rotas
Associados
GET /associados: Listagem de associados com filtros.

POST /associados: Cadastro de novos associados.

POST /editarassociados/:id_associado: Edição de associados.

GET /removerassociado/:id_associado: Remoção de um associado.

Empresas
GET /empresas: Listagem de empresas com filtros.

POST /empresas: Cadastro de novas empresas.

POST /editar_empresa/:id_empresa: Edição de empresas.

GET /remover_empresa/:id_empresa: Remoção de uma empresa.

Exemplo de Utilização
Cadastro de Associado
Navegue até http://localhost:8080/associados.

Preencha as informações no formulário e clique em Cadastrar.

Cadastro de Empresa
Navegue até http://localhost:8080/empresas.
