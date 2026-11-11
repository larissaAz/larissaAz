<h1 align="center">Oi, eu sou a Larissa Azevedo 👋</h1>

<p align="center">
  <b>Desenvolvedora Full Stack</b> · TypeScript · React · Node.js · Python
</p>

<p align="center">
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white" alt="TypeScript"></a>
  <a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.js-22-339933?logo=node.js&logoColor=white" alt="Node.js"></a>
  <a href="https://react.dev/"><img src="https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black" alt="React"></a>
  <a href="https://vitejs.dev/"><img src="https://img.shields.io/badge/Vite-5-646CFF?logo=vite&logoColor=white" alt="Vite"></a>
  <a href="https://expressjs.com/"><img src="https://img.shields.io/badge/Express-4-000000?logo=express&logoColor=white" alt="Express"></a>
  <a href="https://prisma.io/"><img src="https://img.shields.io/badge/Prisma_ORM-7-2D3748?logo=prisma&logoColor=white" alt="Prisma"></a>
  <a href="https://www.postgresql.org/"><img src="https://img.shields.io/badge/PostgreSQL-17-336791?logo=postgresql&logoColor=white" alt="PostgreSQL"></a>
  <a href="https://socket.io/"><img src="https://img.shields.io/badge/Socket.io-4.8-010101?logo=socket.io&logoColor=white" alt="Socket.io"></a>
  <a href="https://tailwindcss.com/"><img src="https://img.shields.io/badge/Tailwind_CSS-3-06B6D4?logo=tailwindcss&logoColor=white" alt="Tailwind"></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" alt="Python"></a>
  <a href="https://fastapi.tiangolo.com/"><img src="https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white" alt="FastAPI"></a>
  <a href="https://www.docker.com/"><img src="https://img.shields.io/badge/Docker_Compose-2496ED?logo=docker&logoColor=white" alt="Docker"></a>
  <a href="https://playwright.dev/"><img src="https://img.shields.io/badge/Playwright-E2E-2EAD33?logo=playwright&logoColor=white" alt="Playwright"></a>
</p>

---

## 💼 No que estou trabalhando hoje

Atualmente atuo no desenvolvimento de um **sistema de gestão empresarial (ERP) full stack, multi-tenant**, em produção, com entregas contínuas — versionamento semântico, changelog automatizado e deploy blue-green. Atendo as áreas **fiscal, operacional e administrativa** da empresa.

Meus projetos pessoais e de estudo focam em **APIs e automação em Python** — hoje tenho quatro repositórios públicos em Python (FastAPI, SQLAlchemy e sockets).

### Domínios que atendo

- **Fiscal e documentos fiscais** — importação de XML, parser de arquivos SPED, geração de documentos em PDF (DANFE e relatórios).
- **Operacional** — compras com alertas, catálogo de produtos, controle de escala de pessoal e ferramentas internas.
- **Atendimento interno** — helpdesk com prioridades, anexos e notificações em tempo real por WebSocket.
- **Plataforma** — multi-tenancy, RBAC por ação, trilha de auditoria e monitoramento de status em tempo real.

---

## 📊 Contribuições no projeto atual

> Histórico de commits meus nos últimos ~10 meses de projeto. A contagem por camada usa caminhos de arquivo: um commit pode aparecer em mais de uma linha, e entregas que só tocam arquivos fora dessas pastas não entram nas linhas de camada. A soma por tipo fecha em 460.

| Métrica | Valor |
|---------|-------|
| Commits autorais | **594** (460 desconsiderando merges) |
| Composição | features **224** · correções **97** · docs **38** · refactors **21** · infra/estilo/testes **45** · fora do padrão **35** |
| Camadas tocadas | frontend **241** · backend/API **153** · docs **35** · testes **3** · CI e config **11** |
| Commits full stack | **32** entregas mudam frontend e backend no mesmo commit |
| Volume de código | **+95k / −23k** linhas |
| Releases do produto no período | **343** |

---

## 🧠 Desafios que resolvi

- **Upload de arquivo grande derrubando o processo** → troquei o buffer em memória por **streaming em disco** e reescrevi o parser para aceitar **4 layouts diferentes**, com fallback de período pelo nome do arquivo e erro individual por arquivo: um XML inválido não derruba mais a importação inteira.
- **Tela travada ao listar milhares de registros fiscais** → paginação local + memoização da filtragem e do agrupamento com `useMemo`, separando a paginação de arquivos da paginação de itens.
- **Importação em massa sobrecarregando banco e WebSocket** → inserção em **lotes de 50 registros**, *throttle* na emissão do progresso e índices novos por empresa, código e status.
- **Módulo de compras lento e com regra duplicada** → refatorei para o padrão repository com consultas otimizadas, índices dedicados e correção de lógicas repetidas em várias telas.

---

## 🔧 Stack

| Camada | Tecnologias |
|--------|-------------|
| Frontend | React 18 · TypeScript · Vite · Tailwind CSS · Chart.js · TanStack Table |
| Backend | Node.js 22 · Express · arquitetura em camadas (controller → service → repository) · Zod |
| Banco | PostgreSQL 17 · Prisma ORM · índices e tipagem ponta a ponta |
| Tempo real | Socket.io — notificações, progresso de jobs e status do sistema |
| Python | FastAPI · SQLAlchemy · SQLite · sockets + threading |
| Infra | Docker Compose (dev/prod) · CI/CD · deploy blue-green |
| Qualidade | Playwright (E2E) · suítes de regra de negócio · specs funcionais versionadas |

---

## 🌱 Como eu trabalho

- **Feature de ponta a ponta** — schema, endpoint, regra de negócio, validação, interface e teste na mesma entrega.
- **Refatorar em vez de contornar** — prefiro reescrever o fluxo a acumular gambiarra.
- **Documentação como parte da entrega** — spec funcional, manual de ajuda e changelog caminham com o código.
- **Conventional Commits com escopo de módulo** — mantém changelog e rastreabilidade automáticos.
- **Fluxo com agentes de IA** — assistentes de IA no planejamento, escrita e revisão, com regras e skills do projeto versionadas.

---

## 📦 Projetos públicos

| Projeto | Stack | O que é |
|---------|-------|---------|
| [Cadastro de usuário API](https://github.com/larissaAz/Cadastro_de_usuario_Api) | FastAPI · SQLAlchemy · SQLite | API REST de cadastro com autenticação por token e CORS |
| [Chat em grupo](https://github.com/larissaAz/chat_em_grupo) | Python · sockets · threading | Servidor e cliente de chat com salas e broadcast |
| [Projeto Mercearia](https://github.com/larissaAz/Projeto_Mercearia_2024) | Python puro | Sistema de estoque/vendas em arquitetura MVC com persistência em arquivo |
| [Sistema de login](https://github.com/larissaAz/Projeto_Sistemalogin) | Python puro | Cadastro e autenticação de usuário em camadas (Model · View · Controller) |

---

## 📫 Onde me encontrar

- GitHub: [@larissaAz](https://github.com/larissaAz)
- LinkedIn: [linkedin.com/in/azevedoalarissa](https://www.linkedin.com/in/azevedoalarissa)
- E-mail: azevedoa.larissa@gmail.com

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=larissaAz&style=flat-square&color=blue" alt="Profile views">
</p>
