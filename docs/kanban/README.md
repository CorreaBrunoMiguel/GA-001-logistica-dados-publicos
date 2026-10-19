# Kanban e inventário dos cards — GA-001

Documentação administrativa produzida pelo agente de IA. Código, SQL, análises e conclusões permanecem com Bruno.

- **Contrato:** GA-001 / 1.0.0, commit 0143e0d4e1a3edf0c084656f9b956a101e24a942.
- **Referências:** [demanda](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/demanda.md), [rubrica](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/rubrica.md), [manifesto](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/manifesto.json) e [política integral](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/politica-execucao.md).
- **Project:** [Project 5](https://github.com/users/CorreaBrunoMiguel/projects/5).
- **Issues:** [lista do repositório](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues).
- **Snapshot completo:** [cards.json](cards.json), com corpo integral, responsáveis, requisitos, dependências, estados, bloqueios e evidências.
- **Data deste snapshot:** 19/10/2026.

## Alcance da conferência

As 19 issues foram criadas e lidas no GitHub. PREP-00, PREP-01 e PREP-02 foram cadastradas retrospectivamente e fechadas com base nas evidências das etapas já realizadas. PREP-03 foi fechada após as confirmações de configuração e entrada dos cards. Há quatro issues fechadas e quinze abertas.

Bruno confirmou o Project como privado; as cinco opções do campo Status e Backlog como padrão; Auto-add ativado para o repositório com filtro is:issue; entrada dos 19 cards; PREP-00/01/02 em Concluído, PREP-03 em Em andamento antes de seu fechamento e demais cards em Backlog. Depois de corrigir os estados iniciais, confirmou o workflow Item closed ativado com destino Concluído.

Essas informações da interface foram fornecidas por Bruno. A conexão do agente não oferece leitura ou edição de Projects. O fechamento da issue 4 foi realizado e consultado no GitHub pelo agente; o valor final do Status do Project após esse fechamento não foi inspecionado pelo agente.

O estado de acompanhamento na tabela é documental. Ele é registrado separadamente do estado aberto/fechado da issue e não é apresentado como leitura direta do campo Status do Project. **PREP-03 concluída; próxima etapa: PREP-04.**

## Estados acordados

| Estado | Significado |
| --- | --- |
| Backlog | Planejada e ainda não liberada |
| Pronto | Liberada, com dependências atendidas |
| Em andamento | Trabalho em execução |
| Em revisão | Evidências aguardando conferência |
| Concluído | Critérios verificados |

Dependências satisfeitas não autorizam marcar uma tarefa como concluída. A sequência será conduzida uma etapa por vez. O agente mantém issues, dependências, evidências e esta exportação; alterações no Project que a conexão não permita serão aplicadas por Bruno com orientação.

## Cards

| ID | Issue | Estado de acompanhamento | Issue no GitHub | Requisitos | Dependências |
| --- | --- | --- | --- | --- | --- |
| PREP-00 | [#1 — Recuperar o contrato publicado e definir papéis](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/1) | Concluído | Fechada | R09, R10, R11 | Nenhuma |
| PREP-01 | [#2 — Inventariar o ambiente local](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/2) | Concluído | Fechada | R11 | PREP-00 |
| PREP-02 | [#3 — Criar o repositório da solução e confirmar o clone](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/3) | Concluído | Fechada | R09, R11 | PREP-00 |
| PREP-03 | [#4 — Configurar o Project, vincular issues e preservar os cards](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/4) | Concluído | Fechada | R09 | PREP-02 |
| PREP-04 | [#5 — Estruturar a governança e a continuidade da execução](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/5) | Backlog | Aberta | R09, R10, R11 | PREP-02 |
| PREP-05 | [#6 — Preparar e identificar o ambiente Python do projeto](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/6) | Backlog | Aberta | R11 | PREP-01, PREP-02 |
| PREP-06 | [#7 — Preparar o destino PostgreSQL e verificar a conexão Python](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/7) | Backlog | Aberta | R11 | PREP-01, PREP-02, PREP-05 |
| PREP-07 | [#8 — Obter e conferir os snapshots contratados](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/8) | Backlog | Aberta | R01, R11 | PREP-02, PREP-04 |
| PREP-08 | [#9 — Conferir a preparação e registrar o checkpoint de ambiente](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/9) | Backlog | Aberta | R09, R10, R11 | PREP-03, PREP-04, PREP-05, PREP-06, PREP-07 |
| T01 | [#10 — Diagnosticar granularidade, cobertura e qualidade dos dois arquivos](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/10) | Backlog | Aberta | R01, R02, R10 | PREP-08 |
| T02 | [#11 — Projetar o modelo relacional e a integridade dos dados](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/11) | Backlog | Aberta | R04, R07, R10 | T01 |
| T03 | [#12 — Implementar ingestão Python e carga reexecutável no PostgreSQL](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/12) | Backlog | Aberta | R03, R04, R07, R10, R11 | T01, T02 |
| T04 | [#13 — Responder Q01 em SQL: evolução mensal de TU e TKU](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/13) | Backlog | Aberta | R05, R07, R10 | T03 |
| T05 | [#14 — Responder Q02 em SQL: concentração nos eixos direcionais](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/14) | Backlog | Aberta | R05, R07, R10 | T03 |
| T06 | [#15 — Responder Q03 em SQL: contribuição das mercadorias à variação](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/15) | Backlog | Aberta | R05, R07, R10 | T03 |
| T07 | [#16 — Consumir resultados SQL no Python e produzir visualizações rastreáveis](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/16) | Backlog | Aberta | R06, R08, R10 | T04, T05, T06 |
| T08 | [#17 — Reconciliar populações, medidas, junções e reexecução](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/17) | Backlog | Aberta | R03, R04, R07, R11 | T03, T04, T05, T06, T07 |
| T09 | [#18 — Elaborar o relatório técnico e registrar interpretações autorais](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/18) | Backlog | Aberta | R08, R10 | T07, T08 |
| T10 | [#19 — Verificar reprodução e preparar a submissão identificada](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/19) | Backlog | Aberta | R09, R10, R11 | T09, PREP-03, PREP-04 |

## Cobertura do contrato

Os cards organizam os requisitos já publicados. Não definem técnicas, notas, prazos ou critérios de aceitação adicionais.

| Requisito | Issues relacionadas |
| --- | --- |
| R01 | [#8](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/8), [#10](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/10) |
| R02 | [#10](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/10) |
| R03 | [#12](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/12), [#17](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/17) |
| R04 | [#11](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/11), [#12](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/12), [#17](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/17) |
| R05 | [#13](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/13), [#14](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/14), [#15](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/15) |
| R06 | [#16](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/16) |
| R07 | [#11](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/11), [#12](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/12), [#13](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/13), [#14](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/14), [#15](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/15), [#17](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/17) |
| R08 | [#16](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/16), [#18](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/18) |
| R09 | [#1](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/1), [#3](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/3), [#4](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/4), [#5](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/5), [#9](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/9), [#19](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/19) |
| R10 | [#1](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/1), [#5](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/5), [#9](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/9), [#10](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/10), [#11](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/11), [#12](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/12), [#13](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/13), [#14](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/14), [#15](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/15), [#16](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/16), [#18](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/18), [#19](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/19) |
| R11 | [#1](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/1), [#2](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/2), [#3](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/3), [#5](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/5), [#6](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/6), [#7](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/7), [#8](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/8), [#9](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/9), [#12](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/12), [#17](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/17), [#19](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/19) |

## Evidências e atualização

Registrar referências concretas a arquivos, saídas, commits e execuções quando ocorrerem. Uma explicação do agente não comprova conclusão técnica. Código, consultas, decisões metodológicas e conteúdo analítico são produzidos por Bruno; a IA orienta e revisa conforme a política.

Atualizar o snapshot ao mudar estados, dependências ou evidências. Preservar o histórico pelo Git; não tratar esta exportação datada como sincronização automática com o Project. A submissão final deverá identificar seu commit completo e conter a exportação atualizada.
