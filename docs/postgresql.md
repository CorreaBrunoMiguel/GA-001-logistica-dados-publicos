# Acesso PostgreSQL — GA-001

Documentação administrativa produzida pela IA com base nos comandos e saídas fornecidos por Bruno. A implementação Python e SQL do fluxo analítico pertence a Bruno.

## Destino verificado

| Configuração de referência | Argumento Psycopg | Valor |
| --- | --- | --- |
| PGHOST | host | 127.0.0.1 |
| PGPORT | port | 5432 |
| PGDATABASE | dbname | ga001_logistica |
| PGUSER | user | ga001_app |

O banco pertence a ga001_app, usa UTF8 e localidade pt_BR.UTF-8. A conexão pelo psql foi demonstrada com Password Used true, Superuser off e TLSv1.3. Essas informações não substituem o teste no Python.

A amostra [.env.example](../.env.example) contém apenas valores não secretos. É uma referência para a configuração: o Python não carrega arquivos .env automaticamente, e nenhum carregador foi implementado pela IA. Nesta preparação, Bruno deve explicitar os parâmetros da conexão e solicitar a senha em tempo de execução. O carregamento da configuração do fluxo analítico será implementado por Bruno no card correspondente. O [.gitignore](../.gitignore) já exclui .env e outras configurações locais.

## Reconstruir em uma instalação nova

Conferir previamente os papéis e bancos existentes. Os comandos de criação abaixo se aplicam onde esses nomes ainda não existem. No ambiente atual de Bruno, papel e banco já estão confirmados; não repetir sua criação.

```bash
(cd /tmp && sudo -u postgres psql -X -P pager=off -d postgres -c '\du' -c '\l')
```

Criar papel com login e privilégios limitados; a senha é definida e confirmada interativamente:

```bash
(cd /tmp && sudo -u postgres createuser --login --no-superuser --no-createdb --no-createrole --pwprompt ga001_app)
```

Criar banco com o papel como proprietário:

```bash
(cd /tmp && sudo -u postgres createdb --owner=ga001_app ga001_logistica)
```

Conferir acesso e propriedade:

```bash
psql -X -P pager=off -h 127.0.0.1 -p 5432 -U ga001_app -d ga001_logistica -W -c '\conninfo' -c '\l ga001_logistica'
```

O acesso TCP local precisa estar permitido pela configuração PostgreSQL da instalação. No ambiente de Bruno, o teste acima já funcionou. As instruções não alteram o método de autenticação do servidor.

## Verificação Python a executar por Bruno

Usar o notebook com kernel SC_TECH, já conferido na PREP-05, e as dependências de [environment.yml](../environment.yml). A biblioteca getpass pertence à biblioteca padrão.

1. Solicitar a senha com getpass.getpass; a senha não deve ser literal da célula nem saída impressa.
2. Abrir psycopg.connect com os argumentos e valores da tabela e a senha obtida em tempo de execução.
3. Usar o gerenciador de contexto da conexão para fechá-la ao sair do bloco.
4. Exibir apenas as propriedades dbname, user, host e port do atributo info da conexão aberta.
5. Fornecer código sem senha e saída ou erro para revisão.

O agente fornece o objetivo e as referências; Bruno escreve e executa a célula. Nenhum código de teste Python ou da solução analítica foi produzido pela IA. Após o resultado, atualizar a evidência de conexão e os critérios da issue PREP-06.

## Referências

- [createuser](https://www.postgresql.org/docs/18/app-createuser.html).
- [createdb](https://www.postgresql.org/docs/18/app-createdb.html).
- [psql](https://www.postgresql.org/docs/18/app-psql.html).
- [Psycopg — conexão e contexto](https://www.psycopg.org/psycopg3/docs/api/connections.html).
- [Psycopg — propriedades da conexão](https://www.psycopg.org/psycopg3/docs/api/objects.html).
- [Python 3.13 — getpass](https://docs.python.org/3.13/library/getpass.html).
