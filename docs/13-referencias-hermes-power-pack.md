# Referências — Hermes Power Pack

> Status: **referência para estudo / POC**. Nenhum item desta página é dependência aprovada da AI Workstation.

Pesquisa revisada em **19/09/2026**. O objetivo é manter uma lista curta de extensões e ferramentas que podem tornar o próprio Hermes mais eficaz antes de qualquer acoplamento ao núcleo da AI Workstation.

## Regra de uso

Estas referências devem ser avaliadas primeiro no Hermes, em profile/workspace de teste. A AI Workstation continua dependendo de seus próprios contratos, estado canônico, políticas e evidências. Um plugin ou skill do Hermes só pode influenciar a arquitetura depois de POC, medição e decisão explícita.

## Candidatos

| Componente | Tipo | O que acrescenta ao Hermes | Estado sugerido |
|---|---|---|---|
| [RTK](https://github.com/rtk-ai/rtk) | CLI + plugin Hermes | Compacta output de terminal e reduz contexto desperdiçado. A integração Hermes usa reescrita de chamadas do tool `terminal`. | **POC prioritária** |
| [Planning with Files](https://github.com/OthmanAdi/planning-with-files) | Skill + plugin Hermes | Plano, findings e progresso persistentes com hooks para reinjeção e retomada de tarefas longas. | **POC prioritária** |
| [Agent Reach](https://github.com/Panniantong/Agent-Reach) | CLI + skill/ecossistema de ferramentas | Pesquisa e leitura especializada em Web, YouTube, GitHub, RSS e outros canais; inclui `doctor` e instalação em modo seguro/read-only. | **POC após baseline** |
| [Delegate Skills](https://github.com/amElnagdy/delegate-skills) | Skills + relay | Permite ao orquestrador delegar para CLIs como Codex e Antigravity, devolver resultado estruturado e manter review/commit no orquestrador. | **Experimento controlado** |
| [Google Mantis](https://github.com/google/mantis) | Coleção de skills + harness | Threat modeling, revisão, reprodução e patching de vulnerabilidades. O projeto exige isolamento forte para execução dinâmica. | **Somente isolado** |
| [Skill Retrieval](https://github.com/moonlight-lupin/agent-skills) | Plugin Hermes | BM25 sobre nomes/descrições de skills e injeção apenas do top-K relevante; útil quando o catálogo cresce. | **Adiar até haver necessidade medida** |

## Compatibilidade com capacidades nativas do Hermes

Antes de adotar qualquer item, comparar com o que o Hermes já oferece:

- **Skills com progressive disclosure:** evitar resolver duas vezes o mesmo problema.
- **Plugins e hooks:** preferir integração suportada pelo Hermes a hacks no prompt.
- **`delegate_task` e skills oficiais de agentes autônomos:** comparar com Delegate Skills antes de adicionar outra camada.
- **Sessions, memory e checkpoints:** Planning with Files deve complementar, não virar fonte canônica.
- **Web/search/browser:** Agent Reach deve entrar apenas onde suas rotas especializadas trouxerem ganho real.

Documentação:
- [Hermes — Skills System](https://github.com/NousResearch/hermes-agent/blob/main/website/docs/user-guide/features/skills.md)
- [Hermes — Plugins](https://github.com/NousResearch/hermes-agent/blob/main/website/docs/user-guide/features/plugins.md)
- [Hermes — Event Hooks](https://github.com/NousResearch/hermes-agent/blob/main/website/docs/user-guide/features/hooks.md)
- [Hermes — Releases](https://github.com/NousResearch/hermes-agent/releases)

## Gates mínimos para H0

Para cada candidato:

1. registrar versão e forma de instalação;
2. testar em profile/repositório descartável;
3. medir RAM, CPU, disco, tempo e impacto de tokens quando aplicável;
4. verificar falha, cancelamento e retomada;
5. testar como desligar/desinstalar;
6. confirmar que nenhuma extensão vira fonte única do estado;
7. só então classificar como `adotar por adaptador`, `adaptar componentes`, `continuar estudando` ou `descartar`.

## Ordem de estudo sugerida

1. RTK
2. Planning with Files
3. Agent Reach em canais públicos/zero-config
4. Delegate Skills com `delegate-setup`, `codex-delegate` e `agy-delegate`
5. Mantis em modo estático/isolado
6. Skill Retrieval quando o catálogo justificar

## Material de apoio

Manual externo da série Nexus Local: **Nexus_Local_Parte_3_Hermes_Power_Pack_v1.docx**.

O manual não é fonte canônica da arquitetura; serve como guia operacional para a POC e deve ser revalidado quando as ferramentas mudarem.
