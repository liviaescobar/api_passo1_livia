# PASSO 1 

criar pasta
```
mkdir NOME_PASTA
```
acessar pasta
```
cd NOME_PASTA
```
criar arquivos para documentar projeto
```
touch readme.md
```
iniciar o gerenciadro de pacotes Node
```
npm init -y
```
instalar os pacotes
```
npm i express nodemon dotenv
```
abrir o vscode
```
code . 
```
criararquivo .gitignore
```
nano .gitignore
```
Adicionar no arquivo .gitignore o nome da pasta criada após a instalação dos pacotes
* Ctrl + o: Salvar o arquivo
* Enter
* Ctrl + x: Fechar o arquivo
```
node_modules
```
Criar estrutura de arquivos e pastas
```
mkdir src
```
Criar arquivos dentro da pasta src
```
touch src/app.js
```
```
touch src/server.js
```
```
mkdir src/config
```
```
mkdir src/controllers
```
```
mkdir src/routes
```
Inicializar o gerenciador de arquivos
```
git init
```
Informar nome e email 
```
git config --global user.name "FIRST_NAME"
```
```
 git config --global user.email "EMAIL@EXAMPLE.COM"
```
verificar arquivos 
```
git status 
```
adicionar arquivos 
```
git add .
```
salvar e escrever comentário
``` 
git commit -m 'estrutura do projeto'
```
- criar repositório no GitHub
- clicar no icone de copiar o URL do repositório

definir a branch main
```
git branch -M main
```
colar a URL 
```
git remote add origin COLAR_URL
```
enviar para o GitHub
```
git push -u origin main
```

# PASSO 2

Copiar a url do projeto
* Acessar repositório do projeto no gitHub
* Clicar no botão verde '<> Code'
* Clicar no ícone para copiar a URL, conforme a imagem

Abrir o gitBash 
```
git clone URL_REPOSITORIO
```

Acessar a pasta 
```
cd NOME_REPOSITORIO
```

Reinstalar os apcotes da aplicação
```
cd NOME_REPOSITORIO
```

Criar arquivo .env 
```
nano .env
```
Digitar no arquivo .env
```
PORT = 3008
```

* Ctrl + o: Salvar o arquivo
* Enter: Confirmar
* Ctrl + x: Fechar o arquivo

Adicionar arquivo .env no .gitignore
```
nano .gitignore
```
```
.env
```

Abrir VSCode
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


* Importar o pacote express (servidor)
```
const express = require('express');
```
* Importar o pacote dotenv, gerenciador de variáveis de ambiente
```
const dotenv = require('dotenv').config();
```
* Instanciar o express na variável app
```
const app = express();
```
* Setar a porta do servidor a partir do arquivo .env
* O operador condicional '||' significa 'OU', caso não tenha a variável PORT, será utilizado o valor '3333'
```
app.set('port', process.env.PORT || 3333);
```
*  Exportar as configurações na variável app
```
module.exports = app;
```

Abrir o arquivo server.js e digitar os códigos
* Importar o arquivo app
```
const app = require('./app');
```
* Importar a porta do servidor
```
const port = app.get('port');
```
* Testar API com a função listen
* 1º parâmetro: passamos a porta do servidor
* 2º parâmetro: arrow function para retornar um console informando a porta que está rodando o servidor
```
app.listen(port, () => {
    console.log(`Running on port ${ port }!`);
});
```


Abrir o arquivo package.json e alterar a chave 'scripts'
* Substituir o comando 'test' pelo comando 'start' na linha 7
```
"start":"nodemon src/server.js"
```

Rodar o comando no termial com gitBash
```
npm run start
```

Atualizar projeto no gitHub
* Adicionar todos arquivos ao versionamento
```
git add .
```
* Salvar projeto e escrever comentário sobre o processo realizado
```
git commit -m 'configuração do projeto'
```
* Enviar os arquivos atualizados para o gitHub
```
git push
```



