AluraDocs
O AluraDocs é um projeto prático desenvolvido durante a formação da Alura, focado na implementação de comunicação em tempo real utilizando WebSockets. A aplicação permite a criação e edição colaborativa de documentos, garantindo que as alterações feitas por um utilizador sejam refletidas instantaneamente para todos os outros conectados ao mesmo documento.

🚀 Funcionalidades
Registo e Autenticação: Sistema completo de criação de contas e login.

Segurança de Dados:

Armazenamento de palavras-passe utilizando hashing e sal (salt) para maior proteção.

Autenticação de sessões através de JSON Web Tokens (JWT).

Edição Colaborativa: Edição de texto em tempo real com sincronização automática entre clientes via Socket.io.

Gestão de Documentos: Interface para listar, adicionar e eliminar documentos na base de dados.

Presença em Tempo Real: Visualização dos utilizadores que estão atualmente conectados e a visualizar cada documento.

🛠 Tecnologias Utilizadas
Node.js: Ambiente de execução do servidor.

Express: Framework web para gerir rotas e ficheiros estáticos.

Socket.io: Motor para a comunicação bidirecional em tempo real.

MongoDB: Base de dados NoSQL utilizada para persistir documentos e utilizadores.

jsonwebtoken: Implementação de tokens para autorização de utilizadores.

dotenv: Gestão de variáveis de ambiente sensíveis.

📦 Estrutura do Projeto
O projeto segue uma arquitetura separada entre a lógica do servidor e os ficheiros do cliente:

public/: Contém o front-end (HTML, CSS e Javascript) organizado por módulos (login, cadastro, documento).

servidor/: Contém a lógica de back-end, incluindo a conexão à base de dados, middlewares de autorização e o registo de eventos do Socket.io.

🔧 Como Executar
Instalar as dependências:

Bash

npm install
Configurar o Ambiente: Crie um ficheiro .env na raiz do projeto com as seguintes chaves:

SEGREDO_JWT: Uma string aleatória para assinar os tokens JWT.

porta: A porta onde o servidor irá correr (ex: 3000).

Iniciar o servidor em modo de desenvolvimento:

Bash

npm run dev
Este comando utiliza o nodemon para reiniciar o servidor automaticamente em cada alteração no ficheiro servidor/socket-back.js.

📄 Licença
Este projeto está licenciado sob a licença ISC.
