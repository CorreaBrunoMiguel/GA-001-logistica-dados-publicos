# Dados — procedência e identidade dos snapshots

**Projeto/contrato:** GA-001 / 1.0.0. **Registro iniciado:** 20/10/2026. **Autoria administrativa:** IA; Bruno realiza a obtenção e as verificações locais.

## Referência fixa

- Commit contratado: 0143e0d4e1a3edf0c084656f9b956a101e24a942.
- [Manifesto](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/manifesto.json).
- [ZIP contratado](https://github.com/CorreaBrunoMiguel/gerador_analitico/blob/0143e0d4e1a3edf0c084656f9b956a101e24a942/projetos/GA-001-logistica-dados-publicos/versoes/1.0.0/dados/fontes-antt-siade-2024-2025.zip).

O repositório de origem é privado. Bruno deve usar o GitHub no navegador com acesso ao repositório, baixar o arquivo e preservá-lo como `data/raw/fontes-antt-siade-2024-2025.zip`.

## Valores esperados — ainda não verificados localmente

| Arquivo | Bytes esperados | SHA-256 esperado |
| --- | ---: | --- |
| fontes-antt-siade-2024-2025.zip | 264642 | 2a5d0b6c0dfaddca5d4415f76eda38a1f7fcca383a4de3a799412ffc713dbbfb |
| producao_origem_destino_2024.csv | 607661 | 5f596d970ca568679b1db2962f82b92b21e39ad9f6fe871137613d4dcf7a0673 |
| producao_origem_destino_2025.csv | 601420 | 265a40f1759fcb6af5a83d28b687d3621d8cf50054ae777f80e7cb0d9e863114 |

Os valores acima foram lidos no manifesto fixo pelo agente; não representam hashes calculados na máquina de Bruno.

A primeira conferência local será do ZIP, com `wc -c` e `sha256sum`. Extração e conferência dos dois CSVs ocorrerão depois, preservando os bytes originais. Nenhuma transformação ou leitura analítica foi realizada por esta orientação.

## Procedência e atribuição registradas no contrato

Publicador identificado documentalmente: Agência Nacional de Transportes Terrestres — ANTT, base SIADE (Produção Origem Destino 2024 e 2025). Os bytes contratados são os CSVs recebidos de Bruno em 19/10/2026, preservados por compactação reversível no ZIP desta versão.

- [Página da base ANTT/SIADE](https://dados.antt.gov.br/dataset/sistema-de-acompanhamento-do-desempenho-operacional-das-concessionarias-siade).
- [Recurso documental de 2024](https://dados.antt.gov.br/dataset/438a5184-09db-49a3-88c8-0bad418b4409/resource/c32ca914-0aa3-4282-b92a-6eb4200c5033).
- [Recurso documental de 2025](https://dados.antt.gov.br/dataset/438a5184-09db-49a3-88c8-0bad418b4409/resource/d7263808-bd77-4153-9910-49e041d73b21).

Conforme o manifesto, a licença indicada é Creative Commons Atribuição, com [referência do portal](https://opendefinition.org/licenses/cc-by/); a versão específica não foi identificada. Preservar atribuição à ANTT/SIADE e identificar futuras transformações.

**Limites de procedência:** data original do download não informada e sem confronto independente byte a byte com o servidor oficial. A identidade a conferir nesta execução é a do snapshot contratado; não se presume equivalência com revisões atuais do portal.

## Evidência local da PREP-07

- Obtenção do ZIP por Bruno: pendente de confirmação.
- Tamanho e SHA-256 do ZIP: pendentes de saída local.
- Extração e tamanhos/SHA-256 dos CSVs: pendentes.
- Data da obtenção e caminhos reais: registrar após a execução.

A PREP-07 permanece em andamento. A elaboração do diagnóstico e da análise pertence aos cards técnicos e a Bruno.
