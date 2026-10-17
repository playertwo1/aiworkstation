# ROADMAP — AI Workstation

Marcos com gate verificável. Detalhe de cada fase (itens e saídas): [`docs/04-roadmap.md`](docs/04-roadmap.md); trilha Hermes: [`docs/11-trilha-hermes.md`](docs/11-trilha-hermes.md). UI Android e Projeto Vivo são implementados em `playertwo1/rin`.

Estados: PLANNED, IN_PROGRESS, BLOCKED, DONE.

| Marco | Resultado verificável | Estado | Gate |
|---|---|---|---|
| Fase 0 | Fronteira e redução de risco: contrato v1, stack do nó, spikes externos | IN_PROGRESS | fake server e fake gateway do RIN passam a mesma suíte; serviço inicia do zero e responde health; spikes com evidência e ADR |
| Fase 1 | Núcleo persistente | PLANNED | Gate F1: estado reconstruído sem chat proprietário e sem perda após reinício |
| Fase 2 | API para RIN | PLANNED | Gate F2: integração real RIN ↔ nó passa online, offline, reconexão e conflito |
| Fase 3 | Git em leitura | PLANNED | Gate F3: três repositórios com estado correto no RIN, sem acesso fora das raízes |
| Fase 4 | Sessões simuladas | PLANNED | Gate F4: falha nunca aparece como sucesso; cancelamento com auditoria coerente |
| Fase 5 | Primeiro adaptador real | PLANNED | Gate F5: tarefa reversível em repositório de teste termina com evidência |
| Fase 6 | Hermes, se aprovado | PLANNED | Gates H0/H1/H2 (`docs/11-trilha-hermes.md`) |
| Fase 7 | Memória e AI Shift | PLANNED | a definir |
| Fase 8 | Knowledge Hub e automações | PLANNED | a definir (backup e recuperação testados) |
| Fase 9 | Piloto e expansão | PLANNED | a definir |

## Marco ativo — Fase 0

| ID | Item | Estado | Evidência exigida |
|---|---|---|---|
| 0.1 | Contrato v1: entidades, health/version/capabilities, idempotência, cursor de eventos, testes de contrato, ADR de versionamento e transporte | PLANNED | fake server e fake gateway do RIN passam a mesma suíte |
| 0.2 | Stack do nó: Fastify × Ktor, SQLite × PostgreSQL, instalação headless, lint/testes/build/CI | PLANNED | serviço inicia do zero e responde health; ADR da stack |
| 0.3 | Spikes externos: Git/GitHub, POC Hermes, providers, Obsidian, suspensão/retomada | PLANNED | evidência reproduzível e ADRs; nenhum acoplamento sem aprovação |

A fundação documental da Fase 0 (fronteiras e divisão de repositórios) está concluída; ver `STATE.md`.
