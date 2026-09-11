# Escopo do MVP

## Hipótese do MVP

Antes de orquestrar múltiplos agentes, o maior valor pode ser obtido resolvendo continuidade e visibilidade. Portanto, o MVP será um **painel confiável de projetos com checkpoints manuais e sincronização GitHub básica**.

## Incluído

### Cadastro de projetos

- nome, descrição e prioridade;
- repositório GitHub opcional;
- estado: ideia, planejando, ativo, bloqueado, pausado ou concluído;
- tecnologia e ferramenta/agente atual;
- execução local ou futura no nó headless.

### Tela inicial

- lista de projetos;
- status visual sem porcentagens inventadas;
- última atividade;
- bloqueio principal;
- próximo passo;
- filtro por status/prioridade.

### Detalhe do projeto

- resumo **Onde parei?**;
- decisões;
- pendências e bugs;
- checkpoints cronológicos;
- informações Git essenciais;
- fontes/evidências do resumo.

### Checkpoint

- registrar manualmente trabalho realizado;
- registrar agente utilizado;
- resultado, problemas, decisões e próximo passo;
- anexar referência a commit, branch, issue ou arquivo;
- editar com histórico básico.

### GitHub somente leitura

- repositório, branch padrão e branch de trabalho;
- último commit;
- issues/PRs relevantes quando disponível;
- atualização manual e indicação clara de horário da última sincronização.

### Operação offline

- leitura e edição dos dados locais;
- fila de sincronização posterior;
- estados explícitos: local, sincronizando, sincronizado e conflito.

## Fora do MVP

- execução remota de Codex/Claude/Gemini;
- roteamento ou troca automática entre assinaturas;
- autonomia multiagente;
- escrita automática em memória ou skills;
- Obsidian Headless em produção;
- Hermes como dependência obrigatória;
- n8n e PostgreSQL obrigatórios;
- monitor de recursos completo;
- comandos destrutivos no notebook;
- colaboração multiusuário.

## Telas mínimas

1. Onboarding local.
2. Home de projetos.
3. Criar/editar projeto.
4. Detalhe do projeto.
5. Criar checkpoint.
6. Histórico.
7. Configuração da integração GitHub.
8. Central de sincronização/erros.

## Critério de saída do MVP

O MVP está pronto quando Rafael conseguir cadastrar ao menos três projetos reais, registrar checkpoints, fechar e reabrir o app sem perder dados e responder “onde parei?” usando informações rastreáveis do app e do GitHub.

