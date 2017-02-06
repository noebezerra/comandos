/*******************
* GitHub
********************/
fonte: http://rogerdudler.github.io/git-guide/index.pt_BR.html

- Iniciando Git
$ git init

- clone
$ git clone <repositorio>

- add
$ git add .
$ git add <nome arquivo>

- commit
$ git commmit -m "first"

- push
$ git push origin master

/*******************
* Typescript2 + Angular 2
*
*********************/

* Requisitos install

NodeJS      - $ curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
              $ sudo apt-get install -y nodejs
Typescript  - $ sudo npm install -g typescript
Typingd     - $ sudo npm install typings --global

* Quick start Loiane clone github

  $ git clone https://github.com/loiane/angular-2-boilerplate.git
  $ npm install
  $ npm start

* Criação de projeto

  $ ng new <meu-proojeto>
  $ cd <meu-projeto>
  $ rm -rf node_modules dist tmp typings
  $ npm install --save-dev angular-cli@webpack
  $ ng init

* Angular 2 - CLI *

  -> install
  $ sudo npm install -g angular-cli
  -> uninstall
  $ sudo npm uninstall -g angular-cli
  $ sudo npm cache clean

  $ ng new <nome_projeto> (--style=sass ou --style=less ou --style=stylus)
  $ cd <nome_projeto>
  $ ng serve

  ou

  $ mkdir <nome_projeto>
  $ cd <nome_projeto>
  $ ng init
  $ ng serve

  - criando componentes, service, directive, pipe, class, interface, enum

  $ ng genrate component <nome_component> ou ng g component <nome_component>
  $ ng genrate service <diretorio>/<nome_component> ou ng g service <diretorio>/<nome_component>
  $ ng g <nome_do_que_deseja> <nome_component>

  - usando pré processador (sass, less, stylus)

  $ ng set defaults.styleExt scss (ou less ou styl)

  - NG LINT, NG TEST, NG E2E

  $ ng lint -> verifica erros ; test -> teste .. e2e

  - BUILD

  $ ng build
  $ ng build --prod

  - Instalando bibliotecas

  $ npm install --save bootstrap@next (pega versão 4)

  /*******************
  * NodeJS
  *
  *********************/

  - Install
  npm i -g express-generator
  express <nomeprojeto> --hogan --css sass

  /*******************
  * Redis
  *
  *********************/

  $ brew install redis
  $ sudo apt install redis-tools
  $ sudo apt install redis-server
  $ redis-cli

  /*******************
  * Knex
  *
  *********************/

  - Install
  $ npm install -g knex

  - criar orm da tabela
  $ knex migrate:make <tabela>
  acesse /migrations/<table> e coloque o shema na func up
     return kenex.raw(` CREATE TABLE <tabela> ... `)
  e em down coloque
    return kenex.shema.dropTable('<tabela>');

  -recuperar orm tabela
  $ knex migrate:latest

  - criar inserts da tabela
  $ knex seed:make 1-<tabela>

  - recuperar inserts do seed
  $ knex seed:run

  /********************
  * Docker
  *
  *********************/

  - Build de uma imagem
  $ docker build -t <nome_da_imagem> <caminho_para_dockerfile>

  - Executar um container
  $ docker run -d -p <porta_host>:<porta_container> --name <nome_container> <nome_imagem>

  - Iniciar uma sessão bash em um container que esteja rodando
  $ docker exec -it <nome_container> bash

  - Ver os logs de um container
  $ docker logs <nome_container>

  - Ver todas as imagens no host
  $ docker images

  - Ver todos os containers
  $ docker ps -a

  - Remover um container
  $ docker rm -f <nome_container>

  - Remover TODOS os containers
  $ docker rm -f $(docker ps -a -q)

  - Remover uma imagem
  $ docker rmi -f <nome_imagem>

  - Remover dangling images
  $ docker rmi $(docker images -q -f dangling=true)

  - Copiar um arquivo do container para o host
  $ docker cp <nome_container>:/caminho/no/container /caminho/no/host
  Exemplo: docker cp app1:/home/ec2-user/log.txt /logs

  /************************
  * Rract JS
  *
  *************************/
  - Install:
  $ sudo npm install -g create-react-app

  - Criando projeto
  $ create-react-app hello-world

  /************************
  * Ionic 2
  *
  *************************/
  - Requisitos:
  Java JDK (java -v , javac -v)
  Android Studio
  $ sudo nano /etc/profile
  ANDROID_HOME=/home/user/Android/Sdk
  PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
  export ANDROID_HOME
  export PATH

  - Install:
  $ npm install -g ionic cordova

  - Criar projeto
  $ ionic start <nome_projeto>
  $ ionic serve

  - Extraindo projeto para uma plataforma
  $ ionic platform add <android/ios>

  - Construindo apk
  $ ionic build android

  - Provider
  $ ionic g provider <service.provider>

  - page
  $ ionic g page <nomepage>
