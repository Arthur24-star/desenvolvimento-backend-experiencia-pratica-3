# Experiência Prática 3 — Desenvolvimento Back-end

## Sobre o projeto

Este projeto foi desenvolvido durante a **Experiência Prática 3** da disciplina de **Desenvolvimento Back-end**.

A atividade teve como objetivo analisar, na prática, a comunicação entre cliente e servidor em uma aplicação web, utilizando o **YouTube Web** como objeto de estudo e as ferramentas de desenvolvedor do navegador (**DevTools**).

Durante a investigação, foram observadas requisições HTTP realizadas pelo navegador, seus métodos, endpoints, códigos de status e respostas retornadas pelos servidores.

---

## Objetivos

- Compreender a arquitetura cliente-servidor;
- Identificar requisições HTTP realizadas por uma aplicação web;
- Analisar métodos HTTP e códigos de status;
- Observar respostas e estruturas de dados;
- Compreender o papel das APIs na comunicação entre front-end e back-end;
- Representar o fluxo de comunicação por meio de um fluxograma.

---

## Aplicação analisada

A aplicação escolhida para a investigação foi o **YouTube Web**.

A plataforma foi selecionada por apresentar diversas interações que geram comunicação entre o navegador e os servidores, como pesquisas, carregamento de vídeos, reprodução de conteúdos e registro de eventos.

---

## Requisições analisadas

Durante a investigação foram identificadas cinco requisições:

| Endpoint | Método | Status | Função |
|---|---|---:|---|
| `/complete/search` | GET | 200 | Realizar pesquisas e retornar resultados |
| `/youtubei/v1/get_watch` | POST | 200 | Carregar dados necessários para exibir o vídeo |
| `/api/stats/watchtime` | POST | 204 | Registrar informações relacionadas ao tempo de reprodução |
| `/videoplayback` | POST | 200 | Solicitar dados necessários para a reprodução |
| `/youtubei/v1/log_event?alt=json` | POST | 200 | Registrar eventos e interações do usuário |

---

## Análise técnica

Uma das principais requisições analisadas foi:

**Endpoint:** `/complete/search`  
**Método:** `GET`  
**Status:** `200 OK`

O método **GET** foi utilizado porque a operação possui finalidade de consulta, buscando informações relacionadas ao termo pesquisado sem alterar os dados do servidor.

O código **200 OK** indica que a requisição foi processada com sucesso e que os dados foram retornados corretamente ao cliente.

Também foi analisada uma requisição utilizada durante o carregamento de um vídeo:

**Endpoint:** `/youtubei/v1/get_watch`  
**Método:** `POST`  
**Status:** `200 OK`

Essa chamada participa do processo de obtenção dos dados necessários para que o navegador possa apresentar o conteúdo selecionado.

---

## Arquitetura cliente-servidor

O fluxo de comunicação analisado pode ser representado da seguinte forma:

```text
Usuário
   ↓
Navegador / Front-end
   ↓
Requisição HTTP
   ↓
Servidor / API
   ↓
Processamento
   ↓
Resposta HTTP
   ↓
Navegador / Front-end
   ↓
Atualização da interface

Essa separação de responsabilidades permite que o cliente seja responsável pela interação e apresentação das informações, enquanto o servidor realiza o processamento das solicitações e disponibiliza os dados necessários.

## Resultado da experiência

Principais conhecimentos adquiridos

Durante a experiência prática foram desenvolvidos conhecimentos relacionados a:

Arquitetura cliente-servidor;
APIs;
Requisições HTTP;
Métodos HTTP;
Status Codes;
Endpoints;
JSON;
DevTools;
Aba Network;
Comunicação entre front-end e back-end;
Fluxo de requisição e resposta.

---

 

A experiência permitiu observar, na prática, como uma aplicação web realiza diversas comunicações com seus servidores durante ações realizadas pelo usuário.

A investigação também demonstrou a importância de compreender a estrutura das APIs, os métodos HTTP, os códigos de status e o fluxo de dados entre cliente e servidor para o desenvolvimento, diagnóstico e manutenção de aplicações back-end modernas.

Documentação

O relatório completo desenvolvido durante a experiência prática está disponível neste repositório:


## Autor

Arthur Fernando Rodrigues Fonseca

Estudante de Análise e Desenvolvimento de Sistemas.

Projeto desenvolvido como parte da disciplina de Desenvolvimento Back-end.
