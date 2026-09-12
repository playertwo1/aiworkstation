# Divisão entre RIN e AI Workstation

Status: decisão aceita em 2026-09-12.

## Hierarquia

- **AI Workstation:** plataforma/cérebro no computador.
- **RIN:** aplicativo Android/controle remoto.
- **Projeto Vivo:** primeiro módulo funcional dentro do RIN.

## Matriz de responsabilidade

| Capacidade | AI Workstation | RIN |
|---|---:|---:|
| API e autenticação do nó | dona | cliente |
| Git local e GitHub | dona | visualiza via API |
| Sessões e agentes | dona | solicita/acompanha |
| Memória canônica e event log | dona | exibe/cacheia |
| Policy engine e auditoria | dona | coleta decisão |
| Hermes/Obsidian/n8n | integra | não integra diretamente |
| UI Android/Compose | não | dona |
| Room/cache offline | não | dona |
| Notificações e biometria | fornece evento/desafio | dona |
| Projeto Vivo UX | fornece dados/capacidades | dona |
| AI Shift | executa e confirma | inicia/aprova/apresenta |

## Conteúdo migrado conceitualmente

Do desenho original do RIN para AI Workstation:

- RIN Server;
- filas e supervisor de processos;
- adaptadores de agentes;
- Git local;
- memória canônica;
- policy engine;
- audit log;
- exportação de handoff;
- Hermes, Obsidian e automações.

Do desenho original do AI Workstation para RIN:

- Home e detalhe de projetos;
- checkpoints editáveis no celular;
- resumo visual “Onde parei?”;
- telas de sessões, aprovações e workstation;
- cache offline e sincronização móvel.

## Regra contra duplicação

Antes de adicionar uma capacidade, perguntar:

1. É interface, interação ou comportamento específico do Android? Então RIN.
2. Exige filesystem, processo, Git local, segredo, agente, política ou estado canônico? Então AI Workstation.
3. É compartilhado? O contrato pertence à plataforma; modelos espelhados no RIN são gerados ou validados por testes.
4. Ainda há dúvida? Registrar ADR antes de codificar.

## Contrato e compatibilidade

O contrato funcional nasce em `playertwo1/rin/docs/INTEGRATION_CONTRACT.md` durante a fundação e deve evoluir para um pacote versionado pela AI Workstation. Ambos os repositórios executam os mesmos testes de contrato. Capabilities permitem degradação segura.

## Sequência integrada

1. Congelar fronteiras e contratos.
2. RIN implementa Projeto Vivo local + fake gateway.
3. AI Workstation implementa fake server equivalente.
4. Integrar health, projects e eventos.
5. Adicionar Git em leitura.
6. Adicionar sessões simuladas.
7. Validar segurança/pareamento.
8. Somente então testar um agente real.
9. Hermes e Obsidian continuam em spikes independentes.

## Documentos históricos

Arquivos de síntese e DOCX não serão apagados. Quando divergirem, prevalecem este documento, README, PROJECT_STATE, decisões e roadmaps atuais.
