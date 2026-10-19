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

## SC_TECH — inspeção para reutilização

**Data:** 19/10/2026. **Fonte:** saídas executadas e fornecidas por Bruno. Escolha operacional: [DOP-001](decisoes-tecnicas.md).

| Componente | Versão informada |
| --- | --- |
| python | 3.13.14 |
| numpy | 2.5.1 |
| pandas | 3.0.5 |
| matplotlib | 3.11.1 |
| seaborn | 0.13.2 |
| jupyterlab | 4.6.2 |
| ipykernel | 7.3.0 |
| ipython | 9.16.1 |

Prefixo informado pelo Conda: /home/bruno/anaconda3/envs/SC_TECH. A maioria dos pacotes listados tem origem conda-forge; Seaborn foi listado como pypi. Não se generaliza essa origem a pacotes não mostrados.

pip check retornou **No broken requirements found.** Isso é verificação de dependências declaradas, não teste de importações nem de execução da solução.

| Kernel registrado | Diretório informado |
| --- | --- |
| dados | /home/bruno/.local/share/jupyter/kernels/dados |
| sc_tech | /home/bruno/.local/share/jupyter/kernels/sc_tech |
| python3 | /home/bruno/anaconda3/share/jupyter/kernels/python3 |

O registro sc_tech existe; o interpretador efetivamente usado por ele ainda será conferido. SQLAlchemy e Psycopg não apareceram no filtro de pacotes. O agente propôs acrescentá-los para a integração PostgreSQL, sem declarar essa proposta como requisito de biblioteca do contrato ou como instalação já realizada.

**PREP-05 permanece em andamento:** complementos, importações, ligação do kernel e dependências reproduzíveis ainda pendentes. A versão 3.12.7 no inventário inicial pertence ao base; o ambiente escolhido para avaliação é SC_TECH com Python 3.13.14, conforme a inspeção acima.

## SC_TECH — plano Conda aceito

**Data:** 19/10/2026. Bruno forneceu o plano do comando `conda install -n SC_TECH -c conda-forge --freeze-installed sqlalchemy psycopg` e informou que o aceitou, declarando não haver problema em alterar a versão do Python.

O plano prevê Python **3.13.14 → 3.13.9**, SQLAlchemy **2.1.5**, Psycopg e psycopg-c **3.3.4**, libpq **18.6** e download de **198,1 MB**. Também altera certificados, OpenSSL, Qt/PySide6, bibliotecas gráficas, MySQL e outras bibliotecas nativas. Esses valores descrevem o plano; não são um inventário posterior à instalação. A opção `--freeze-installed` não preservou integralmente o conjunto instalado neste plano.

A aceitação foi informada por Bruno; a saída final da transação ainda não foi fornecida. Conferir Python, pacotes e `pip check` após a transação, depois importações e interpretador do kernel. O inventário anterior permanece como registro histórico. Nenhuma instalação ou reversão foi executada pelo agente.

## SC_TECH — resultado posterior à instalação

**Data:** 19/10/2026. **Fonte:** três comandos executados por Bruno e saídas fornecidas na conversa; o agente não acessou a máquina.

| Componente | Versão após a instalação |
| --- | --- |
| python | 3.13.9 |
| numpy | 2.5.1 |
| pandas | 3.0.5 |
| matplotlib | 3.11.1 |
| seaborn | 0.13.2 |
| sqlalchemy | 2.1.5 |
| psycopg | 3.3.4 |
| psycopg-c | 3.3.4 |
| jupyterlab | 4.6.2 |
| ipykernel | 7.3.0 |

Prefixo informado: `/home/bruno/anaconda3/envs/SC_TECH`. Os pacotes acima foram listados como conda-forge, exceto Seaborn, listado como pypi.

`pip check` retornou **No broken requirements found.** As saídas demonstram os pacotes instalados e a versão efetiva do Python; não é preciso repetir a instalação ou exigir o log final da transação para reconhecer isso. O plano aceito e o inventário anterior permanecem como histórico.

**Situação após a instalação:** o interpretador do notebook e as dependências de reprodução foram registrados nas seções seguintes. As importações foram confirmadas explicitamente por Bruno na conclusão abaixo. A conexão PostgreSQL pertence à PREP-06.

## SC_TECH — interpretador do notebook confirmado

**Data:** 19/10/2026. **Fonte:** saídas fornecidas por Bruno.

Uma tentativa anterior foi executada no Python do `base` (`/home/bruno/anaconda3/bin/python`, 3.12.7) e retornou `ModuleNotFoundError: No module named 'psycopg'`. Essa tentativa não testou o SC_TECH. Após `conda activate SC_TECH`, o terminal mostrou o executável `/home/bruno/anaconda3/envs/SC_TECH/bin/python` e Python 3.13.9.

Após orientação para abrir JupyterLab, selecionar o kernel do SC_TECH e repetir as importações, Bruno forneceu:

```text
/home/bruno/anaconda3/envs/SC_TECH/bin/python 3.13.9 | packaged by conda-forge | (main, Oct 16 2025, 10:31:39) [GCC 14.3.0]
```

O interpretador efetivo do notebook está confirmado. Bruno confirmou posteriormente que todas as importações solicitadas foram executadas sem erro, incluindo Psycopg. Não repetir a instalação nem a identificação do interpretador.

## Dependências e reconstrução do ambiente

A IA preparou administrativamente [environment.yml](../environment.yml) a partir das versões fornecidas por Bruno. Ele declara Python, NumPy e pandas (manipulação e leitura), Matplotlib e Seaborn (visualização), SQLAlchemy (acesso SQL), Psycopg/psycopg-c (driver PostgreSQL), JupyterLab e ipykernel (interface e kernel). O Seaborn foi mantido na seção pip conforme o inventário; os demais pacotes versionados foram informados como conda-forge.

O arquivo registra o subconjunto usado na preparação do projeto, com versões diretas; não é uma exportação integral do SC_TECH nem um lock de dependências transitivas. O ambiente de trabalho escolhido por Bruno é SC_TECH.

Para reconstruir em uma instalação Conda separada ou em um nome ainda não existente, a partir da raiz do repositório:

```bash
conda env create --name ga001-repro --file environment.yml
conda activate ga001-repro
python -m pip check
jupyter lab
```

No JupyterLab, selecionar o kernel do ambiente reconstruído e conferir `sys.executable`, `sys.version` e as importações de NumPy, pandas, matplotlib.pyplot, Seaborn, SQLAlchemy e Psycopg. Caso a interface não exponha o kernel, registrá-lo a partir desse ambiente com `python -m ipykernel install --user --name ga001-repro --display-name "Python (ga001-repro)"` e selecioná-lo antes da conferência.

**Limite da evidência:** a reconstrução não foi executada. O arquivo e as instruções ficam disponíveis para a verificação de reprodução da entrega (T10); nenhuma nova instalação foi realizada ou solicitada agora. A PREP-05 está concluída após a confirmação explícita das importações no notebook atual.

## Conclusão da PREP-05

**Data:** 19/10/2026. Em 19/10/2026, Bruno confirmou explicitamente que todas as importações solicitadas no notebook executaram sem erro, incluindo Psycopg. NumPy, pandas, matplotlib.pyplot, Seaborn, SQLAlchemy e Psycopg verificados por relato do participante; interpretador identificado pelas saídas anteriores.

**PREP-05 concluída:** ambiente SC_TECH utilizável nas verificações realizadas, Python 3.13.9 e kernel identificados, pacotes e versões registrados, pip check sem dependências declaradas quebradas e especificação/instruções de reconstrução disponíveis. O agente organizou os registros administrativos; Bruno executou e confirmou os testes.

A conexão PostgreSQL será verificada na PREP-06. A reconstrução do ambiente ainda não foi executada. Antes da próxima etapa, sincronizar a cópia local com o remoto e conferir o estado Git.

## PostgreSQL — inventário para o acesso do projeto (PREP-06)

**Data:** 19/10/2026. **Fonte:** saídas de `sudo -u postgres psql -X -P pager=off -d postgres -c '\du' -c '\l'` executado por Bruno; registro administrativo da IA.

Foram listados três papéis e seis bancos. O papel postgres apresenta os atributos administrativos. Os nomes propostos para o projeto, `ga001_app` (papel) e `ga001_logistica` (banco), não aparecem nessas listagens. Não foi necessária alteração nos recursos existentes para realizar o inventário.

Próxima ação: criar e conferir `ga001_app`, com login e atributos NOSUPERUSER, NOCREATEDB e NOCREATEROLE; senha definida interativamente por Bruno com `createuser --pwprompt`. A proposta de configuração foi orientada pelo agente, e sua execução ainda não foi comprovada. O banco, seu proprietário, o destino final, a autenticação e a conexão Python serão conferidos nas ações seguintes. Modelagem das tabelas e carga pertencem aos cards técnicos.

Referência administrativa: [createuser — documentação PostgreSQL](https://www.postgresql.org/docs/18/app-createuser.html).
