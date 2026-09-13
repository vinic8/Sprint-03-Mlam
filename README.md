# Challenge Sprint 3 — Estatística, Probabilidade e Regressão Linear

Projeto desenvolvido para o Challenge Sprint 3, com foco na aplicação de conceitos de Estatística, Probabilidade e Regressão Linear utilizando Python e técnicas introdutórias de Machine Learning.

## Sobre o projeto

O projeto utiliza um conjunto de dados diário referente ao ano de 2015, contendo 365 registros. A base apresenta informações relacionadas à temperatura, chuva, dias de fim de semana e consumo.

O objetivo principal é utilizar esses dados para realizar análises estatísticas e probabilísticas e, posteriormente, aplicar um modelo de Regressão Linear para analisar a relação entre a temperatura média e o consumo.

## Base de dados

O projeto utiliza o arquivo:

```
consumo.csv
```

A base possui 365 registros e 7 variáveis:

| Variável | Descrição |
|---|---|
| `data` | Data do registro |
| `temp_media` | Temperatura média diária em °C |
| `temp_min` | Temperatura mínima diária em °C |
| `temp_max` | Temperatura máxima diária em °C |
| `chuva` | Volume de chuva em mm |
| `fds` | Indicador de fim de semana |
| `consumo` | Consumo diário |

Não foram encontrados valores ausentes na base, e as variáveis numéricas já estavam em formatos adequados para as análises.

## Tecnologias utilizadas

- Python
- Pandas
- NumPy
- SciPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook / Google Colab

As principais bibliotecas utilizadas no projeto são `pandas`, `numpy`, `scipy`, `scikit-learn` e `matplotlib`.

## Análises realizadas

### 1. Probabilidade acima da mediana

A primeira análise utiliza a variável `consumo`.

Foram calculados:

- **Média:** 25.401,37
- **Mediana:** 24.867,00
- **Desvio-padrão:** 4.399,14

A partir da distribuição Normal ajustada aos dados, foi calculada a probabilidade de o consumo diário ser maior que a mediana.

**Resultado:**

```
P(consumo > mediana) = 54,83%
```

De acordo com a classificação utilizada no projeto, esse evento é considerado **provável**.

### 2. Probabilidade no intervalo média ± 2 desvios-padrão

A segunda análise calcula a probabilidade de o consumo estar dentro do intervalo:

```
média − 2σ ≤ consumo ≤ média + 2σ
```

Os limites encontrados foram:

- **Limite inferior:** 16.603,08
- **Limite superior:** 34.199,65

A probabilidade calculada foi:

```
95,45%
```

Esse resultado é compatível com a regra empírica da distribuição Normal, segundo a qual aproximadamente 95% dos valores estão dentro de dois desvios-padrão da média.

O evento foi classificado como **quase certo**.

### 3. Regressão Linear

Na terceira etapa foi aplicado um modelo de Regressão Linear utilizando:

- **Variável explicativa (X):** `temp_media`
- **Variável resposta (Y):** `consumo`

A hipótese analisada foi que dias com temperaturas médias maiores tendem a apresentar maior consumo.

#### Resultados

O modelo encontrado foi:

```
consumo = 8528,91 + 794,88 × temp_media
```

Principais resultados:

| Métrica | Resultado |
|---|---|
| Coeficiente angular | 794,88 |
| Intercepto | 8.528,91 |
| R² | 0,3302 |
| Correlação de Pearson | 0,5746 |

O coeficiente angular positivo indica que, segundo o modelo, um aumento de 1°C na temperatura média está associado a um aumento estimado de aproximadamente 795 unidades no consumo.

O valor de R² = 0,3302 indica que aproximadamente 33% da variação do consumo é explicada pela temperatura média nesse modelo.

A correlação de r = 0,5746 indica uma relação linear positiva e moderada entre temperatura média e consumo.

## Visualizações

O projeto também gera gráficos para facilitar a interpretação dos resultados, incluindo:

- Distribuição Normal do consumo e probabilidade acima da mediana;
- Distribuição Normal com o intervalo média ± 2 desvios-padrão;
- Gráfico de dispersão entre temperatura média e consumo;
- Reta de Regressão Linear ajustada aos dados.

## Relação com Machine Learning

As análises realizadas demonstram como conceitos estatísticos podem ser utilizados como base para Machine Learning.

A média, mediana e o desvio-padrão ajudam na compreensão e preparação dos dados. A distribuição Normal pode ser utilizada para analisar probabilidades e identificar valores que estejam fora de determinados intervalos.

A Regressão Linear representa uma introdução aos modelos de aprendizado supervisionado. Neste projeto, foi utilizada apenas uma variável explicativa, a temperatura média.

O resultado de R² aproximadamente igual a 0,33 mostra que a temperatura possui relação com o consumo, mas não explica sozinha todo o comportamento da variável.

Em uma aplicação futura, poderiam ser utilizadas outras variáveis disponíveis na base, como:

- Temperatura mínima;
- Temperatura máxima;
- Volume de chuva;
- Indicador de fim de semana.

A utilização de múltiplas variáveis poderia permitir a construção de um modelo mais completo para explicar e prever o consumo.

## Conclusão

A análise realizada mostrou que o consumo diário apresenta comportamento compatível com a distribuição Normal utilizada no projeto, apresentando uma média de aproximadamente 25.401 unidades e desvio-padrão de aproximadamente 4.399 unidades.

A probabilidade de o consumo estar acima da mediana foi de 54,83%, sendo classificada como provável. Já a probabilidade de o consumo estar dentro do intervalo de média ± 2 desvios-padrão foi de 95,45%, sendo classificada como quase certa.

Na Regressão Linear, foi identificada uma relação positiva e moderada entre temperatura média e consumo. Entretanto, o R² de aproximadamente 0,33 demonstra que somente a temperatura não é suficiente para explicar grande parte da variação do consumo.

Dessa forma, o projeto demonstra na prática a importância da Estatística para compreender dados e construir modelos iniciais de Machine Learning.

## Estrutura do projeto

```
Challenge-Sprint-3/
│
├── challenge_sprint3-MLAM.ipynb
├── consumo.csv
└── README.md
```

## Integrantes

-Vinicius Molena - RM 571270
Ricardo Algazi - RM 569600


##Video demostrativo
[Assista ao vídeo](https://youtu.be/PDGPYVY2vO0)
