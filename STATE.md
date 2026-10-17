# STATE — ponto de retomada

Qualquer agente deve conseguir retomar só com este arquivo + a seção ativa do `ROADMAP.md`, sem a conversa anterior. Curto: o que não for estado atual sai daqui. Substitui `PROJECT_STATE.md` (arquivado em `docs/archive/`).

**Atualizado:** 2026-10-17 (conteúdo de estado de 2026-09-12; últimos commits de 2026-09-20) · **Marco ativo:** Fase 0 — fronteira e redução de risco (0.1 Contrato v1) · **Estado:** IN_PROGRESS

## O que funciona hoje (confirmado no código)
- Código de produção: ainda não iniciado. O repositório só tem documentação (`README.md`, `docs/01`–`docs/13`, `docs/adr/`).
- Papel: plataforma headless central; cliente inicial: aplicativo Android RIN; primeiro caso de uso: módulo Projeto Vivo. Hardware-alvo: Galaxy Book6 Pro com 32 GB.

### Concluído (fundação documental)
- Sobreposição entre RIN e AI Workstation analisada.
- AI Workstation definida como dona de API, execução, agentes, memória canônica, Git local, políticas e auditoria.
- RIN definido como Control Plane Android; Projeto Vivo definido como módulo do RIN.
- "RIN Server" incorporado ao AI Workstation Node/API.
- Fronteira e contrato inicial entre repositórios documentados.
- Hermes e Obsidian preservados como trilhas opcionais por adaptador.

### Não iniciado
- Scaffold do serviço; escolha documentada da stack; banco/event log; pairing e autenticação; adaptadores Git/agentes; spikes Hermes e Obsidian.

## Última atividade
- ID / commit: `c274af4` (2026-09-20) — referências de estudo do Hermes Power Pack (`docs/13-referencias-hermes-power-pack.md`).
- Resultado real: só documentação.
- Testes executados: não há testes (sem código).
- Evidência: `git log`.

## Próxima ação
- Fase 0.1 — definir o contrato v1 executável e implementar o menor serviço com `GET /health`, capabilities, lista simulada de projetos, event cursor e erros estruturados. O RIN deve consumir o mesmo contrato via fake antes da integração real.

## Bloqueios e aprovações humanas
- Sistema operacional/WSL do nó será validado quando o Galaxy Book estiver disponível.
- Transporte de eventos e pareamento ainda exigem ADR.
- Interfaces oficiais atuais dos provedores precisam de validação antes de implementação.

## Divergências entre roadmap e implementação
- Comandos de execução e verificação: a definir (sem código; a stack sai do spike 0.2).
- O `CHANGELOG.md` não tinha versões; os números `0.x.y` foram atribuídos na padronização com as datas dos commits.
