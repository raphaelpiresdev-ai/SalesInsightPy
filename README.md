# SalesInsight PY

Pipeline de análise e visualização de dados de vendas desenvolvido em Python para o mini-projeto avaliativo do Módulo 01.

## Sobre o projeto

O SalesInsight PY é um pipeline completo de análise de dados de vendas. O sistema lê, inspeciona, limpa, transforma e visualiza um dataset de vendas, gerando métricas, segmentações, projeções simples de tendência e arquivos de saída em CSV, JSON e PNG.

O arquivo principal do projeto é o notebook `salesinsight.ipynb`.

## O que o sistema analisa

- Receita total e volume de vendas por mês.
- Top produtos e categorias por receita.
- Desempenho por região.
- Segmentação de clientes por nível de gasto: Bronze, Prata e Ouro.
- Estatísticas gerais de receita usando NumPy.
- Projeção simples de tendência para os próximos meses.
- Exportação de relatórios em CSV e JSON.
- Geração de visualizações em PNG.

## Objetivo

Praticar os principais conceitos do Módulo 01 de IA para Análise Preditiva:

- Lógica de programação com Python.
- Variáveis, tipos de dados e operadores.
- Condicionais `if`, `elif` e `else`.
- Estruturas de repetição.
- Funções, parâmetros e retorno.
- Funções lambda.
- Função de ordem superior, ou seja, função que recebe outra função como argumento.
- Leitura e escrita de arquivos CSV e JSON.
- Manipulação de datas.
- Expressões regulares com o módulo `re`.
- Pandas: DataFrames, limpeza, filtros, seleções, transformações e `groupby`.
- NumPy: arrays, operações vetorizadas, broadcasting e `np.select`.
- Matplotlib e Seaborn: gráficos, customização e exportação em PNG.
- Programação orientada a objetos com classes, construtores, atributos e métodos.
- Herança e uso de `super()`.
- GitHub, branches, commits e fluxo simplificado com `main`, `develop` e branches de funcionalidade.
- Kanban para organização do projeto.

## Como executar

### No Google Colab

1. Faça upload do arquivo `salesinsight.ipynb`.
2. Faça upload do arquivo `vendas.csv`.
3. Execute as células do notebook em ordem.

### Localmente com VS Code ou Jupyter

1. Instale Python 3.10 ou superior.
2. Instale as dependências:

```bash
pip install -r requirements.txt
```

3. Abra o arquivo `salesinsight.ipynb`.
4. Execute as células do notebook em ordem.

## Estrutura do projeto

```text
SalesInsightPy/
├── README.md
├── requirements.txt
├── salesinsight.ipynb
├── vendas.csv
├── gerar_csv.py
└── outputs/
    ├── relatorio_resumo.csv
    ├── relatorio_resumo.json
    └── graficos/
        ├── receita_por_mes.png
        ├── top_produtos.png
        └── distribuicao_regioes.png
```

## Arquivos principais

- `salesinsight.ipynb`: notebook principal do projeto, contendo o pipeline completo.
- `vendas.csv`: dataset de vendas utilizado na análise.
- `gerar_csv.py`: script auxiliar usado para gerar o dataset sintético `vendas.csv`.
- `requirements.txt`: lista de dependências necessárias para executar o projeto localmente.
- `outputs/relatorio_resumo.csv`: relatório resumido exportado em CSV.
- `outputs/relatorio_resumo.json`: relatório resumido exportado em JSON e lido novamente com `json.load()` para conferência.
- `outputs/graficos/receita_por_mes.png`: gráfico de linha com a receita mensal.
- `outputs/graficos/top_produtos.png`: gráfico de barras com os principais produtos por receita.
- `outputs/graficos/distribuicao_regioes.png`: gráfico adicional com a distribuição de receita por região.

## Pipeline implementado

O notebook executa as seguintes etapas:

1. Importação das bibliotecas.
2. Leitura do dataset `vendas.csv`.
3. Inspeção inicial dos dados.
4. Limpeza e tratamento:
   - remoção de espaços extras;
   - tratamento de valores nulos;
   - conversão de datas;
   - remoção de datas inválidas;
   - limpeza de strings com expressões regulares.
5. Criação de colunas derivadas:
   - `receita_total`;
   - `mes`;
   - `mes_nome`;
   - `trimestre`;
   - `ano`;
   - `faixa_receita_item`.
6. Cálculo de métricas agregadas com `groupby`.
7. Segmentação de clientes por gasto total.
8. Cálculos estatísticos com NumPy.
9. Geração e exportação de gráficos.
10. Organização do pipeline em classes.
11. Projeção simples de tendência.
12. Exportação dos resultados em CSV e JSON.

## Ferramentas utilizadas

- Python 3.10+
- VS Code / Jupyter Notebook / Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Módulos nativos: `os`, `json`, `re`, `datetime` e `random`
- GitHub e GitHub Desktop
- Jira para organização do Kanban

## Como a internet funciona no contexto do projeto

Neste projeto, os dados são lidos de um arquivo local CSV. Em um cenário real de produção, esses dados poderiam vir de uma API REST.

Nesse caso, o notebook Python atuaria como cliente, enviando uma requisição HTTP para um servidor. O servidor processaria a requisição e retornaria os dados, geralmente em JSON. Depois disso, o Python poderia transformar os dados em um DataFrame do Pandas para executar as mesmas etapas de limpeza, transformação, análise e visualização.

Essa comunicação segue a arquitetura cliente-servidor: o cliente solicita dados ou serviços, e o servidor responde.

## Organização e versionamento

O trabalho foi organizado em squad usando branches descritivas e Kanban.

- Repositório: [raphaelpiresdev-ai/SalesInsightPy](https://github.com/raphaelpiresdev-ai/SalesInsightPy)
- Kanban: [Jira - Board KAN](https://raphaelpiresdev.atlassian.net/jira/software/projects/KAN/boards/1)

Branches utilizadas:

- `main`
- `develop`
- `feat/leitura-limpeza`
- `feat/analise-metricas`
- `feat/visualizacoes`
- `feat/classes-poo`
- `docs/readme-video`

## Vídeo de demonstração

Link do vídeo: (https://possoliengenharia-my.sharepoint.com/:v:/g/personal/luis_possoli_com/IQBXp6zqzgIkSIR6PiJZPt_IAYk6lK7aHPtYHXlOLUYEhdo?e=ms2yrG)

## Autores

Projeto desenvolvido para a disciplina de IA para Análise Preditiva por:

- Luis Gustavo da Silva
- Acacia Rosar
- Raphael Antonio dos Santos Pires
