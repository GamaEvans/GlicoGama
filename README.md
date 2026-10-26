# Meu Caderno Diabetes — Parte 1

Implementado: cadastro/login/logout (sessões em PostgreSQL, bcrypt, rate limit, CSRF via SameSite + cabeçalho, CSP); CRUD de glicemias isolado por usuário; filtro por período; estatísticas normalizadas em mg/dL; gráfico Chart.js; histórico responsivo; visual de caderno.

## Rodar
1. `npm install`
2. `cp .env.example .env` e preencha `DATABASE_URL` e `SESSION_SECRET`
3. `npm run db:init`
4. `npm start` → http://localhost:3000

## API
`POST /api/auth/{register,login,logout}`, `GET /api/auth/me`, `GET/POST /api/glucose`, `PATCH/DELETE /api/glucose/:id` (filtros: from, to, moment, order).

## Ainda não implementado
Recuperação de senha, diário alimentar e integração nutricional, calculadora educativa (deve nascer desabilitada), assistente de IA, relatórios PDF/CSV, lembretes, exclusão/exportação de conta, perfil, testes automatizados, política de privacidade.
