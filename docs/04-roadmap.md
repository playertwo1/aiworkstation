# Roadmap em pequenas partes

Não há datas artificiais. Cada marco termina com evidência demonstrável e decisão de continuar, ajustar ou descartar.

## Duas trilhas desde o início

O Projeto Vivo será desenvolvido em duas trilhas coordenadas:

| Trilha | Começa | Objetivo | Regra |
|---|---|---|---|
| Produto Android | Fase 0 | Provar “Onde parei?” e continuidade | Não depender do Hermes |
| Hermes Runtime | Fase 0 | Descobrir se Hermes serve como motor de agentes | POC isolado, sem modificar projetos reais |

O Hermes não foi adiado para o fim. Sua investigação começa antes do código de produção, mas a integração só acontece depois de evidência suficiente. Detalhes completos estão em `docs/11-trilha-hermes.md`.

## Fase 0 — Fundação

### Marco 0.1 — Alinhar o produto

- validar a promessa central;
- confirmar o nome “Projeto Vivo” e o nome técnico;
- escolher os três projetos-piloto;
- confirmar package Android e política de versões;
- registrar configuração real do Galaxy Book após a chegada.

**Aceite:** uma página de visão aprovada e questões abertas classificadas.

### Marco 0.2 — Protótipo de fluxo

- wireframes de home, detalhe e checkpoint;
- testar navegação 100% no celular;
- validar linguagem e densidade de informação;
- evitar botão “Continuar” que prometa execução ainda inexistente.

**Aceite:** Rafael consegue simular a retomada de um projeto sem explicação externa.

### Marco 0.3 — Spikes de risco

- autenticação GitHub e limites mínimos;
- iniciar a Trilha Hermes com POC isolado e repositório descartável;
- validar instalação headless, licença, manutenção, API real e compatibilidade com Windows/WSL;
- testar profiles, sessões, busca, memória, skills, approvals, cancelamento e eventos;
- medir providers realmente disponíveis, autenticação oficial, limites e consumo;
- comparar integração direta via `AgentRuntimeProvider` com adoção mais profunda;
- Obsidian: arquivos Markdown primeiro; CLI/Headless como opção;
- comunicação segura Android ↔ nó headless;
- prova de suspensão/retomada de serviço sem perda de estado.

**Aceite Hermes:** demonstração reproduzível e um parecer preliminar `promissor`, `limitado` ou `inviável`. Isso ainda não autoriza acoplamento ao app.

**Aceite geral:** relatório reproduzível com passou/falhou, evidência e recomendação para cada spike.

### Marco 0.4 — Gate Hermes H0

- consolidar evidências do POC;
- comparar Hermes com runtime próprio mínimo;
- registrar lacunas, riscos de lock-in e esforço de adaptação;
- decidir uma das opções: `adotar por adaptador`, `adaptar componentes`, `continuar estudando` ou `descartar`;
- criar ADR com a decisão.

**Gate H0:** nenhuma funcionalidade do MVP Android pode depender do Hermes antes deste gate.

## Fase 1 — Aplicativo local

### Marco 1.1 — Casca Android

- projeto Kotlin/Compose;
- tema Material 3;
- navegação;
- CI mínima;
- testes unitários e de UI essenciais.

### Marco 1.2 — Projetos persistentes

- schema Room e migração inicial;
- CRUD de projetos;
- Home com filtros;
- estados vazios, erro e carregamento.

### Marco 1.3 — Checkpoints

- criação e edição;
- histórico cronológico;
- decisões, bloqueios e próximo passo;
- rastreabilidade por fonte.

### Marco 1.4 — “Onde parei?” local

- composição determinística do resumo a partir do último checkpoint e pendências;
- sem IA obrigatória;
- indicação de desatualização.

**Gate F1:** usar três projetos reais durante uma semana sem perda de dados.

## Fase 2 — GitHub em modo leitura

### Marco 2.1 — Conexão segura

- autenticação adequada para app pessoal;
- token fora do banco e dos logs;
- revogação e reconexão;
- escopo mínimo.

### Marco 2.2 — Estado Git

- repositório e branches;
- último commit;
- issues e PRs selecionados;
- cache e sincronização manual.

### Marco 2.3 — Resumo com evidências

- juntar checkpoint local e GitHub;
- cada trecho aponta para sua fonte;
- conflito entre relato e Git fica visível.

**Gate F2:** o resumo reproduz corretamente o estado de três repositórios.

## Fase 3 — Nó headless

### Marco 3.1 — Agente do nó

- serviço instalável no Galaxy Book/WSL;
- health check;
- pairing seguro;
- capacidade e versão reportadas ao app.

### Marco 3.2 — Observabilidade

- CPU, RAM, disco, energia e serviços;
- logs estruturados;
- estados online/offline/degradado;
- limites de concorrência.

### Marco 3.3 — Comandos não destrutivos

- sincronizar repositório;
- verificar status;
- coletar contexto;
- cancelar tarefa;
- idempotência e timeout.

**Gate F3:** executar comandos permitidos do celular, com auditoria e sem shell arbitrário.

### Marco 3.4 — Hospedar o adaptador Hermes, se aprovado

- executar o Hermes no Galaxy Book/WSL como serviço isolado;
- expor somente capacidades permitidas pelo `AgentRuntimeProvider`;
- separar sessões e workspaces por projeto;
- health check, cancelamento, timeout e recuperação de falhas;
- limites de CPU, RAM e concorrência;
- nenhum token no Android ou nos logs.

**Gate H1:** o nó continua seguro e funcional quando o Hermes falha, reinicia ou fica indisponível.

## Fase 4 — Knowledge Hub

### Marco 4.1 — Exportação Markdown

- estrutura de Vault proposta;
- exportar checkpoints e decisões;
- links estáveis e metadados legíveis;
- Git opcional para o Vault sem segredos.

### Marco 4.2 — Obsidian opcional

- testar desktop CLI versus Headless;
- leitura limitada à pasta autorizada;
- busca e backlinks como contexto;
- conflitos e versionamento.

**Gate F4:** Obsidian agrega valor sem virar dependência do núcleo.

## Fase 5 — Runtime de agentes

### Marco 5.1 — Abstração de runtime

- contrato de sessão, tarefa, evento, cancelamento e resultado;
- fake runtime para testes;
- política de timeout, custo e auditoria.

### Marco 5.2 — Spike Hermes

- revalidar o POC da Fase 0 contra a versão atual;
- implementar o adaptador somente se o Gate H0 aprovou o caminho;
- validar handoff, persistência, busca de sessões e retomada real;
- integrar skills e approvals sem permitir autopromoção;
- medir RAM/CPU, cancelamento e recuperação sob carga;
- atualizar o ADR de adoção.

### Marco 5.3 — Primeiro trabalho assistido

- somente tarefa reversível em repositório de teste;
- branch isolada;
- diff e testes apresentados;
- confirmação antes de merge/push quando aplicável.

**Gate F5:** uma retomada real assistida termina com evidência e controle humano.

**Gate H2:** o app troca o Hermes por um runtime falso ou alternativo sem perder o estado principal do projeto.

## Fase 6 — Providers e continuidade

- matriz oficial de capacidades por provedor;
- autenticação individual e revogável;
- quotas e erros explícitos;
- seleção manual primeiro;
- fallback automático apenas quando permitido, transparente e seguro;
- nunca burlar limites ou termos de assinatura.

## Fase 7 — Learning Gate

- detectar proposta de memória/skill/regra;
- classificar e anexar evidências;
- validar automaticamente;
- Rafael aprova/rejeita;
- versionar, auditar e permitir rollback;
- impedir autopromoção direta para produção.

## Fase 8 — Plataforma compartilhada futura

Somente após o Projeto Vivo estar estável, avaliar extração de infraestrutura compartilhada para `Rafael AI Platform` e integração com o Diretor 360. Esse marco não autoriza levar dados bancários ao Projeto Vivo.
