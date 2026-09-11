# Instruções para agentes

## Missão atual

Construir o Projeto Vivo em incrementos pequenos, verificáveis e reversíveis. Não iniciar o Diretor 360 neste repositório sem decisão explícita registrada.

## Ordem de leitura obrigatória

1. `README.md`
2. `docs/01-visao-produto.md`
3. `docs/02-escopo-mvp.md`
4. `docs/03-arquitetura-inicial.md`
5. `docs/04-roadmap.md`
6. `docs/06-decisoes-e-hipoteses.md`
7. `docs/07-seguranca.md`

## Princípios

- Local-first sempre que for simples e seguro.
- O app Android controla; não executa cargas pesadas.
- GitHub é a verdade do código e do histórico versionado.
- Nenhuma integração de assinatura é presumida até um spike provar autenticação, limites, estabilidade e conformidade.
- Nenhuma ação destrutiva, promoção de memória, alteração de regra ou execução privilegiada ocorre sem aprovação humana.
- Diferenciar fato confirmado, hipótese, decisão e questão aberta.
- Não misturar conhecimento, memória operacional, dados de negócio e código.
- Entregas pequenas: uma história vertical por vez, com critérios de aceite e testes.

## Disciplina de mudança

- Antes de implementar, identifique o item do roadmap/backlog.
- Se uma escolha arquitetural importante surgir, crie ou atualize um ADR em `docs/adr/`.
- Atualize `PROJECT_STATE.md` e `CHANGELOG.md` em toda entrega material.
- Não armazenar tokens, cookies, segredos, dados bancários ou dados pessoais no Git.
- Preferir mocks e contratos na primeira fase; integrações reais entram depois dos spikes.

## Definition of Done

Uma entrega só está concluída quando:

- critérios de aceite foram satisfeitos;
- testes relevantes passaram;
- documentação afetada foi atualizada;
- estados de erro e carregamento foram considerados;
- segurança e privacidade foram revisadas;
- não há segredo no diff;
- o próximo passo está registrado.

