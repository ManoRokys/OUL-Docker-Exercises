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
```bash
docker ps -a
docker stop <nome-ou-id>
docker rm <nome-ou-id>
```

**Print da listagem e remoção:**

---

## 4. Dockerfile para aplicação Python (Flask)

**Objetivo:** Criar uma imagem Docker com Flask que retorna mensagem em um endpoint.

**Print do Dockerfile:**

**Print do app.py:**

**Comando para build e execução:**
```bash
docker build -t flask-app .
docker run -p 5000:5000 flask-app
```

**Print do resultado em localhost:**

---

## 5. Volume com MySQL

**Objetivo:** Criar volume para persistência dos dados de um container MySQL.

**Print do docker-compose.yml:**

**Print dos comandos e testes de persistência:**
```bash
docker-compose up -d
docker exec -it mysql bash
mysql -u root -p
```

---

## 6. Multi-stage com aplicação Go (GS PING)

**Objetivo:** Utilizar multi-stage build para gerar imagem otimizada.

**Print do Dockerfile com multi-stage:**

**Comandos executados:**
```bash
docker build -f Dockerfile.multistage -t gs-ping .
docker run -p 8080:8080 gs-ping
```

**Print da aplicação funcionando:**

---

## 7. Rede personalizada entre Node.js e MongoDB

**Objetivo:** Criar uma rede Docker e comunicar containers.

**Print do docker-compose.yml com redes:**

**Comandos utilizados:**
```bash
docker network ls
docker-compose up -d
```

**Print de comunicação entre backend e banco:**

---

## 8. Compose com PostgreSQL e pgAdmin

**Objetivo:** Rodar aplicação com banco PostgreSQL usando Docker Compose.

**Print do docker-compose.yml:**

**Print do pgAdmin acessando PostgreSQL:**

---

## 9. Imagem personalizada com site estático

**Objetivo:** Construir imagem com servidor Nginx/Apache e HTML/CSS estático.

**Print do Dockerfile:**

**Print do site carregado no navegador:**

---

## 10. Rodar container como usuário não-root

**Objetivo:** Criar usuário no Dockerfile e verificar execução com permissão segura.

**Print do Dockerfile:**

**Comando de execução e verificação:**
```bash
docker run -d --name safe-container lucas-python

docker exec safe-container whoami
```

**Print da verificação:**

---

## 11. Análise de imagem com Trivy

**Objetivo:** Usar Trivy para identificar vulnerabilidades em imagem pública.

**Imagem analisada:** `python:3.9`

**Comando:**
```bash
trivy image python:3.9
```

**Print dos resultados com severidade HIGH e CRITICAL:**

**Print ou tabela com sugestões de correção:**

---

## 12. Correção de vulnerabilidades em Dockerfile

**Objetivo:** Otimizar Dockerfile vulnerável, melhorar segurança e tamanho.

**Print do Dockerfile original:**

**Print do Dockerfile corrigido:**

**Comandos usados e tamanho da imagem final:**

---

## Conclusão

A execução desta lista de exercícios proporcionou uma prática completa com as principais funcionalidades do Docker, incluindo imagens personalizadas, volumes, redes, boas práticas de segurança e análise de vulnerabilidades.


