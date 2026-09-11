# ADR 0002 — Tratar integrações como componentes substituíveis

- Status: aceito
- Data: 2026-09-11

## Contexto

Recursos, autenticação, planos e termos de Hermes, Obsidian e provedores podem mudar. O produto precisa sobreviver a essas mudanças.

## Decisão

GitHub, Knowledge Hub, runtime de agentes, nó e providers serão acessados por contratos específicos quando forem implementados. Nenhuma integração opcional será fonte única irrecuperável do estado principal.

## Consequências

- Mais facilidade de testar e trocar integrações.
- Necessidade de manter contratos pequenos e evitar abstrações genéricas demais.
- Todo provider requer spike e decisão antes da adoção.

