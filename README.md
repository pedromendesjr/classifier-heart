# Projeto de Detecção de Doenças Cardíacas *(Heart Disease)* através de Machine Learning

### Pedro Lourenço Mendes Júnior - ds.pedromendes@gmail.com - [Acessar GitHub](https://github.com/pedromendesjr)

<img src='https://img.freepik.com/vetores-gratis/ilustracao-do-conceito-de-cardiologista_114360-6847.jpg?w=740&t=st=1687444617~exp=1687445217~hmac=564e0d5401d982c44da6a51f0eb9101fbd448b20a5ae2a61f689c63a53d1709a' alt='Ilustração do conceito de cardiologista' width='500' height='500' title="Image by rawpixel.com on Freepik">

## Introdução
No campo da saúde, a capacidade de prever e diagnosticar doenças de forma precisa desempenha um papel crucial no tratamento e na melhoria dos resultados para os pacientes. Com o avanço da tecnologia e o acesso a conjuntos de dados cada vez maiores, técnicas de Machine Learning têm se mostrado promissoras para auxiliar nesse processo. Neste projeto de estudos, utilizamos algoritmos de Decision Tree e Random Forest para prever casos de doença cardíaca, explorando técnicas de limpeza de dados, feature scaling, análise exploratória e validação cruzada.

A doença cardíaca é uma das principais causas de morbidade e mortalidade em todo o mundo. A capacidade de identificar corretamente os indivíduos com maior risco de desenvolver doença cardíaca pode ajudar na prevenção, no tratamento precoce e no acompanhamento adequado dos pacientes. Nesse contexto, o uso de técnicas de Machine Learning pode fornecer insights valiosos e contribuir para aprimorar os métodos tradicionais de diagnóstico.

## Objetivo
O objetivo principal deste projeto é utilizar algoritmos de Machine Learning para prever a presença de doenças cardíacas em indivíduos, proporcionando insights que possam auxiliar médicos e profissionais de saúde na tomada de decisões.

## Dicionário de Dados
Aqui estão as principais variáveis utilizadas na análise:

| Variável           | Descrição                                                                                      |
|--------------------|------------------------------------------------------------------------------------------------|
| `age`              | Idade do paciente                                                                              |
| `sex`              | Sexo do paciente                                                                               |
| `cp`               | Tipo de dor no peito (4 valores)                                                               |
| `trestbps`         | Pressão arterial em repouso                                                                     |
| `chol`             | Nível de colesterol sérico                                                                     |
| `fbs`              | Glicemia em jejum > 120 mg/dl (1 = verdadeiro; 0 = falso)                                       |
| `restecg`          | Resultados do eletrocardiograma em repouso (0, 1, 2)                                            |
| `thalach`          | Frequência cardíaca máxima atingida                                                            |
| `exang`            | Angina induzida por exercício (1 = sim; 0 = não)                                                |
| `oldpeak`          | Depressão do segmento ST induzida por exercício relativo ao repouso                            |
| `slope`            | Inclinação do segmento ST do pico do exercício                                                 |
| `ca`               | Número de vasos principais (0-3) coloridos por fluoroscopia                                    |
| `thal`             | Talassemia (3 = normal; 6 = fixed defect; 7 = reversible defect)                               |
| `target`           | Variável alvo (1 = doença cardíaca presente; 0 = doença cardíaca ausente)                      |

## Dados
Os dados utilizados neste projeto foram obtidos a partir do repositório [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+disease), uma fonte confiável de dados de saúde. O conjunto de dados contém informações sobre pacientes que podem ou não ter doenças cardíacas.

## Principais Análises e Resultados

### 1. Importância das Features
![Importância das Features](https://github.com/pedromendesjr/classifier-heart/blob/main/imagens/features.png)

A tabela mostra a importância das features no modelo Random Forest. A `ST_Slope`, `ChestPainType` e `Cholesterol` são as features mais importantes na previsão de doenças cardíacas.

### 2. Distribuição da Idade dos Pacientes
![Distribuição da Idade](https://github.com/pedromendesjr/classifier-heart/blob/main/imagens/grafico_idade.png)

O histograma mostra a distribuição da idade dos pacientes, segmentada pela presença de doença cardíaca. Indivíduos entre 50 e 60 anos são os mais propensos a ter doenças cardíacas.

### 3. Matriz de Confusão
![Matriz de Confusão](https://github.com/pedromendesjr/classifier-heart/blob/main/imagens/matriz_confusao.png)

A matriz de confusão para o modelo Random Forest mostra uma acurácia de 86%, com um bom equilíbrio entre verdadeiros positivos e negativos. O modelo tem uma alta taxa de recall de 91%.

### 4. Matriz de Correlação
![Matriz de Correlação](https://github.com/pedromendesjr/classifier-heart/blob/main/imagens/matriz_correlacao.png)

A matriz de correlação mostra a relação entre as variáveis. A `ST_Slope`, `ChestPainType` e `Oldpeak` têm alta correlação com a presença de doenças cardíacas.

## Conclusão
Neste projeto, utilizamos técnicas de Machine Learning para prever a presença de doenças cardíacas, aplicando os algoritmos Decision Tree e Random Forest. O processo incluiu:

1. **Cross Validation**: Utilizada para validar a robustez dos modelos e evitar overfitting. Dividimos os dados em várias partes e treinamos/testamos o modelo várias vezes para garantir que os resultados são consistentes.
   
2. **Decision Tree**: Aplicado como um modelo inicial devido à sua simplicidade e facilidade de interpretação. Embora útil, o Decision Tree pode sofrer de overfitting, o que nos levou a explorar modelos mais complexos.

3. **Random Forest**: Este modelo combina várias árvores de decisão para melhorar a precisão e controlar o overfitting. O Random Forest se mostrou superior, com uma acurácia de 86%, precisão de 84%, recall de 91% e AUC ROC de 85.6%.

Esses resultados destacam a eficácia do uso de algoritmos de ensemble como o Random Forest em problemas de classificação médica, proporcionando insights valiosos que podem auxiliar no diagnóstico precoce e tratamento de doenças cardíacas.
