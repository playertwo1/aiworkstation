# Escopo do MVP da AI Workstation

## Hipótese

Antes da orquestração real, o maior risco é a fronteira entre celular e computador. O MVP provará uma plataforma headless segura e rastreável consumível pelo RIN, primeiro com dados simulados e depois com Git em leitura.

## Incluído

### Serviço do nó

- instalação local/headless;
- health, versão e capabilities;
- configuração sem segredos no Git;
- encerramento e reinício coerentes.

### Projetos e estado

- cadastro de raízes autorizadas;
- projetos, checkpoints, decisões e work items;
- snapshots e event log persistentes;
- erros estruturados;
- cursor para sincronização incremental.

### API v1

- projetos e detalhe;
- eventos;
- comandos tipados simulados;
- aprovações simuladas;
- idempotência, timeout e versionamento;
- testes de contrato compatíveis com RIN.

### Git em leitura

- branch, HEAD, working tree e commits;
- sanitização de caminhos/conteúdo;
- vínculo entre afirmação e evidência.

### Simuladores

- fake agent;
- fake Git repository;
- estados de sucesso, falha, espera, cancelamento e interrupção;
- execução reproduzível em CI.

## Fora do MVP

- código Android, Room, Compose ou notificações;
- execução real de Codex/Claude/Antigravity;
- roteamento e fallback automáticos;
- Hermes obrigatório;
- Obsidian obrigatório;
- shell remoto;
- push/merge/destruição;
- multiusuário;
- Diretor 360/dados bancários;
- acesso público pela internet.

## Critério de saída

O MVP está pronto quando o RIN consegue parear em ambiente de teste, consultar health/capabilities, sincronizar três projetos, recuperar eventos após desconexão e acompanhar uma sessão simulada sem falso sucesso ou perda de estado.
