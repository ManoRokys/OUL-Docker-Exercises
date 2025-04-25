# OUL-Docker-Exercises


# Documentação dos Exercícios Docker

## Introdução

Este documento apresenta a resolução da lista de exercícios propostos para prática com Docker. Cada atividade está documentada com uma breve descrição, espaço para inserção de prints de código (Dockerfile, scripts, aplicações) e comandos utilizados na execução dos containers.

---

## 1. Rodando um container básico

**Objetivo:** Executar um container com a imagem do Nginx e servir um site estático (landing page do TailwindCSS).

**Landing page do TailwindCSS:** https://github.com/tailwindtoolbox/Landing-Page

**Print do Dockerfile (e da estrutura do projeto):**

Copiei o Repositório do TailwindCSS para a raiz do meu projeto Docker:

![Captura de tela 2025-04-17 103848](https://github.com/user-attachments/assets/760be4b7-1f05-4ebc-83f8-756c3400cc53)

Dockerfile:

![Captura de tela 2025-04-17 105900](https://github.com/user-attachments/assets/573e8f81-321b-4e28-9885-1ce20a6a0bff)


**Comandos executados:**

Fazendo a montagem da imagem:
![Captura de tela 2025-04-17 103823](https://github.com/user-attachments/assets/7658147c-51fd-43b4-860c-cd44784bceb7)
Rodando o container na porta 8080:
![Captura de tela 2025-04-17 103834](https://github.com/user-attachments/assets/8bec355f-0213-47b6-bb8a-65d0eb63bf01)


**Print da landing page no navegador:**

![Captura de tela 2025-04-17 103914](https://github.com/user-attachments/assets/a0f4cdbe-ac2f-4095-b8ec-655abe99ea6b)

---

## 2. Rodando container interativo com Ubuntu

**Objetivo:** Iniciar um container Ubuntu e testar um script bash de logs ou instalação.

**Print do Dockerfile:**

![Captura de tela 2025-04-22 092810](https://github.com/user-attachments/assets/5265b65a-1a38-4e09-8419-b63736dee8ca)

**Script sh utilizado:**

Script que instala algumas bibliotecas:

![Captura de tela 2025-04-22 092801](https://github.com/user-attachments/assets/56b323ae-189c-4fba-9b0b-550144b37ff6)

**Comandos executados:**

![Captura de tela 2025-04-22 090715](https://github.com/user-attachments/assets/a08b8e08-db95-4504-a725-e61e5d82e24d)

**Print do terminal com os pacotes do script instalados:**

![Captura de tela 2025-04-22 092736](https://github.com/user-attachments/assets/4d0fa64d-0364-4461-9662-e6c1827f3fbe)

---

## 3. Listando e removendo containers

**Objetivo:** Listar containers, parar e remover um específico.

**Comandos executados:**

Rodando um container ubuntu genérico:

![Captura de tela 2025-04-22 094920](https://github.com/user-attachments/assets/44a87ef2-76ee-4c8f-b511-29e079ac10b1)

Listagem dos containers ativos: 

![Captura de tela 2025-04-22 094933](https://github.com/user-attachments/assets/bb40327e-4834-4493-8127-749ef80bf802)

Parando o container de teste: 

![Captura de tela 2025-04-22 094956](https://github.com/user-attachments/assets/61414f80-ff5f-4c79-b4bd-9f3f56d1d9c1)

Listagem mostrando os containers parados: 

![Captura de tela 2025-04-22 095053](https://github.com/user-attachments/assets/db986e5e-23b0-4369-9d90-85a9f38b6e2b)

Comando para remover o container de teste:

![Captura de tela 2025-04-22 095118](https://github.com/user-attachments/assets/b4851bf0-36c9-4320-bd3a-fc9cb322cfda)

---

## 4. Dockerfile para aplicação Python (Flask)

**Objetivo:** Criar uma imagem Docker com Flask que retorna mensagem em um endpoint.

**Projeto Python (flask) usado de exemplo:**
https://github.com/docker/awesome-compose/tree/master/flask

**Print do app.py:**

![Captura de tela 2025-04-22 114114](https://github.com/user-attachments/assets/3bf28b72-5d2c-43b5-96ce-90c840604f83)

**Print do Dockerfile:**

![Captura de tela 2025-04-22 114747](https://github.com/user-attachments/assets/72f67201-a5e5-4faa-92d5-6f8404cb845e)


**Comando para build e execução:**

![Captura de tela 2025-04-22 114130](https://github.com/user-attachments/assets/9b318101-9b40-4d90-aa5d-f284d6bcfc23)

![Captura de tela 2025-04-22 114723](https://github.com/user-attachments/assets/409ac390-63eb-4156-a861-5476dab83476)


**Print do resultado em localhost:**

![Captura de tela 2025-04-22 114705](https://github.com/user-attachments/assets/684c88c4-a276-44da-9fe5-2d87a678f783)


---

## 5. Volume com MySQL

**Objetivo:** Criar volume para persistência dos dados de um container MySQL.

**Projeto de base react-express-mysql:**
https://github.com/docker/awesome-compose/tree/master/react-express-mysql

**Print dos comandos e testes de persistência:**

Rodando o docker compose do projeto:

![Captura de tela 2025-04-23 084446](https://github.com/user-attachments/assets/b9c2ee3a-b8e0-49b0-8dc6-2b474ac260c3)

Listagem dos volumes (mostrando que o volume foi criado):

![Captura de tela 2025-04-23 085000](https://github.com/user-attachments/assets/464223eb-3f08-4895-b535-085cfe931ee6)

Aplicação rodando em localhost:3000 :

![Captura de tela 2025-04-23 085145](https://github.com/user-attachments/assets/b039f498-3fc7-41a4-8395-0dae1cacdd93)

Executando o container no modo interativo para a criação do banco de dados:

![Captura de tela 2025-04-23 085903](https://github.com/user-attachments/assets/4d1a3306-0b1d-47b3-8d0d-fe2d5df7bdd9)

Entrando no mysql:

![Captura de tela 2025-04-23 085421](https://github.com/user-attachments/assets/002a10ed-1993-49a9-a111-1241d5138562)

Banco de dados criado para testar a persistência do volume:

![Captura de tela 2025-04-23 085614](https://github.com/user-attachments/assets/b666199a-9058-4a00-b1d7-332f04acd185)

Saindo do modo mysql e da execução:

![Captura de tela 2025-04-23 085636](https://github.com/user-attachments/assets/c7fdee8f-cdf9-40d2-99d2-04233939edaa)

Derrubando os containers: 

![Captura de tela 2025-04-23 085700](https://github.com/user-attachments/assets/01e21c7c-15d9-48e7-905d-1f16d8c1dc2f)

Montando os containers novamente e abrindo o mysql no modo de execução:

![Captura de tela 2025-04-23 085903](https://github.com/user-attachments/assets/d5509ecd-35f3-48f7-9a3a-7f2bf6b672c8)

Mostrando que os dados estão persistêntes no volume:

![Captura de tela 2025-04-23 085849](https://github.com/user-attachments/assets/2d956dcd-8719-4288-988f-8413967762ec)

---

## 6. Multi-stage com aplicação Go (GS PING)

**Objetivo:** Utilizar multi-stage build para gerar imagem otimizada.

**Projeto usado de exemplo desenvolvido em Golang:**
https://github.com/docker/docker-gs-ping

**Print do Dockerfile com multi-stage:**

![Captura de tela 2025-04-23 091200](https://github.com/user-attachments/assets/5bd3f9b3-d3a4-47ca-8aa5-94ff03092419)

**Comandos executados:**

Montando a imagem: 

![Captura de tela 2025-04-23 091148](https://github.com/user-attachments/assets/1b4570e1-ba53-4edc-a20c-6fe112f80afe)

Listagem das images (mostrando que o tamanho da imagem é bem otimizada):

![Captura de tela 2025-04-23 091353](https://github.com/user-attachments/assets/ef955fb8-93d0-4021-ac2a-f756dbc1f88d)

Rodando o container na porta 8080:

![Captura de tela 2025-04-23 091421](https://github.com/user-attachments/assets/081bee45-88e0-4275-bc93-5dc3ab00ec57)

**Print da aplicação funcionando:**

![Captura de tela 2025-04-23 091433](https://github.com/user-attachments/assets/bf0784ef-3674-430d-af0f-a7ba9d3c40c4)


---

## 7. Rede personalizada entre Node.js e MongoDB

**Objetivo:** Criar uma rede Docker e comunicar containers.

**Projeto original de React Express + Mongo:**
https://github.com/docker/awesome-compose/tree/master/react-express-mongodb

**Comandos utilizados:**

Rodando o compose do projeto: 

![Captura de tela 2025-04-23 092733](https://github.com/user-attachments/assets/62471e3f-b289-4093-93ba-14a5c7123574)

Listagem das redes criadas:

![Captura de tela 2025-04-23 092911](https://github.com/user-attachments/assets/824d1374-e234-483e-8901-fb9fdc686a99)

**Print da aplicação rodando na porta 3000:**

![Captura de tela 2025-04-23 093012](https://github.com/user-attachments/assets/996b8ab3-47fb-4522-99b5-306eb23820aa)


---

## 8. Compose com PostgreSQL e pgAdmin

**Objetivo:** Rodar aplicação com banco PostgreSQL usando Docker Compose.

**Projeto usado de exemplo com pgadmin:**
https://github.com/docker/awesome-compose/tree/master/postgresql-pgadmin

**Print do docker-compose.yml:**

![Captura de tela 2025-04-23 093758](https://github.com/user-attachments/assets/72350b48-366f-42b3-8528-be0ce528d023)

**Configurando usuário no postgres e rodando o projeto:**

![Captura de tela 2025-04-23 093804](https://github.com/user-attachments/assets/8033e92e-749e-454d-b144-d7db987996b6)

![Captura de tela 2025-04-23 093906](https://github.com/user-attachments/assets/df704fb0-6344-48f0-b980-7cf82ecc5c2e)

**Print do pgAdmin acessando PostgreSQL:**

![Captura de tela 2025-04-23 094034](https://github.com/user-attachments/assets/6295342e-b077-4d04-88f2-b5cf175d1ac8)

---

## 9. Imagem personalizada com site estático

**Objetivo:** Construir imagem com servidor Nginx/Apache e HTML/CSS estático.

**Projeto usado de exemplo para a Landing page estática:**
https://github.com/creativetimofficial/material-kit

**Print do Dockerfile:**

![Captura de tela 2025-04-23 102505](https://github.com/user-attachments/assets/4e03b29e-3e0f-4c95-ab40-78e678617f2a)

**Comandos utilizados:**

![Captura de tela 2025-04-23 102520](https://github.com/user-attachments/assets/702643c0-1884-4c3d-acc6-59922bc5bce5)

![Captura de tela 2025-04-23 102530](https://github.com/user-attachments/assets/0945738a-8755-4252-b1f0-26ac403fb4a9)

**Print do site carregado no navegador:**

![Captura de tela 2025-04-25 104502](https://github.com/user-attachments/assets/1a2ac6ba-d86f-43f8-8d59-fc43c38251b4)

---

## 10. Rodar container como usuário não-root

**Objetivo:** Criar usuário no Dockerfile e verificar execução com permissão segura.

**Entrypoint do projeto para ele se manter ativo:**

![Captura de tela 2025-04-24 094919](https://github.com/user-attachments/assets/8f7fcf52-4fad-4cfe-b0c7-b781fd5ec584)

**Print do Dockerfile:**

![Captura de tela 2025-04-24 094928](https://github.com/user-attachments/assets/5acf5012-b9c7-40cb-ad81-33ed4f4ebf61)

**Comando de execução e verificação:**

![Captura de tela 2025-04-24 094949](https://github.com/user-attachments/assets/2129e0ff-889d-4d07-a413-09ae5acacd77)

![Captura de tela 2025-04-24 095008](https://github.com/user-attachments/assets/2809c442-aa8f-402e-82e5-71e929f2a9a1)

**Print da verificação:**

![Captura de tela 2025-04-24 095023](https://github.com/user-attachments/assets/3ee07953-acd2-4c69-b44b-b439f9426370)


---

## 11. Análise de imagem com Trivy

**Objetivo:** Usar Trivy para identificar vulnerabilidades em imagem pública.

**Site oficial do Trivy, com instalação e documentações:**
https://trivy.dev/latest/

**Imagem analisada:** `python:3.9`

**Instalação do trivy via linux**

![Captura de tela 2025-04-24 095319](https://github.com/user-attachments/assets/59d39c0d-138c-412e-9c41-2e38d7014de1)

![Captura de tela 2025-04-24 095825](https://github.com/user-attachments/assets/45433e87-18f0-43fd-ae63-e6178dc1237d)

Teste se o trivy foi instalado com sucesso:

![Captura de tela 2025-04-24 095841](https://github.com/user-attachments/assets/75500adf-c3cf-4dbb-83d7-79d28d56c488)

**Comando:**

![Captura de tela 2025-04-24 103548](https://github.com/user-attachments/assets/91a086a4-aa79-4569-8dac-13028874a77c)

**Print dos resultados com severidade HIGH e CRITICAL:**

![Captura de tela 2025-04-24 112810](https://github.com/user-attachments/assets/528fd364-e138-486e-9350-5f7eb916c55b)


**Print com sugestões de correção:**

![Captura de tela 2025-04-24 112751](https://github.com/user-attachments/assets/3a294170-ba5e-4a7c-9f56-7ddc100a5259)

---

## 12. Correção de vulnerabilidades em Dockerfile

**Objetivo:** Otimizar Dockerfile vulnerável, melhorar segurança.

**Print do Dockerfile original:**

![Captura de tela 2025-04-25 105526](https://github.com/user-attachments/assets/f300732b-6437-42a1-975d-55f21ab46eb5)

**Print do Dockerfile corrigido:**

![Captura de tela 2025-04-24 112537](https://github.com/user-attachments/assets/a8bfade0-a6e6-41a8-88c3-ce8c623c7a02)

**Comandos usados:**

![Captura de tela 2025-04-24 112738](https://github.com/user-attachments/assets/5820efbd-81bc-4af0-9dd0-ff67bdf55277)

---

## Conclusão

A execução desta lista de exercícios proporcionou uma prática completa com as principais funcionalidades do Docker, incluindo imagens personalizadas, volumes, redes, boas práticas de segurança e análise de vulnerabilidades.


