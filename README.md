# Localização de instalações capacitadas

Trabalho de GCC118 — Programação Matemática. A AED usa setores do Censo 2022 para caracterizar a demanda e preparar instâncias municipais. Quantidade e capacidades das instalações serão definidas na etapa de modelagem.

## Notebooks

- `AED_Brasil.ipynb`: inventário nacional e comparação entre UFs.
- `AED_UF.ipynb`: análise de uma UF; altere `codigo_uf`.
- `AED_Municipal.ipynb`: análise de um município; altere `codigo_municipio`.

## Executar

Com [uv](https://docs.astral.sh/uv/) instalado:

```bash
uv sync
uv run --with notebook jupyter notebook
```

Ao trocar o recorte, reinicie o kernel e execute todas as células. Os notebooks do Brasil, por UF e municipal não geram matrizes completas de distâncias.

## Dados e resultados

Coloque `BR_setores_CD2022.gpkg` e `Dicionario_de_dados_malha_agregados.xlsx` em `data/`. A base GPKG não é versionada devido ao tamanho. Fonte: [IBGE — Censo 2022](https://www.ibge.gov.br/estatisticas/sociais/trabalho/22827-censo-demografico-2022.html?edicao=41852&t=resultados).

As figuras são salvas em SVG em `outputs/`. Os arquivos de dados originais são preservados; registros repetidos são tratados antes de somar população.
