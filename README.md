# Proload - Avaliação de Desenvovimento

## Desafio

Criar um sistema que busca notícias de um feed RSS e usa a API do Zapito para enviá-las por WhatsApp a celulares cadastrados em um painel admin.

## Detalhes

O sistema deve ter um painel com uma tela de CRUD (criar, listar, atualizar e deletar) dos **destinatários** das mensagens, com no mínimo:

- Nome
- Telefone
- Ativo/Inativo

De tempos em tempos o sistema deve, automaticamente, buscar e processar o feed RSS do G1:
https://g1.globo.com/rss/g1/

Então, o sistema deve preparar e enviar mensagens via WhatsApp para os telefones dos **destinatários** usando o endpoint `POST /messages` API do Zapito:
https://zapito.com.br/api/docs

- É necessário criar uma conta em https://zapito.com.br para acessar o token da API;
- Não é necessário contratar um plano, as mensagens podem ser enviadas com a flag `test_mode`;
- A mensagem deve conter ao menos o nome do **destinatário** e o título da notícia.

## Requisitos

- Desenvolver o sistema usando [Laravel](https://laravel.com/);

- Criar o painel usando o [Laravel Backpack](https://backpackforlaravel.com);
  - Não é necessário comprar uma licensa para [instalar](https://backpackforlaravel.com/docs/4.1/installation) o Backpack;
  - É possível criar [CRUDs simples](https://backpackforlaravel.com/docs/4.1/getting-started-basics) com o Backpack com apenas um `Controller`, sem a necessidade de HTML.

- Criar um [Dockerfile](https://docs.docker.com/engine/reference/builder/) com o PHP e as dependências para facilitar o *deploy*;
  - [Docker Compose](https://docs.docker.com/compose/) pode ser utilizado para executar outros serviços, como o servidor HTTP.


## Essa parte não é obrigatória mas é um diferencial
- Subir o código e rodar o sistema em uma [máquina grátis](https://aws.amazon.com/pt/free) da AWS;

- Enviar por e-mail a URL do repositório público contendo o código e o IP do servidor para contato@zapito.com.br com o assunto `TESTE - ZAPITO`.
