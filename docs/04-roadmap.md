# Roadmap da AI Workstation

Este roadmap cobre a plataforma no computador. UI Android e Projeto Vivo são implementados em `playertwo1/rin`.

## Fase 0 — Fronteira e redução de risco

### 0.1 Contrato v1

- consolidar entidades Project, Session, Event, Checkpoint, Handoff, Approval e Error;
- health, version e capabilities;
- idempotência e cursor de eventos;
- testes de contrato consumíveis pelo RIN;
- ADR de versionamento e transporte.

**Saída:** fake server e fake gateway do RIN passam a mesma suíte.

### 0.2 Stack do nó

- comparar Fastify e Ktor por spike/ADR;
- escolher SQLite ou PostgreSQL para o piloto;
- definir instalação headless Windows/WSL;
- configurar lint, testes, build e CI.

**Saída:** serviço inicia do zero e responde health.

### 0.3 Spikes externos

- validar Git/GitHub;
- iniciar POC Hermes isolado;
- medir providers oficiais, autenticação, termos e limites;
- testar Markdown/Obsidian sem torná-lo obrigatório;
- medir suspensão/retomada e consumo de recursos.

**Saída:** evidência reproduzível e ADRs; nenhum acoplamento sem aprovação.

## Fase 1 — Núcleo persistente

- projetos e raízes autorizadas;
- banco transacional e event log;
- snapshots, checkpoints, decisões e work items;
- erros estruturados;
- exportação/backup atômico;
- recuperação após reinício.

**Gate F1:** estado reconstruído sem chat proprietário e sem perda após reinício.

## Fase 2 — API para RIN

- pairing e dispositivo revogável;
- projetos/detalhe;
- eventos incrementais;
- comandos tipados simulados;
- approvals simuladas;
- rate limit, timeout e auditoria;
- compatibilidade por capabilities.

**Gate F2:** integração real RIN ↔ nó passa cenários online, offline, reconexão e conflito.

## Fase 3 — Git em leitura

- roots allowlisted e caminhos canônicos;
- branch, HEAD, working tree, diff e commits;
- adaptador GitHub em leitura;
- vínculo de evidência;
- sanitização de segredos/conteúdo.

**Gate F3:** três repositórios exibem estado correto no RIN, sem acesso fora das raízes.

## Fase 4 — Sessões simuladas

- `AgentRuntimeProvider`;
- FakeAgent determinístico;
- fila serial por projeto;
- supervisor, timeout, cancelamento e interrupção;
- reconciliação de processos órfãos;
- eventos persistidos antes da transmissão.

**Gate F4:** falha nunca aparece como sucesso e cancelamento deixa auditoria coerente.

## Fase 5 — Primeiro adaptador real

- matriz atual de capabilities dos provedores;
- autenticação oficial e revogável;
- primeiro adaptador escolhido por evidência;
- workspace/branch isolados;
- diff, testes e resultado;
- nenhum push/merge automático.

**Gate F5:** tarefa reversível em repositório de teste termina com evidência.

## Fase 6 — Hermes, se aprovado

- concluir Gate H0 conforme `docs/11-trilha-hermes.md`;
- hospedar por adaptador isolado;
- sessões/workspaces separados;
- limites de CPU/RAM/concorrência;
- falha do Hermes não derruba núcleo;
- substituição por fake/alternativo sem perder estado.

**Gates H1/H2:** tolerância a falha e substituibilidade comprovadas.

## Fase 7 — Memória e AI Shift

- Handoff Manifest versionado;
- snapshot, hashes e prévia;
- congelamento de concorrência;
- confirmação do agente de destino;
- retry sem perda da origem;
- Learning Gate para memória/skills/regras.

## Fase 8 — Knowledge Hub e automações

- exportação Markdown;
- Obsidian opcional;
- n8n/scripts para regras determinísticas;
- tarefas agendadas governadas;
- backup e recuperação testados.

## Fase 9 — Piloto e expansão

- piloto diário com RIN;
- métricas de retomada, falha e recursos;
- acesso remoto zero-trust;
- Modo Jogo com pausa/restauração segura;
- multi-PC e novos módulos apenas após estabilidade.

## Fora deste repositório

Compose, Room, UX do Projeto Vivo, notificações, biometria e navegação pertencem ao RIN.
