# Estatística Descritiva e Exploratória (EDA) com o dataset Tips

Atividade prática da disciplina de Estatística do 3º período de Análise e Desenvolvimento de Sistemas (ADS) na Cesar School. O trabalho aplica, em Python, os principais conceitos de estatística descritiva e análise exploratória de dados sobre o dataset `tips`, que registra contas e gorjetas de um restaurante.

## Objetivo

Carregar, inspecionar e interpretar um conjunto de dados real, combinando cálculo de métricas, visualizações e análise escrita dos resultados.

## Dataset

- **Fonte:** dataset `tips`, disponível na biblioteca [seaborn](https://seaborn.pydata.org/).
- **Tamanho:** 244 registros e 7 colunas, sem valores nulos.
- **Variáveis numéricas:** `total_bill` (valor da conta), `tip` (gorjeta) e `size` (tamanho da mesa).
- **Variáveis categóricas:** `sex`, `smoker`, `day` e `time`.

## O que foi feito

| Etapa | Técnicas |
|---|---|
| 1. Exploração inicial | `head()`, `info()`, `shape` |
| 2. Tendência central e dispersão | Média, mediana, desvio padrão, variância e coeficiente de variação |
| 3. Quartis e outliers | Q1, Q2, Q3, IQR e limites de 1,5 × IQR |
| 4. Forma da distribuição | Assimetria (skewness) e curtose |
| 5. Correlação | Matriz de correlação e mapa de calor |
| 6. Visualização | Histogramas com KDE e boxplots |
| 7. Normalização | Min-Max e StandardScaler (Z-score), com discussão sobre o RobustScaler |

Cada etapa contém o código e uma análise escrita interpretando os resultados no contexto de um restaurante.

## Principais resultados

- `total_bill` tem média de 19,79 e mediana de 17,80, com desvio padrão de 8,90. A média acima da mediana indica assimetria positiva (1,13).
- Pelo critério do IQR (10,78), foram encontrados 9 outliers em `total_bill`, todos acima do limite superior de 40,30. O limite inferior é negativo (-2,82), então não há outliers abaixo dele.
- `tip` e `size` também têm assimetria positiva (1,46 e 1,44), e as três variáveis têm curtose em excesso positiva, ou seja, caudas mais pesadas que a de uma distribuição normal.
- A correlação mais forte é entre `total_bill` e `tip` (0,68), seguida de `tip` e `size` (0,49). Todas as correlações são positivas.
- Para normalizar `total_bill`, que tem outliers, a análise discute o `RobustScaler` como alternativa mais resistente que o Min-Max e o Z-score.

## Tecnologias

- Python
- pandas
- seaborn
- matplotlib
- scipy
- scikit-learn
- Jupyter Notebook / Google Colab

## Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/Joanna-Farias/Analise-Exploratoria-Pratica-Estatistica.git
   cd Analise-Exploratoria-Pratica-Estatistica 
   ```
2. Instale as dependências:
   ```bash
   pip install pandas seaborn matplotlib scipy scikit-learn jupyter
   ```
3. Abra o notebook:
   ```bash
   jupyter notebook Atividade_estatística_descritiva.ipynb
   ```

Também é possível abrir o arquivo `.ipynb` diretamente no Google Colab. O dataset é baixado automaticamente por `sns.load_dataset('tips')`, então é necessário ter conexão com a internet.

## Estrutura do repositório

```
├── Atividade_estatística_descritiva.ipynb   # Código, gráficos e análises
└── README.md
```

## Créditos

O enunciado e a estrutura dos exercícios foram propostos pela disciplina de Estatística (ADS, Cesar School). O código e as análises escritas foram desenvolvidos por mim.

## Autor

**[Seu nome]**
Estudante de Análise e Desenvolvimento de Sistemas, Cesar School
[LinkedIn] · [E-mail]