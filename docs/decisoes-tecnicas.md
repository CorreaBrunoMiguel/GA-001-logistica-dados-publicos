# Decisões técnicas de Bruno

Estrutura administrativa preparada pelo agente de IA em 19/10/2026. O conteúdo das decisões e suas justificativas é de Bruno.

Nenhuma decisão metodológica, de modelagem, transformação, biblioteca ou interpretação é atribuída a Bruno sem seu registro. O inventário de ferramentas existentes está em [ambiente.md](ambiente.md); versões instaladas não são, por si só, decisões sobre a solução.

Ao registrar uma decisão, indicar:

- Identificador e data.
- Questão técnica e requisito relacionado.
- Alternativas consideradas.
- Escolha e justificativa de Bruno.
- Evidências e consequências observadas.
- Issue, arquivo ou commit correspondente.

O agente pode organizar a redação administrativa do registro a partir do raciocínio expresso por Bruno, preservando sua autoria e sem acrescentar justificativas ou resultados não fornecidos.

## Registros

### DOP-001 — Avaliar a reutilização do SC_TECH

- **Data:** 19/10/2026.
- **Natureza:** escolha operacional de ambiente; registro administrativo pelo agente a partir da manifestação de Bruno.
- **Escolha expressa por Bruno:** priorizar a avaliação do ambiente Conda existente SC_TECH para o projeto, com JupyterLab como interface.
- **Justificativa informada:** aproveitar bibliotecas já instaladas e evitar baixá-las novamente.
- **Alternativa considerada na conversa:** continuar a preparação do novo ga001. Bruno confirmou esse ambiente com Python 3.12.15 antes de solicitar a avaliação do SC_TECH.
- **Estado da decisão:** preferência definida e inventário inicial recebido; complementos, importações, ligação do kernel e dependências reproduzíveis ainda pendentes.
- **Evidências:** mensagens de Bruno e [PREP-05 / issue 6](https://github.com/CorreaBrunoMiguel/GA-001-logistica-dados-publicos/issues/6). A escolha do ambiente foi explícita; não se infere compatibilidade das versões.
- **Consequências verificadas:** Python 3.13.14 e pacotes de análise/Jupyter inventariados; pip check sem dependências quebradas declaradas; registro do kernel sc_tech encontrado. Não se infere funcionamento das importações ou ligação do kernel. O agente não instalou, atualizou ou removeu ambientes na máquina de Bruno.
- **Contrato relacionado:** R11; a demanda exige Python 3 e ambiente/dependências documentados, sem impor a criação de uma env nova.

**Complemento do registro:** o agente recomendou SQLAlchemy e Psycopg, ausentes da listagem filtrada, para a integração PostgreSQL. É proposta de preparação; a instalação e as versões efetivas ainda aguardam evidências de Bruno.
