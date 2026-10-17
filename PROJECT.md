# PROJECT — AI Workstation

Contrato de visão. Atualize quando o projeto nasce e quando a visão muda; o resto (marcos, estado) fica em `ROADMAP.md` e `STATE.md`. Resumo de [`docs/01-visao-produto.md`](docs/01-visao-produto.md), [`docs/02-escopo-mvp.md`](docs/02-escopo-mvp.md) e [`docs/12-divisao-rin-aiworkstation.md`](docs/12-divisao-rin-aiworkstation.md), que continuam sendo o detalhe.

## Problema
Rafael desenvolve vários projetos usando Codex, Claude, Antigravity, GitHub e outras ferramentas. O contexto se fragmenta, os runtimes não compartilham estado confiável e o computador não possui uma camada única de execução, memória, políticas e auditoria.

## Para quem
Um único usuário: Rafael, pelo aplicativo Android RIN (cliente inicial) e pelo Galaxy Book/PC como nó.

## MVP — até três fluxos que entregam valor
1. O RIN pareia com o nó em ambiente de teste e consulta health/capabilities.
2. O RIN sincroniza três projetos (estado, eventos com cursor, Git em leitura) e recupera eventos após desconexão.
3. O RIN acompanha uma sessão simulada (fake agent) sem falso sucesso ou perda de estado.

## Fora do MVP (escrito para não voltar escondido)
- Código Android, Room, Compose ou notificações (pertencem ao `playertwo1/rin`).
- Execução real de Codex/Claude/Antigravity; roteamento e fallback automáticos.
- Hermes ou Obsidian obrigatórios; shell remoto; push/merge/destruição.
- Multiusuário; Diretor 360/dados bancários; acesso público pela internet.

## Restrições
- Plataforma/ambiente: serviço headless local no Galaxy Book6 Pro (32 GB), Windows/WSL a validar; stack a definir por spike (Fastify × Ktor, SQLite × PostgreSQL).
- Dados sensíveis e privacidade: sem segredos no Git; aprovação humana para ações críticas; local-first (`docs/07-seguranca.md`).
- Custos, licenças, integrações obrigatórias: validar autenticação, limites e termos atuais de cada provedor; não burlar quotas, planos ou termos.

## Como saberemos que funcionou
Critério de saída do MVP (`docs/02-escopo-mvp.md`) e métricas de `docs/01-visao-produto.md`: 100% dos estados terminais com evidência, zero ação crítica sem autorização e recuperação coerente após reinício.

## Autoridade de produto
Rafael.

## Alternativas consideradas
"RIN Server" e backend separado do Projeto Vivo, absorvidos pelo AI Workstation Node/API para não haver dois servidores concorrentes (`docs/12-divisao-rin-aiworkstation.md`, ADRs em `docs/adr/`).
