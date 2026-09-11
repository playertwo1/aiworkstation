# Segurança e privacidade

## Modelo de ameaça inicial

Ativos protegidos:

- tokens e sessões de provedores;
- repositórios e código privado;
- documentos e conhecimento pessoal;
- capacidade de executar comandos no Galaxy Book;
- histórico e decisões dos projetos.

Riscos prioritários:

- roubo de token;
- comando remoto arbitrário;
- prompt injection em documentos/repositórios;
- vazamento em logs;
- agente promovendo regra/memória indevida;
- confusão entre projetos;
- sobrescrita ou exclusão sem recuperação;
- falsa indicação de sucesso.

## Controles obrigatórios

- segredos fora do Git, Room comum e logs;
- armazenamento seguro de credenciais no Android e no nó;
- menor privilégio e escopos mínimos;
- sessão e workspace isolados por projeto;
- allowlist de comandos/capacidades;
- sem endpoint de shell genérico;
- aprovação explícita para escrita remota, merge, exclusão, mudança de regra e promoção de aprendizado;
- auditoria imutável ou resistente a adulteração;
- confirmação de efeito: não declarar sucesso só porque uma fila aceitou a tarefa;
- timeouts, cancelamento e idempotência;
- backups e rollback testados;
- sanitização de conteúdo não confiável antes de alimentar agentes.

## Matriz inicial de aprovação

| Ação | Política inicial |
|---|---|
| Ler status/commit público ou autorizado | Automática |
| Atualizar cache local | Automática |
| Gerar resumo | Automática, com fontes |
| Criar branch de trabalho isolada | Aprovação configurável |
| Alterar arquivo/código | Revisão do diff antes de integrar |
| Push, PR ou merge | Aprovação explícita inicialmente |
| Executar comando privilegiado | Aprovação explícita |
| Excluir arquivo, branch ou dado | Aprovação explícita + recuperação |
| Promover memória/skill/regra | Learning Gate obrigatório |
| Enviar dado a novo provedor | Consentimento e política de dados |

## Dados bancários

Este repositório não deve conter dados reais de clientes, credenciais bancárias ou documentos internos. Uma eventual plataforma compartilhada exigirá separação forte de domínios, políticas e repositórios.

