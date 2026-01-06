# 📋 Kanban Board - Sprint 1: Fundação & Identidade

> **Legenda**:
> - 📝 `To Do`: Aguardando início.
> - 🚧 `In Progress`: Sendo trabalhado agora.
> - 🔍 `Code Review`: Pull Request aberto.
> - ✅ `Done`: Mergeado na develop/main.

---

## 📝 To Do



### PB-025: API Gateway Config
- **Estimativa**: 1 dia
- **Detalhes**: Roteamento básico para o user-service.

---

## 🚧 In Progress

*(Nenhum item em progresso no momento)*


*(Nenhum item em progresso no momento)*

---

## 🔍 Code Review

*(Nenhum item em review no momento)*

---

## ✅ Done

### PB-001: Setup inicial `user-service`
- **Concluído em**: 06/01/2026
- **Branch**: `feat/PB-001-setup-user-service` (Merged)
- **O que foi feito**:
  - Estrutura do projeto criada.
  - `pom.xml` configurado (JPA, Security, Lombok, JWT).
  - `application.yaml` configurado (Conexão DB PostgreSQL).
  - Pacote `com.lucasgrf.userservice` criado.

### PB-002: Cadastro de usuários (`/register`)
- **Concluído em**: 06/01/2026
- **Branch**: `feat/PB-002-user-register` (Merged)
- **O que foi feito**:
  - Endpoint `POST /api/v1/auth/register` implementado.
  - Validação de campos obrigatórios.
  - Senha encriptada com BCrypt.
  - Retorna 201 Created com UUID do usuário.

### PB-003: Login e JWT (`/login`)
- **Concluído em**: 06/01/2026
- **Branch**: `feat/PB-003-auth-login` (Merged)
- **O que foi feito**:
  - Endpoint `POST /api/v1/auth/login` implementado.
  - Validação de credenciais (email/senha).
  - Geração de JWT com claims (`sub`, `roles`).
  - Token válido por 1 hora.

### PB-004: Configuração de Segurança (Spring Security)
- **Concluído em**: 06/01/2026
- **Branch**: `feat/PB-004-security-config` (Merged)
- **O que foi feito**:
  - `JwtAuthenticationFilter` implementado.
  - Validação de token em rotas protegidas.
  - Sessão configurada como STATELESS.
  - Endpoint `/me` para verificação de autenticação.

### PB-026: Subir ambiente local (Docker Compose)
- **Concluído em**: 05/01/2026
- **Branch**: `fix/PB-026-mongo-optimization` (Merged)
- **O que foi feito**:
  - Criado `docker-compose.yml` com Postgres (5432), Mongo (27017) e RabbitMQ (5672/15672).
  - Otimização de logs (max-file 3).
  - Otimização de memória (limits) e cache do Mongo (wiredTiger).
- **Validação**:
  - `docker ps` mostrou 3 containers UP.
  - Portas acessíveis localmente.
