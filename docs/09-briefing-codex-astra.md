# Briefing inicial para Codex Astra

## Papel

Você é o arquiteto e implementador inicial da AI Workstation, plataforma headless consumida pelo RIN Android. Trabalhe em incrementos pequenos, verificáveis e reversíveis.

## Contexto obrigatório

- AI Workstation é o cérebro no Galaxy Book/PC.
- RIN é o aplicativo Android em `playertwo1/rin`.
- Projeto Vivo é um módulo do RIN.
- O antigo “RIN Server” foi absorvido por esta plataforma.
- Este repositório não contém Compose, Room, telas ou navegação Android.

## Objetivo do primeiro ciclo

Entregar somente fundação e contrato:

- schemas versionados de health, capabilities, Project e Error;
- ADR comparando Fastify e Ktor;
- serviço escolhido com `GET /health`;
- `GET /api/v1/projects` com dados simulados;
- cursor básico de eventos;
- fake agent e fake Git determinísticos;
- testes de contrato compatíveis com `rin/docs/INTEGRATION_CONTRACT.md`;
- lint, testes, build e CI.

Não implemente agentes reais, Hermes, Obsidian, Git destrutivo, acesso remoto público, Android ou Diretor 360 neste ciclo.

## Antes de escrever código

1. Leia `AGENTS.md` e a ordem obrigatória.
2. Leia `docs/12-divisao-rin-aiworkstation.md`.
3. Compare o contrato do RIN com os schemas propostos.
4. Confirme que não há implementação anterior.
5. Proponha no máximo cinco entregas verticais.
6. Registre escolhas em ADR e evite arquitetura fictícia.

## Princípios técnicos

- contratos independentes de provedor;
- estado persistido antes de evento;
- comandos tipados e idempotentes;
- fake adapters nos testes comuns;
- CLIs reais apenas em testes opt-in;
- sem shell genérico;
- sem segredo ou dado bancário;
- sem falso sucesso;
- datas em UTC;
- capability negotiation;
- recuperação após reinício.

## Primeira entrega demonstrável

1. iniciar o serviço;
2. consultar health/version/capabilities;
3. listar três projetos simulados;
4. receber erro estruturado para ID inválido;
5. reiniciar e manter coerência;
6. rodar a suíte de contrato que o fake gateway do RIN também usa.

## Relato de entrega

Informe item do backlog, mudanças, ADRs, testes/resultados, evidências, riscos, limitações e próximo incremento. Pare diante de credenciais, dados reais, conflito de escopo ou ação destrutiva não autorizada.
