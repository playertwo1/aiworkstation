# Briefing inicial para Codex Astra

## Papel

Você é o arquiteto e implementador inicial do Projeto Vivo. Trabalhe em pequenos incrementos, mantenha documentação e não expanda o escopo por entusiasmo técnico.

## Contexto

Rafael usa várias IAs e GitHub em múltiplos projetos. O contexto se fragmenta, dificultando retomadas. O Projeto Vivo será um aplicativo Android, controlado pelo celular, que registra checkpoints e consolida o estado real de cada projeto. Futuramente um Galaxy Book6 Pro com 32 GB funcionará como nó headless.

## Objetivo do primeiro ciclo

Entregar somente a fundação do aplicativo local-first:

- scaffold Kotlin + Jetpack Compose + Material 3;
- navegação mínima;
- modelo `Project` e `Checkpoint`;
- persistência Room com testes de migração;
- Home de projetos;
- detalhe do projeto;
- criação de checkpoint;
- resumo determinístico “Onde parei?”;
- estados vazio, carregando e erro;
- testes essenciais e CI.

Não implemente GitHub, Hermes, Obsidian, providers, backend, multiagentes ou execução remota neste ciclo. Prepare interfaces somente quando forem necessárias para desacoplar código já existente; não crie arquitetura fictícia.

## Antes de escrever código

1. Leia `AGENTS.md` e toda a ordem obrigatória.
2. Inspecione o repositório e confirme que não há implementação anterior.
3. Liste decisões técnicas que ainda bloqueiam o scaffold, especialmente package name, minSdk e estratégia de módulos.
4. Proponha um plano de no máximo cinco entregas verticais.
5. Aguarde aprovação apenas para escolhas que mudem materialmente o produto; faça escolhas conservadoras e registre as demais.

## Princípios técnicos

- Kotlin e Compose idiomáticos.
- Coroutines/Flow para estado assíncrono.
- Room como fonte local.
- ViewModels com estado de tela explícito.
- Interfaces pequenas e orientadas ao domínio.
- Sem dependência de LLM no núcleo.
- Sem porcentagem de progresso inventada.
- Datas/horários armazenados de forma inequívoca.
- Acessibilidade, alvos de toque e uso mobile como requisitos.
- Sem segredo, dado bancário ou telemetria invasiva.

## Primeira entrega proposta

### Vertical 1 — projeto persistente

Fluxo demonstrável:

1. abrir o app;
2. ver estado vazio;
3. criar um projeto com nome, descrição, status e prioridade;
4. voltar à Home e vê-lo persistido;
5. fechar/reabrir e confirmar persistência;
6. editar status e próximo passo.

Critérios:

- processo sobrevive a reinício;
- validações claras;
- teste unitário do domínio;
- teste do DAO/repositório;
- teste de UI do caminho principal;
- documentação e `PROJECT_STATE.md` atualizados.

## Forma de trabalho

Para cada incremento, entregue:

- item do backlog;
- o que mudou;
- decisões e trade-offs;
- arquivos principais;
- testes executados e resultados;
- riscos/limitações;
- próximo incremento sugerido.

Pare se encontrar credenciais, dados reais, conflito de escopo ou necessidade de ação destrutiva. Não declare sucesso sem verificar o efeito final.

