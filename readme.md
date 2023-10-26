Criar pasta para aplicação
```
mkdir projetoBackend
```
Acessar pasta
```
cd projetoBackend
```
Criar arquivo para documentar projeto
```
touch readme.md
```
Iniciar o gerenciador de pacotes Node
```
npm init -y
```
Instalar os pacotes
```
npm i express nodemon dotenv
```
Abrir o VSCode
```
code .
```
Criar arquivo .gitignore
```
nano .gitignore
```
Adicionar no arquivo .gitignore o nome da pasta criada após a instalação dos pacotes
```
node_modules
```
Criar estrutura de arquivos e pastas
```
mkdir srcInformar seu nome e e-mail
```
git config --global user.name "FIRST_NAME"
 git config --global user.email "EMAIL@EXAMPLE.COM"

```
Criar arquivos dentro da pasta src
```
touch src/app.js
```
Criar pastas dentro da pasta src
```
mkdir src/config
```
Enviar estrutura do projeto para o gitHub
```
git init
```
Informar seu nome e e-mail
```
git config --global user.name "FIRST_NAME"
 git config --global user.email "EMAIL@EXAMPLE.COM"
```
Verificar arquivos que serão enviados ao  gitHub
```
git status
```
Adicionar todos arquivos ao versionamento
```
git add .
```
Salvar projeto e escrever comentário sobre o processo realizado
```
git commit -m 'estrutura do projeto'
```
De volta ao terminal, executar o comando para definir a branch main
```
git branch -M main
```
Colar a URL do seu repositório copiada
```
git remote add origin COLAR_URL
```
Enviar os arquivos para o gitHub
```
git push -u origin main
```
Com o projeto no servidor remoto podemos remover os arquivos na nossa máquina
```
cd ..
```
Comando para acessar uma pasta anterior
```
rm -rf projetoBackend
```
Clonar o repositório na sua máquina
```
git clone URL_REPOSITORIO
```
Acessar pasta
```
cd NOME_REPOSITORIO
```
Reinstalar os pacotes da aplicação
```
npm i
```
Criar arquivo .env na raiz do projeto
```
nano .env
```
Digitar no arquivo .env
```
PORT = 3008
```
Adicionar arquivo .env no .gitignore
```
nano .gitignore
```
```
.env
```
Abrir o VSCode
```
code .
```
Criar arquivo de exemplo para para as variáveis necessárias da aplicação
```
nano .env.example
```
Adicionar no arquivo .env.example
```
PORT = 
```
Abrir o arquivo app.js e digitar o código
```
const express = require('express');
```
Importar o pacote dotenv, gerenciador de variáveis de ambiente
```
const dotenv = require('dotenv').config();
```
Instanciar o express na variável app
```
const app = express();
```
const app = express();
```
Setar a porta do servidor a partir do arquivo .env
```
app.set('port', process.env.PORT || 3333);
```
Exportar as configurações na variável app
```
module.exports = app;
```
Abrir o arquivo server.js e digitar os códigos
```
const app = require('./app');
```
Importar a porta do servidor
```
const port = app.get('port');
```
Testar API com a função listen
```
app.listen(port, () => {
    console.log(`Running on port ${ port }!`);
});
```
Abrir o arquivo package.json e alterar a chave 'scripts'
```
"start":"nodemon src/server.js"
```
Rodar o comando no termial com gitBash
```
npm run start
```
Atualizar projeto no gitHub
```
git add .
```
Salvar projeto e escrever comentário sobre o processo realizado
```
git commit -m 'configuração do projeto'
```
Enviar os arquivos atualizados para o gitHub
```
git push
```
Atualize a página no gitHub e verifique se os arquivos foram atualizados
```
cd ..
```
Comando para acessar uma pasta anterior
```
rm -rf projetoBackend
```
Conclusão do Passo 2
```
