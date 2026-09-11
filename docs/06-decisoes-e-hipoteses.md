# Decisões, hipóteses e questões abertas

## Decisões vigentes

| ID | Decisão | Motivo |
|---|---|---|
| D-001 | Foco inicial somente no Projeto Vivo | Reduz dispersão de um projeto grande |
| D-002 | Android é o Control Plane | Uso prioritário pelo celular |
| D-003 | Galaxy Book é o Execution Node headless | Centraliza serviços e reduz carga no celular |
| D-004 | GitHub é a verdade do código | Histórico e colaboração já consolidados |
| D-005 | Local-first no MVP | Valor e validação antes de backend complexo |
| D-006 | “Onde parei?” vem antes de “Continuar” | Continuidade é o risco/valor principal |
| D-007 | Aprovação humana para ações críticas | Segurança e governança |
| D-008 | Obsidian, Hermes e provedores são adaptadores opcionais | Evita lock-in prematuro |

## Hipóteses a validar

| ID | Hipótese | Como validar |
|---|---|---|
| H-001 | Hermes economiza infraestrutura genérica | Spike isolado com métricas e ADR |
| H-002 | Obsidian melhora continuidade sem aumentar manutenção | Exportação Markdown + teste real de uso |
| H-003 | O resumo determinístico já resolve boa parte de “onde parei?” | Uso por uma semana em três projetos |
| H-004 | Nó headless cabe confortavelmente em 32 GB | Medir idle, pico, build e múltiplos serviços |
| H-005 | Integrações oficiais permitem usar alguns planos/assinaturas | Conferir documentação/termos e autenticar em ambiente de teste |
| H-006 | Fallback entre providers agrega valor | Medir falhas, custo, qualidade e fricção; começar manual |

## Questões abertas

- Nome técnico e package Android.
- Repositório monorepo ou apps separados após o MVP.
- Autenticação GitHub: OAuth/App/device flow adequado ao cenário pessoal.
- Transporte Android ↔ notebook: rede local, túnel privado ou gateway externo.
- Necessidade real de backend central antes do nó headless.
- Obsidian Sync, Git ou outro mecanismo para o Vault.
- Hermes: adotar, adaptar ou somente estudar padrões.
- Política de backup e recuperação.
- Projetos-piloto definitivos.

## Regra para alegações externas

Suporte de OAuth, assinatura, quotas, integrações e recursos de terceiros muda com o tempo. Antes de implementação, toda alegação deve ser revalidada em documentação oficial, registrar data/versão e receber um status: `confirmado`, `parcial`, `não suportado` ou `incerto`.

