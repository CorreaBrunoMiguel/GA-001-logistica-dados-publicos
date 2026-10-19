# GA-001-logistica-dados-publicos

Estudo de portfólio sobre os fluxos ferroviários de cargas dos snapshots ANTT/SIADE de 2024 e 2025, conforme a demanda GA-001. O fluxo contratado é arquivos originais → Python → PostgreSQL → SQL → resultados consumidos em Python.

Código, SQL, decisões técnicas, análises e conclusões são de **Bruno**. O agente de IA responde pela governança e orientação conforme a política publicada.

## Contrato e recursos

| Referência | Recurso |
| --- | --- |
| Contrato | [Demanda GA-001 / 1.0.0](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/demanda.md), commit 0143e0d4e1a3edf0c084656f9b956a101e24a942 |
| Avaliação | [Rubrica publicada](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/rubrica.md), por conformidade, sem nota |
| Dados | [Manifesto e hashes](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/manifesto.json); obtenção prevista na PREP-07 |
| Repositório | [GA-001-logistica-dados-publicos](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos) |
| Project | [Project 5](https://github.com/users/CorreaBrunoMiguel/projects/5), privado segundo confirmação de Bruno |
| Tarefas | [Issues](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues) e [inventário/exportação](docs/kanban/README.md) |

## Começar ou retomar

Leia [AGENTS.md](AGENTS.md), [estado da execução](docs/continuidade/estado.json) e [procedimento de continuidade](docs/continuidade/README.md). Consulte o remoto para identificar a referência atual antes de retomar a issue indicada.

Situação deste checkpoint: PREP-00 a PREP-04 concluídas; PREP-05 em andamento: SC_TECH escolhido e plano Conda aceito por Bruno, incluindo mudança de versão do Python; resultado e validação pendentes. Bruno confirmou sincronização local até o commit 548f8e1c29d07fa03e8693be677c2bc51e1f72fa; alterações de acompanhamento posteriores são identificadas pelo histórico remoto.

## Documentação e autoria

- [Organização de pastas e entregáveis](docs/estrutura.md).
- [Inventário inicial do ambiente](docs/ambiente.md).
- [Registro de decisões técnicas de Bruno](docs/decisoes-tecnicas.md).
- [Declaração de apoio da IA](docs/apoio-ia.md).
- [Cards completos e evidências](docs/kanban/cards.json).

As pastas técnicas estão vazias. A implementação e os resultados serão produzidos por Bruno nas respectivas tarefas. Dependências, configuração de exemplo e comandos reais de execução serão documentados a partir da preparação e implementação efetivamente realizadas.

A estrutura de pastas é uma convenção de organização; não altera requisitos, dados ou critérios do contrato. A submissão final deverá identificar um commit completo e a exportação atualizada dos cards.
