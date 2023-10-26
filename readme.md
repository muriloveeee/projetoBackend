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
# 3º Passo: Clonar o projeto do gitHub, criar a configuração do arquivo de rotas

* Comando clone do git
* Configurar arquivo routes

<hr>

#### Copiar a url do projeto

* Acessar repositório do projeto no gitHub
* Clicar no botão verde '<> Code'
* Clicar no ícone para copiar a URL, conforme a imagem

<img src="../assets/clone_repo.png">

#### Clonar o repositório na sua máquina

* Abrir o gitBash em um local do computador
* Digitar o comando 'git clone' junto com a URL do seu repositório

```
git clone URL_REPOSITORIO
```

<img src="../assets/git_clone.png">

#### Acessar pasta
* Digitar o comando 'cd' e o nome do seu repositório
* cd (change directory): acessar outra pasta
```
cd NOME_REPOSITORIO
```

<img src="../assets/cd_projeto.png">

#### Reinstalar os pacotes da aplicação
```
npm i
```
* Este comando irá recriar a pasta node_modules no projeto

#### Criar pastas dentro da pasta src
```
mkdir src/routes
```

#### Criar arquivo dentro da pasta routes
```
touch src/routes/rotas.js
```
* Responsável pelas rotas que serão acessadas na API

#### Abrir o VSCode
```
code .
```

#### Abrir o arquivo rotas.js e digitar os códigos
```
// Importar o modulo de Router do express
const { Router } = require('express');

// Instanciar o Router na variável router
const router = Router();

router.get('/listar', (request, response) => {
    response.send('Método GET: listar informações');
});
router.post('/cadastrar', (request, response) => {
    response.send('Método POST: salvar informações');
});
router.put('/user/:id', (request, response) => {
    response.send('Método PUT: atualizar informações');
});
router.delete('/user/:id', (request, response) => {
    response.send('Método DELETE: remover informações');
});

module.exports = router;
```

#### Abrir o arquivo app.js e adicionar o código
* Precisamos importar o arquivo de rotas nas configurações da API
```
const router = require('./routes/rotas');
```

* Habilitar as rotas na aplicação
* Esta linha deve inserida depois da criação da variável app
```
app.use('/api', router);
```

#### Atualizar projeto no gitHub
* Adicionar todos arquivos ao versionamento
```
git add .
```

* Salvar projeto e escrever comentário sobre o processo realizado
```
git commit -m 'rotas do projeto'
```

* Enviar os arquivos atualizados para o gitHub
```
git push
```

### Atualize a página no gitHub e verifique se os arquivos foram atualizados 
* Com o projeto no servidor remoto podemos remover os arquivos na nossa máquina
```
cd ..
```
* Comando para acessar uma pasta anterior
* Fechar o VSCode com o projeto aberto

```
rm -rf projetoBackend
```
* rm (remove): comando utilizado para apagar arquivo
* -r (recursive): apaga pastas e subpastas de forma recursiva
* -f (force): não pergunta confirmações
* projetoBackend: nome da pasta que contem os arquivos da aplicação

## Conclusão do Passo 3
#### URL do repositório com:
 * Estrutura do projeto 
 * Arquivo readme de documentação dos passos realizados
 * Configuração 
 * Retorno de teste da API
 * Arquivo de rotas com os métodos [GET, POST, PUT, DELETE]

#### Enviar a URL na tarefa do teams
 * Tarefa 3 - Configuração de rotas