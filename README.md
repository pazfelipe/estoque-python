# Construindo um gerenciador de estoque com Python, Mongo, Nginx, Nuxt, Varnish, Redis e GKE

## Frustração é o nome disso?
É muito comum acharmos vários cursos abordando tecnologias como `kubernetes`, `Google Cloud Platform` e outras coisas mas já parou para pensar que quando caímos num cenário de verdade, parece que os cursos não adiantaram de nada?

Pois é, se você é um desses devs que zerou os cursos da Udemy e mesmo assim fica perdido igual cachorro em tiroteio, seja bem-vindo ao clube.

## Chega de to-do
A ideia é construirmos uma aplicação do zero em Python, para um gerenciamento de estoque. Com essa aplicação vai ser possível controlar entrada e saída de produtos, simular uma venda no PDV, aplicar desconto, importar XML de NF para dar entrada em produtos.

Além disso vamos emitir relatórios em PDF sobre o estado do nosso estoque, produtos em falta, produtos a vencer, solicitação semi-automática de produtos aos fornecedores e disparos de e-mail.

Aplicação bem completinha né? Pensa na trabalheira que isso vai dar!!!

## Tecnologias
E para ajudar tudo isso, vamos usar algumas tecnologias bem conhecidas e outras nem tanto, como:

- backend: flask (python)
- frontend: nuxt (vuejs)
- load-balancer: nginx
- http-cache: varnish
- database: mongodb / redis

## Onde rodar toda essa parada?
Tudo isso vamos orquestrar via `docker-compose` e ao final, vamos subir tudo para o Google Cloud usando Kubernetes para orquestrar todos os nossos serviços.

Ufa, acho que era isso. Enquanto vou liberando o projeto, vou atualizando essa intro para que você acompanhe passo a passo o progresso do nosso projeto.

## Etapas

- Backend
  - [ ] Instalação python
  - [ ] Definição da estrutura
  - [ ] Conexão com MongoDB
    - [ ] Definir collections
  - [ ] Conexão com Redis
  - [ ] Rotinas
    - [ ] Produtos
      - [ ] Cadastrar produto
      - [ ] Atualizar produto
      - [ ] Retornar produto(s)
      - [ ] Excluir produto
      - [ ] Importar XML
    - [ ] Fornecedores
      - [ ] Cadastrar fornecedor
      - [ ] Atualizar fornecedor
      - [ ] Retornar fornecedor(s)
      - [ ] Excluir fornecedor
    - [ ] Clientes
      - [ ] Cadastrar cliente
      - [ ] Atualizar cliente
      - [ ] Retornar cliente(s)
      - [ ] Excluir cliente
    - [ ] PDV
      - [ ] Gerar pedido de venda
      - [ ] Atualizar estoque
      - [ ] Emitir recibo de venda
      - [ ] Emitir Nota de devolução
  - [ ] Geral
    - [ ] Relatórios em PDF
    - [ ] Gerar pedido com base no estoque
    - [ ] Disparo de e-mail para fornecedores

- Frontend
  - [ ] Gerenciamento de produtos
  - [ ] Gerenciamento de Fornecedores
  - [ ] Gerenciamento de Clientes
  - [ ] Download PDFs
  - [ ] Importar XML

- LoadBalancer
  - [ ] Configuração NGINX

- HTTP-Cache
  - [ ] Configuração Varnish

- Deploy
  - [ ] Criação e configuração GCP `Google Cloud Platform`
  - [ ] Crição Cluster
  - [ ] `Push to GCR - Google Container Registry`
  - [ ] Subindo Kubernetes
  - [ ] Ajustes finais
    