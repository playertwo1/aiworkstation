# ADR 0001 — Começar pelo MVP local-first

- Status: aceito
- Data: 2026-09-11

## Contexto

A visão completa inclui Android, nó headless, GitHub, Obsidian, Hermes e vários provedores. Implementar tudo simultaneamente impediria validar qual parte realmente resolve o problema.

## Decisão

Começar por cadastro de projetos, checkpoints, histórico e “Onde parei?” determinístico no Android. GitHub entra depois em modo leitura; execução e agentes ficam para fases posteriores.

## Consequências

- Entrega de valor mais cedo.
- Menor risco técnico e de segurança.
- Algumas informações serão manuais no começo.
- Contratos futuros não devem gerar infraestrutura prematura.

