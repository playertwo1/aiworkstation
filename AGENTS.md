# Instruções para agentes

## Missão atual

Construir a **AI Workstation**, plataforma headless consumida pelo aplicativo Android RIN. O Projeto Vivo é um módulo do RIN; não implementar UI Android neste repositório.

## Ordem de leitura obrigatória

1. `README.md` e `STATE.md` (onde paramos e próxima ação)
2. `docs/12-divisao-rin-aiworkstation.md`
3. `docs/01-visao-produto.md`
4. `docs/02-escopo-mvp.md`
5. `docs/03-arquitetura-inicial.md`
6. `ROADMAP.md` (marcos) e `docs/04-roadmap.md` (detalhe)
7. `docs/06-decisoes-e-hipoteses.md`
8. `docs/07-seguranca.md`
9. contrato correspondente em `playertwo1/rin/docs/INTEGRATION_CONTRACT.md`

## Responsabilidade deste repositório

- API versionada e pareamento.
- Estado canônico, eventos e auditoria.
- Git local e adaptador GitHub.
- Supervisor, filas, comandos e políticas.
- Adaptadores de Codex, Claude, Antigravity e possível Hermes.
- Knowledge Hub/Obsidian e automações, quando aprovados.
- Monitoramento do nó headless.

## Fora deste repositório

- Compose, Room, WorkManager, telas e navegação.
- Cache offline e preferências móveis.
- Implementação do módulo visual Projeto Vivo.
- Notificações e biometria Android.

Esses itens pertencem ao `playertwo1/rin`.

## Princípios

- Local-first e headless quando simples e seguro.
- Contrato público independente de provedores.
- Git/GitHub como verdade do código.
- Estado persistido antes de transmissão.
- Aprovação humana para ações críticas.
- Fato, hipótese, decisão e questão aberta são distintos.
- Fake adapters em testes; CLIs reais somente em testes opt-in.
- Sem shell genérico, segredos no Git ou sucesso sem evidência.

## Disciplina de mudança

- Identificar item do roadmap/backlog.
- Registrar arquitetura em `docs/adr/`.
- Atualizar `STATE.md` e `CHANGELOG.md` (`## X.Y.Z — AAAA-MM-DD`).
- Alterações incompatíveis de API exigem versão nova e coordenação com RIN.
- Validar autenticação, limites, estabilidade e termos atuais de cada integração.
- Parar diante de dados reais sensíveis, credenciais ou ação destrutiva não autorizada.

## Comandos

- Rodar e verificar: a definir. Ainda não há código; a stack sai do spike da Fase 0.2.

## Git

- `CLAUDE.md` só importa este arquivo (`@AGENTS.md`).
- Nunca force push nem reescreva histórico.

## Definition of Done

Critérios aceitos, testes passando, documentação atualizada, erros considerados, revisão de segurança concluída, nenhum segredo no diff, evidência persistida e próximo passo registrado.
