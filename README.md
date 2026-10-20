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

Situação deste checkpoint: PREP-00 a PREP-06 concluídas. SC_TECH com Python 3.13.9 e bibliotecas identificados; kernel e importações conferidos. Banco ga001_logistica, proprietário ga001_app e acessos por psql e Python confirmados por evidências de Bruno. [Dependências](environment.yml), [configuração de referência](.env.example) e [instruções de acesso](docs/postgresql.md) registradas; reconstrução integral ainda não executada. PREP-07 pronta para iniciar após sincronização local. A última sincronização comprovada permanece em 9da5f1a532194dcbb34bd5c50d448f75576d34ef; o teste Python atual teve código e saída enviados na conversa.

## Documentação e autoria

- [Organização de pastas e entregáveis](docs/estrutura.md).
- [Inventário inicial do ambiente](docs/ambiente.md).
- [Configuração e instruções PostgreSQL](docs/postgresql.md), com [referência não secreta](.env.example).
- [Registro de decisões técnicas de Bruno](docs/decisoes-tecnicas.md).
- [Declaração de apoio da IA](docs/apoio-ia.md).
- [Cards completos e evidências](docs/kanban/cards.json).

As pastas técnicas estão vazias. A implementação e os resultados serão produzidos por Bruno nas respectivas tarefas. As dependências da preparação estão em [environment.yml](environment.yml), com [instruções e limites de reconstrução](docs/ambiente.md). A configuração de referência do acesso PostgreSQL está documentada; carregamento da configuração e comandos do fluxo analítico serão implementados/documentados por Bruno nos respectivos cards.

A estrutura de pastas é uma convenção de organização; não altera requisitos, dados ou critérios do contrato. A submissão final deverá identificar um commit completo e a exportação atualizada dos cards.
