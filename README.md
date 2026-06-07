# SalesInsight PY
## Sobre o projeto
O SalesInsight PY é um pipeline completo de análise de dados de vendas desenvolvido em Python.
O sistema lê, limpa, transforma e visualiza um dataset de vendas, gerando métricas,
segmentações e projeções simples de tendência.
## O que o sistema analisa
- Receita total e volume de vendas por mês e trimestre
- Top produtos e categorias por receita
- Desempenho por região
- Segmentação de clientes por nível de gasto (Bronze, Prata, Ouro)
- Projeção simples de tendência para os próximos meses
- Exportação de relatórios em CSV e JSON
## Objetivo
Praticar os principais conceitos do Módulo 01 de IA para Análise Preditiva:
- Lógica de programação com Python
- Variáveis, tipos de dados e operadores
- Condicionais (if, elif, else) e repetição (for, while)
- Funções, parâmetros, retorno e funções lambda
- Funções de ordem superior (função que recebe função)
- Leitura e escrita de arquivos CSV e JSON
- Módulo datetime para manipulação de datas
- Expressões regulares com o módulo re
- Pandas: DataFrames, limpeza, groupby, filtros e transformações
- NumPy: arrays, operações vetorizadas, broadcasting, np.select
- Matplotlib e Seaborn: gráficos, customização e exportação em PNG
- Classes, construtores, atributos, métodos, herança e super()
- GitHub, branches, commits e GitFlow simplificado
- Kanban para organização do projeto

## Como executar
### No Google Colab (recomendado)
1. Faça upload do arquivo `salesinsight.py` e do `vendas.csv` para o Colab.
2. Execute: `!python salesinsight.py`
3. Ou cole o conteúdo diretamente em células de um notebook `.ipynb`.
### Localmente com VS Code
1. Instale o Python 3.10+ e o VS Code.
2. Instale as dependências: pip install pandas numpy matplotlib seaborn
3. Execute no terminal: python salesinsight.py

## Estrutura do projeto
salesinsight-py/
│
├── salesinsight.py # Pipeline principal
├── vendas.csv # Dataset de vendas (gerado pelo próprio código ou externo)
├── README.md # Este arquivo
└── outputs/
  ├── metricas_por_mes.csv
  ├── segmentacao_clientes.csv
  ├── estatisticas_gerais.json
└── graficos/
  ├── vendas_por_mes.png
  ├── top_produtos.png
  └── distribuicao_regioes.png
## Ferramentas utilizadas
- Python 3.10+
- Google Colab / VS Code
- Bibliotecas: pandas, numpy, matplotlib, seaborn, re, json, datetime, os, random
- GitHub + GitHub Desktop para versionamento
- Trello / GitHub Projects para Kanban
## Sobre var, let e const (Python equivalente)
Em Python, não existe a distinção entre `var`, `let` e `const` como no JavaScript.
Toda variável é declarada com simples atribuição. Por convenção, constantes são
escritas em MAIÚSCULAS (ex.: `CAMINHO_ARQUIVO = "vendas.csv"`).
Para simular imutabilidade real, pode-se usar tuplas no lugar de listas.
## Como a internet funciona (contexto do projeto)
Neste projeto, os dados são lidos de um arquivo local CSV. Em um cenário real de
produção, esses dados poderiam vir de uma API REST (ex.: uma requisição HTTP GET
para um servidor que retorna JSON). O cliente (seu script Python) faria a requisição,
o servidor processaria e retornaria os dados — seguindo a arquitetura cliente-servidor.
Bibliotecas como `requests` permitem consumir essas APIs diretamente no Python.
## Vídeo de demonstração
[Inserir link do Google Drive ou YouTube aqui]

## Autores
Projeto desenvolvido para a disciplina de IA para Analise Preditiva por Luis Gustavo da Silva, Acacia Rosar e Raphael Antonio dos Santos Pires.
