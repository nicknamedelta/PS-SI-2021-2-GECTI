# GErenciador de Chamados de TI - GECTI

Um sistema estruturado para gerenciar os chamados de TI.

## O que foi utilizado?

- Ruby
- Rails
- Puma
- JWT

## Referências

- [JWT Authentication in Ruby on Rails](https://medium.com/ruby-daily/a-devise-jwt-tutorial-for-authenticating-users-in-ruby-on-rails-ca214898318e)
- [Executando uma instância postgresql e pgadmin no docker](https://renatogroffe.medium.com/postgresql-docker-executando-uma-inst%C3%A2ncia-e-o-pgadmin-4-a-partir-de-containers-ad783e85b1a4)

## Como configurar o Docker?

> Para os passos seguintes faz-se necessário a instalação do Docker;

Faça o download da imagem Docker do pdAdmin: `sudo docker pull dpage/pgadmin4`

Criar a 'ponte' para interligar o container do postgres e do pgAdmin: `sudo docker network create --driver bridge ponte_postgres`

Criar um container do postgres conectado a 'ponte': `sudo docker run --name nome_container --network=ponte_postgres -e "POSTGRES_PASSWORD=senha_container" -p 5432:5432 -d postgres`

Criar um container do pgAdmin conectado a 'ponte': `sudo docker run --name bpgadmin --network=ponte_postgres -p 15432:80 -e "PGADMIN_DEFAULT_EMAIL=email@email.com" -e "PGADMIN_DEFAULT_PASSWORD=bpgadmin" -d dpage/pgadmin4`

Por fim, acesse o endereço http://localhost:15432 para visualizar o pgAdmin web no seu navegador(faz-se necessário preencher o email e a senha declarados no comando acima).

## :runner: Como executar o projeto?

Primeiramente, instale as dependências do projeto executando o seguinte comando no terminal: `bundle install`

Após finalizar, atualize as credenciais do banco no arquivo `config/database.yml` e execute os comandos para criar o banco e executar as migrations: `rake db:create` e `rake db:migrate`

Por fim, para executar o projeto use o comando: `rails server`

## Como utilizar as rotas?

Importe o arquivo `Insomnia.json` no [Insomnia](https://insomnia.rest/) que está na raiz do projeto e utilize as rotas já preenchidas.
