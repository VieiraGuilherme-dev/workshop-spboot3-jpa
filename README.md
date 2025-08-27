#  Web Services com Spring Boot, JPA e Hibernate

Este projeto é uma **API RESTful** desenvolvida em **Java 17** com **Spring Boot**, utilizando **JPA/Hibernate** para persistência de dados e banco **PostgreSQL** (com H2 para testes).  
O sistema segue uma arquitetura em camadas (Controller → Service → Repository → Model), implementa CRUD completo, relacionamentos entre entidades e tratamento personalizado de exceções.

---

## Funcionalidades

- CRUD completo para **usuários, produtos, categorias, pedidos e pagamentos**.
- Relacionamentos **One-to-One**, **One-to-Many** e **Many-to-Many**.
- Mapeamento de chaves compostas (entidade `OrderItem`).
- Perfil **test** com banco **H2** para desenvolvimento rápido.
- Perfil **dev** integrado ao **PostgreSQL** local.
- Perfil **prod** para deploy no **Heroku**.
- Tratamento de exceções customizado.
- Povoamento inicial do banco de dados para testes.
- Implementação de status de pedido via **enum**.

---


##  Tecnologias Utilizadas

![Java](https://img.shields.io/badge/Java%2017-ED8B00?style=for-the-badge&logo=java&logoColor=white)  
• Linguagem principal do projeto.

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)  
• Framework Java para criação rápida de APIs RESTful e injeção de dependência.

![JPA](https://img.shields.io/badge/JPA%20%2F%20Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white)  
• API e framework ORM para mapeamento objeto-relacional.

![H2 Database](https://img.shields.io/badge/H2%20Database-006699?style=for-the-badge&logo=h2&logoColor=white)  
• Banco em memória para testes e desenvolvimento rápido.

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)  
• Banco de dados relacional utilizado no ambiente de desenvolvimento e produção.

![Heroku](https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white)  
• Plataforma utilizada para deploy da aplicação.

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)  
• Ferramenta para testar os endpoints da API.

---

## Endpoints Principais

- `GET /users` → Lista todos os usuários.  
- `GET /users/{id}` → Busca usuário por ID.  
- `POST /users` → Cadastra novo usuário.  
- `PUT /users/{id}` → Atualiza dados do usuário.  
- `DELETE /users/{id}` → Remove usuário.  

Também existem endpoints para **Orders**, **Products**, **Categories** e **Payments**.

---

##  Perfis de Execução

**🔹 Test (H2)**  
Banco em memória para desenvolvimento rápido e testes.  
Configuração: `application-test.properties`

**🔹 Dev (PostgreSQL Local)**  
Banco local para desenvolvimento real.  
Configuração: `application-dev.properties`

**🔹 Prod (Heroku + PostgreSQL)**  
Banco remoto para deploy em produção.  
Configuração: `application-prod.properties`

---

## ▶️ Como Executar o Projeto

### Pré-requisitos
- **Java 17+**
- **Maven**
- **PostgreSQL** (para o perfil `dev`)

### Passos
```bash
# Clonar repositório
git clone https://github.com/seu-usuario/seu-repositorio.git

# Entrar no diretório
cd seu-repositorio

# Executar com perfil de teste (H2)
mvn spring-boot:run -Dspring-boot.run.profiles=test

# Executar com perfil de desenvolvimento (PostgreSQL)
mvn spring-boot:run -Dspring-boot.run.profiles=dev

✅ Entregáveis
✅ CRUD completo de todas as entidades.

✅ Relacionamentos complexos (One-to-One, One-to-Many, Many-to-Many).

✅ Perfis separados para Test, Dev e Prod.

✅ Tratamento global de exceções.

✅ Script de inicialização do banco.

✅ Deploy funcional no Heroku.

CONTATO - gv524003@gmail.com
