# Checkpoint 5 — Wines: Análise Estatística e Clusterização com K-means

Trabalho do 2º semestre do Tecnólogo em Inteligência Artificial (FIAP), integrando as disciplinas
**Statistical Computing with R & Python** e **Machine Learning & Modelling**.

## Integrantes

| Nome | RM |
|---|---|
| Adalberto Alves Cruz | 574115 |
| Bruno Henrique Ferreira Ambrosio | 571218 |
| Gustavo da Silva Nascimento | 570821 |
| Lucas Maximo dos Santos | 569714 |
| Renan de Assis Rodrigues | 574049 |
| Tiago Thomaz Cesaro | 569374 |

## Dataset

[Wine Dataset for Clustering](https://www.kaggle.com/datasets/harrywang/wine-dataset-for-clustering) (Kaggle): 178 vinhos e 13 variáveis químicas contínuas, sem valores nulos.

## Conteúdo do notebook

**Parte 1 — Statistical Computing** (variáveis `Alcohol` e `Malic_Acid`)
- Tabela de distribuição de frequências (regra de Sturges), histograma e boxplot
- Medidas de tendência central, dispersão e quartis, com detecção de outliers
- Distribuição Normal aplicada ao teor alcoólico, teste de Shapiro-Wilk e cálculos probabilísticos comparando valores teóricos e observados

**Parte 2 — Machine Learning**
- Pré-processamento: verificação de colunas de classe, nulos, duplicatas e padronização (StandardScaler)
- Escolha do número de grupos pelos métodos Elbow e Silhouette Score
- Ajuste do K-means, visualização com PCA e perfil químico de cada grupo

## Resultados

Os métodos Elbow e Silhouette indicaram **k = 3** (Silhouette = 0,285).

| Grupo | Vinhos | Álcool médio | Ácido málico | Perfil |
|---|---|---|---|---|
| 1 | 65 | 12,25% | 1,90 g/L | Leves, cor clara, menor teor de prolina |
| 2 | 51 | 13,13% | 3,31 g/L | Mais ácidos, cor intensa, poucos flavonoides |
| 3 | 62 | 13,68% | 2,00 g/L | Mais alcoólicos, ricos em prolina e fenóis |

## Como executar

1. Abra o `CP5_Wines_Grupo.ipynb` no Google Colab ou no Jupyter.
2. Deixe o `wine-clustering.csv` na mesma pasta. Se o arquivo não for encontrado, o notebook baixa os dados automaticamente.
3. Execute todas as células em ordem.

Bibliotecas: pandas, numpy, matplotlib, seaborn, scipy e scikit-learn (todas já vêm instaladas no Colab).
