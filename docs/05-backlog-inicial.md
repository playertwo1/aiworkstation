# Backlog inicial da AI Workstation

## Épico AW-A — Contratos

- AW-001 — Schema versionado de health/capabilities.
- AW-002 — Project, Checkpoint, Decision e WorkItem.
- AW-003 — Session, Event, Handoff e Approval.
- AW-004 — Error envelope e códigos estáveis.
- AW-005 — Idempotência e cursor.
- AW-006 — Testes de contrato compartilháveis com RIN.

## Épico AW-B — Serviço e persistência

- AW-010 — ADR Fastify versus Ktor.
- AW-011 — Scaffold do serviço headless.
- AW-012 — Banco e migrações.
- AW-013 — Event log append-only.
- AW-014 — Recuperação após reinício.
- AW-015 — Exportação e backup atômicos.

## Épico AW-C — API e segurança

- AW-020 — `GET /health` com version/capabilities.
- AW-021 — Projetos e detalhe.
- AW-022 — Eventos por cursor.
- AW-023 — Comandos tipados/idempotentes.
- AW-024 — Pairing e revogação de dispositivo.
- AW-025 — Rate limit, timeout e auditoria.
- AW-026 — Approval com hash e expiração.

## Épico AW-D — Git

- AW-030 — Raízes autorizadas.
- AW-031 — Status, branch e HEAD.
- AW-032 — Diff/commits e arquivos não rastreados.
- AW-033 — GitHub em leitura.
- AW-034 — Sanitização e evidências.
- AW-035 — FakeGitRepository.

## Épico AW-E — Sessões

- AW-040 — AgentRuntimeProvider.
- AW-041 — FakeAgent determinístico.
- AW-042 — Fila serial por projeto.
- AW-043 — Supervisor e cancelamento.
- AW-044 — Reconciliação de órfãos.
- AW-045 — Estados/erros sem falso sucesso.

## Épico AW-F — Integrações posteriores

- AW-050 — Primeiro adaptador real.
- AW-051 — POC e adaptador Hermes.
- AW-052 — KnowledgeProvider/Markdown.
- AW-053 — Obsidian opcional.
- AW-054 — Handoff Manifest e AI Shift.
- AW-055 — Learning Gate.
- AW-056 — Monitor de recursos e Modo Jogo.

## Primeira sequência para Codex Astra

1. AW-001
2. AW-002
3. AW-004
4. AW-005
5. AW-006
6. AW-010
7. AW-011
8. AW-020
9. AW-021
10. AW-022

O código Android pertence a `playertwo1/rin`.
