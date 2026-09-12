# Estado da AI Workstation

Atualizado em: 2026-09-12

## Agora

- Fase: 0 — fundação documental e contratos.
- Papel: plataforma headless central.
- Cliente inicial: aplicativo Android RIN.
- Primeiro caso de uso: módulo Projeto Vivo.
- Código de produção: ainda não iniciado.
- Hardware-alvo: Galaxy Book6 Pro com 32 GB.

## Concluído

- Sobreposição entre RIN e AI Workstation analisada.
- AI Workstation definida como dona de API, execução, agentes, memória canônica, Git local, políticas e auditoria.
- RIN definido como Control Plane Android.
- Projeto Vivo definido como módulo do RIN.
- “RIN Server” incorporado ao AI Workstation Node/API.
- Fronteira e contrato inicial entre repositórios documentados.
- Hermes e Obsidian preservados como trilhas opcionais por adaptador.

## Próximo marco

Definir o contrato v1 executável e implementar o menor serviço com `GET /health`, capabilities, lista simulada de projetos, event cursor e erros estruturados. O RIN deve consumir o mesmo contrato via fake antes da integração real.

## Não iniciado

- Scaffold do serviço.
- Escolha documentada da stack.
- Banco/event log.
- Pairing e autenticação.
- Adaptadores Git/agentes.
- Spikes Hermes e Obsidian.

## Bloqueios

- Sistema operacional/WSL do nó será validado quando o Galaxy Book estiver disponível.
- Transporte de eventos e pareamento ainda exigem ADR.
- Interfaces oficiais atuais dos provedores precisam de validação antes de implementação.
