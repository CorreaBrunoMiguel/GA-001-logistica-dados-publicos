# Ambiente — inventário inicial (PREP-01)

**Projeto:** GA-001 / contrato 1.0.0.  
**Coleta:** 19/10/2026.  
**Evidência:** comandos executados por Bruno em sua máquina e saídas fornecidas nesta conversa.  
**Registro administrativo:** transcrição e organização pelo agente de IA; os comandos não foram executados pelo agente na máquina de Bruno.

## Sistema e ferramentas

| Componente | Valor informado |
| --- | --- |
| Sistema operacional | Linux Mint 21.3 (Virginia), base Ubuntu jammy |
| Bash | 5.1.16(1)-release, x86_64-pc-linux-gnu |
| Git | 2.34.1 |
| Conda | 24.11.3 |
| Ambiente Conda ativo | base |
| Python ativo | 3.12.7 |
| Executável Python | /home/bruno/anaconda3/bin/python |
| Cliente psql | 18.6 (Ubuntu 18.6-1.pgdg22.04+2) |
| Servidor PostgreSQL consultado | 14.24 (Ubuntu 14.24-1.pgdg22.04+2) |
| Disponibilidade local | /var/run/postgresql:5432 — aceitando conexões |

Ambientes Conda informados: base, SC_TECH e dados. O inventário se refere ao ambiente base; não representa um ambiente Python dedicado ao projeto.

## Pacotes Jupyter no ambiente ativo

| Pacote | Versão |
| --- | --- |
| IPython | 8.27.0 |
| ipykernel | 6.31.0 |
| ipywidgets | 8.1.8 |
| jupyter_client | 8.6.0 |
| jupyter_core | 5.7.2 |
| jupyter_server | 2.14.1 |
| jupyterlab | 4.2.5 |
| nbclient | 0.8.0 |
| nbconvert | 7.16.4 |
| nbformat | 5.10.4 |
| notebook | 7.2.2 |
| qtconsole | 5.7.0 |
| traitlets | 5.14.3 |

## Verificações fornecidas por Bruno

O inventário foi obtido com cat /etc/os-release, bash --version, git --version, conda --version, conda env list, command -v python, python --version, jupyter --version, psql --version e pg_isready.

A consulta inicial:

```bash
psql -X -d postgres -c "SHOW server_version;"
```

retornou FATAL: role "bruno" does not exist. O servidor respondeu, mas esse papel de banco não existe no destino consultado.

A consulta pela conta administrativa local:

```bash
sudo -u postgres psql -X -d postgres -c "SHOW server_version;"
```

retornou 14.24 (Ubuntu 14.24-1.pgdg22.04+2). Assim, versão do cliente e versão do servidor foram registradas separadamente. A consulta bem-sucedida demonstra acesso administrativo local ao banco postgres; não demonstra uma conexão Python nem o acesso próprio da aplicação.

## Conclusão do inventário

**PREP-01 concluída com evidência fornecida pelo participante.** Sistema, ferramentas, ambiente ativo, cliente e servidor PostgreSQL foram identificados; a lacuna de acesso pelo papel bruno foi registrada.

Permanecem em tarefas próprias a confirmação do clone local (PREP-02), a preparação do ambiente Python dedicado (PREP-05) e o destino e acesso PostgreSQL para o projeto, incluindo conexão pelo Python (PREP-06). Nenhuma dessas configurações é declarada concluída por este inventário.

Este arquivo é documentação administrativa. O conteúdo técnico da solução permanece de autoria de Bruno.
