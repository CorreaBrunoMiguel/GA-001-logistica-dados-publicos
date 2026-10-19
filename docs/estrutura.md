# Organização do repositório

Autoria administrativa: agente de IA. Esta estrutura organiza a GA-001 e pode ser ajustada com justificativa; não é um critério adicional da rubrica.

| Local | Finalidade | Situação inicial |
| --- | --- | --- |
| data/raw/ | Arquivos originais contratados, preservados sem transformação | Vazio; obtenção e hashes na PREP-07 |
| data/processed/ | Dados derivados, se necessários e identificados como transformação | Vazio |
| src/ | Implementação Python autoral de Bruno | Vazio |
| sql/ | Estrutura, carga e consultas SQL autorais de Bruno | Vazio |
| notebooks/ | Diagnóstico ou análise autorais, se Bruno escolher notebooks | Vazio |
| results/tables/ | Saídas tabulares em formato aberto | Vazio |
| results/figures/ | Visualizações produzidas pelo fluxo SQL–Python | Vazio |
| docs/ambiente.md | Inventário e futura documentação do ambiente efetivamente usado | Inventário inicial registrado |
| docs/decisoes-tecnicas.md | Registro das decisões técnicas de Bruno | Estrutura administrativa sem decisões inventadas |
| docs/apoio-ia.md | Declaração factual do apoio da IA | Declaração inicial |
| docs/continuidade/ | Estado e procedimento de retomada | Fonte de continuidade da execução |
| docs/kanban/ | Inventário e exportação dos cards | 19 issues cadastradas |

Os arquivos .gitkeep apenas permitem versionar pastas vazias. Não constituem código, dados, consultas ou resultados.

Dados originais e resultados necessários à reprodução não são ignorados por regra geral. O registro de obtenção deve indicar onde estão os arquivos, a referência fixa e os hashes. Atribuição e identificação de transformações permanecem obrigatórias conforme o contrato.

A configuração de exemplo será definida na PREP-06 conforme a conexão escolhida. Dependências serão registradas na PREP-05 a partir das versões efetivas. Não há código de ingestão, modelo relacional, consultas ou análises implementados nesta preparação administrativa.

| Entregável | Localização prevista, a completar por Bruno |
| --- | --- |
| E01 | Python, SQL, dependências, configuração de exemplo e ordem de execução no README |
| E02 | Documentação ou notebook técnico, origem, diagnóstico, decisões e reconciliação |
| E03 | Saídas abertas, figuras e relatório técnico ou notebook narrativo autoral |
| E04 | Issues, Project, exportação, apoio da IA, continuidade e referência fixa da submissão |
