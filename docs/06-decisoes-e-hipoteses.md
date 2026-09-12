# Decisões, hipóteses e questões abertas

## Decisões vigentes

| ID | Decisão | Motivo |
|---|---|---|
| D-001 | AI Workstation é a plataforma headless central | Elimina dois backends concorrentes |
| D-002 | RIN é o aplicativo Android/Control Plane | Mantém UX móvel em repositório próprio |
| D-003 | Projeto Vivo é o primeiro módulo do RIN | Evita terceiro produto sobreposto |
| D-004 | “RIN Server” passa a ser AI Workstation Node/API | Consolida execução, memória e políticas |
| D-005 | Git/GitHub é a verdade do código | Estado verificável |
| D-006 | Banco/event log da plataforma é a verdade operacional | Recuperação e auditoria |
| D-007 | Integração usa contrato v1 e capabilities | Evolução independente |
| D-008 | RIN nunca acessa CLI, filesystem ou banco do nó diretamente | Segurança e desacoplamento |
| D-009 | Aprovação humana para ações críticas | Governança |
| D-010 | Hermes, Obsidian e provedores são adaptadores opcionais | Evita lock-in |
| D-011 | MVP começa por fake + contrato, depois Git leitura | Reduz risco |
| D-012 | Diretor 360 permanece fora do MVP | Separação de domínios e dados |

## Hipóteses a validar

| ID | Hipótese | Como validar |
|---|---|---|
| H-001 | Hermes economiza infraestrutura genérica | Spike isolado com métricas e ADR |
| H-002 | Obsidian melhora continuidade | Exportação Markdown + uso real |
| H-003 | Contrato mínimo cobre o Projeto Vivo | Fake e cliente RIN com testes compartilhados |
| H-004 | Nó headless cabe confortavelmente em 32 GB | Medir idle, pico, build e concorrência |
| H-005 | Integrações oficiais permitem alguns planos | Validar documentação, termos e autenticação |
| H-006 | Fallback entre providers agrega valor | Começar manual e medir falha/custo/fricção |

## Questões abertas

- Fastify ou Ktor para o nó.
- SQLite ou PostgreSQL no piloto.
- REST + WebSocket ou REST + SSE.
- Pareamento e acesso fora da rede local.
- Formato/repositório do pacote de contratos.
- Obsidian Sync, Git ou outro mecanismo para o Vault.
- Hermes: adotar, adaptar ou somente estudar padrões.
- Política de backup e recuperação.
- Projetos-piloto definitivos.

## Regra externa

Recursos, OAuth, assinaturas e quotas mudam. Revalidar em documentação oficial, registrar data/versão e classificar: `confirmado`, `parcial`, `não suportado` ou `incerto`.
