# Continuidade da execução — GA-001

Documentação administrativa produzida pelo agente de IA. O [estado.json](estado.json) é o índice da execução; [cards.json](../kanban/cards.json) preserva o detalhamento dos cards.

## Retomar um Work

1. Consultar o head remoto e ler [AGENTS.md](../../AGENTS.md), [README](../../README.md), este procedimento e o estado da execução.
2. Recuperar a versão e o commit fixo do contrato a partir do estado; não substituir os snapshots por revisões atuais de um portal ou os documentos por rascunhos.
3. Identificar a etapa, issue, evidências e próxima ação. Se a cópia for local, distinguir a referência consultada de uma atualização remota que não ocorreu.
4. Retomar uma tarefa por vez. A solução técnica e as decisões são de Bruno; o agente responde pela governança e orientação.
5. Usar as evidências já registradas sem refazer etapas comprovadas. Perguntar apenas quando faltar informação relevante.

## Registrar um checkpoint

- Registrar o que foi realizado e o que permanece pendente.
- Atualizar estado, issue, exportação, declaração de apoio e README quando necessário.
- Diferenciar execução pelo agente, saída fornecida por Bruno e inspeção estática. Não transformar explicação em conclusão técnica.
- Usar referências reais de arquivos, comandos, saídas e commits; não inventar hash, URL ou resultado.
- Conferir JSON e consistência de IDs, dependências e estados.
- Persistir no Git e informar a referência concluída. O commit que contém um estado é identificado pelo histórico Git; não inserir um hash inventado no próprio arquivo para tentar antecipar o commit.

## Concorrência e sincronização local

Releia head e arquivos antes de gravar. Atualizações do remoto devem detectar avanço concorrente; preserve as mudanças de Bruno e não force sobrescrita.

Alterações administrativas feitas pelo agente no remoto precisam chegar à cópia local antes das etapas seguintes. Registrar a sincronização como pendente enquanto não houver saída fornecida por Bruno que a confirme.

## Estados e evidências

As etapas administrativas podem ser executadas pelo agente. Etapas técnicas só são concluídas com as evidências de Bruno previstas no contrato.

O Project possui Status próprio. Estado aberto/fechado da issue e estado documental da exportação não substituem uma leitura do campo do Project. Quando a conexão não oferece essa leitura, identificar confirmações de Bruno como sua fonte.

A próxima ação deve ser concreta e manter dependências e bloqueios explícitos. Pastas vazias e registros administrativos não significam implementação do fluxo analítico.
