# Visão do Produto Vivo

## Problema

Rafael desenvolve vários projetos usando Codex, Claude, Antigravity, GitHub e outras ferramentas. O contexto fica fragmentado entre conversas, commits, arquivos, issues e anotações. Retomar um projeto exige reconstruir manualmente o que aconteceu e aumenta o risco de repetir trabalho, perder decisões ou executar a próxima ação errada.

## Visão

O Projeto Vivo será o **sistema operacional pessoal de projetos assistidos por IA**. Ele reunirá estado, contexto, histórico, agentes e capacidade de execução em uma experiência móvel simples.

## Promessa central

Ao abrir um projeto, o usuário entende em menos de 30 segundos:

- estado atual;
- última mudança relevante;
- agente ou ferramenta que trabalhou nele;
- bloqueios e riscos;
- decisões recentes;
- próximo passo recomendado;
- se é seguro continuar.

## Usuário inicial

Um único usuário: Rafael. O produto será otimizado para seu fluxo real antes de qualquer ambição multiusuário.

## Cenário principal

1. Rafael abre o app no Android.
2. Vê os projetos e seus estados.
3. Abre `Diretor 360`, `Minha Floresta`, `RelogioFace` ou outro projeto.
4. Toca em **Onde parei?**.
5. O sistema consolida estado registrado, Git e tarefas.
6. Rafael revisa o próximo passo.
7. Somente em fase posterior, toca em **Continuar** e escolhe/autoriza um agente.

## Pilares

### Continuidade

O projeto conserva um checkpoint compreensível, não apenas logs brutos.

### Evidência

Cada afirmação importante deve apontar sua origem: commit, issue, arquivo, sessão ou anotação.

### Controle humano

Agentes propõem; Rafael aprova ações críticas, aprendizados e mudanças permanentes.

### Eficiência

Serviços ficam ociosos quando não usados. O processamento pesado permanece preferencialmente na nuvem; o notebook orquestra.

### Portabilidade

Componentes externos devem ser substituíveis. O produto não pode depender irreversivelmente de um único runtime ou provedor.

## Não objetivos iniciais

- Criar uma IDE móvel completa.
- Substituir GitHub, Obsidian, Codex, Claude, Gemini, Hermes ou n8n.
- Rodar modelos grandes localmente.
- Automatizar alternância de assinaturas antes de validar suporte oficial e termos.
- Gerenciar dados bancários ou implementar o Diretor 360 no MVP.

## Métricas iniciais de sucesso

- Tempo mediano para entender onde o projeto parou: abaixo de 30 segundos.
- Checkpoints com fonte rastreável: 100%.
- Retomadas sem reconstrução manual de contexto: pelo menos 80% nos projetos-piloto.
- Zero ação crítica executada sem confirmação.
- App utilizável integralmente no celular.

