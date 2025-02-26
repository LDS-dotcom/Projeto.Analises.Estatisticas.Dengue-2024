# Projeto.Analises.Estatisticas.Dengue-2024 <br>
<br>
<br>
# Sumário

 [Objetivo](#objetivo)
- [Fonte dos Dados](#fonte-dos-dados)
- [Desenvolvimento](#desenvolvimento)
- [Metodologia](#metodologia)
  - [Ferramentas](#ferramentas)
  - [Linguagem de Progração e Bibliotecas utilizadas](#linguagem-de-programacao-e-bibliotecas-utilizadas)
  - [Exploração Inicial](#exploracao-inicial)
  - [Estrutura do Dataset](#estrutura-do-dataset)
  - [Limpeza dos Dados](#limpeza-dos-dados)
- [Técnicas Estatísticas Utilizadas](#tecnicas-estatisticas-utilizadas)
- [Análise dos Dados](#analise-dos-dados)
   - [O que descobrimos?](#o-que-descobrimos)
   - [Recomendações](#recomendacoes)
   - [Plano de Ação](#plano-de-acao)
 






<br>
<br>
<br>

# Objetivo


Este projeto foi desenvolvido com o objetivo de analisar a distribuição dos casos de dengue no Brasil em 2024, utilizando técnicas de estatística descritiva e visualização de dados. A motivação para essa análise surge do crescente número de casos registrados no país, tornando essencial a compreensão dos padrões epidemiológicos para embasar políticas públicas de prevenção e combate à doença. 
Os dados utilizados neste projeto foram extraídos do site Kaggle, contendo 
informações relevantes como o ID da notificação, sexo, idade, data da notificação, região, UF, estado e município. O dataset foi processado e limpo para garantir a integridade das análises

<br>
<br>

# Fonte dos Dados

Os dados utilizados neste projeto foram extraídos do site Kaggle, uma plataforma reconhecida por fornecer datasets variados e confiáveis. O dataset específico utilizado contém informações sobre notificações de casos de dengue no Brasil no ano de 2024


<br>
<br>
<br>


# Desenvolvimento

- Coleta e Importação dos Dados: Importação do dataset no formato CSV.
-	Limpeza e Tratamento: Exclusão de colunas desnecessárias, remoção de 
valores ausentes (NaN). 
-	Análise Exploratória: Cálculo de estatísticas descritivas (média, mediana, 
desvio padrão) e visualização da distribuição dos casos por faixa etária, sexo e localização geográfica. 
-	Identificação de Padrões: Análise da distribuição temporal dos casos, 
incluindo séries temporais por mês e ano.
- Testes Estatísticos: Aplicação do teste qui-quadrado para verificar se há 
diferença significativa na incidência de dengue entre diferentes faixas etárias e sexos.
- Visualização: Geração de gráficos de barras, histogramas e heatmaps para 
ilustrar as tendências identificadas. 


<br>
<br>
<br>





# Metodologia

A estrutura do trabalho inclui a coleta e preparação do conjunto de 
dados, a análise exploratória com estatísticas descritivas e visualização gráfica, a aplicação de testes estatísticos para verificar a existência de padrões significativos e, por fim, a discussão dos resultados obtidos.  


## Ferramentas

| Ferramentas |         Propósito                                        |
| ------------|----------------------------------------------------------|
| Python      | Para limpeza, testes estatísticos e análises             |
| GitHub	    | Hospedar o projeto                                       |


<br>
<br>

## Bibliotecas utilizadas

- Pandas
-	Numpy
-	Matplotlib
-	Seaborn
-	Scipy
-	Statistics



<br>
<br>
<br>


## Estrutura do dataset

 O dataset é composto pelas seguintes colunas: 
- ID da Notificação: Identificação única de cada notificação
- Sexo: Indica o sexo da pessoa infectada (F para feminino, M para masculino).
- Idade: Idade da pessoa infectada.
- Região: Região geográfica do Brasil onde a notificação foi registrada.
- UF: Unidade Federativa (Estado) onde a notificação foi registrada.
- Município: Município onde a notificação foi registrada. 

<br>
<br>
<br>

## Exploração Inicial


Durante a exploração inicial dos dados, foram realizadas análises básicas, como o cálculo de estatísticas descritivas (média, mediana, desvio padrão) e a geração de gráficos para visualizar a distribuição dos casos de dengue por faixa etária, sexo e localização geográfica.

imagem

<br>
<br>
<br>



## Limpeza dos Dados

O pré-processamento dos dados inclui: 
- Remoção de valores nulos (NaN) para garantir a integridade das análises.
- Exclusão de colunas que não são relevantes para as análises propostas. 



<br>
<br>
<br>


# Técnicas Estatísticas Utilizadas

## Estatística Descritiva 

No projeto, foi realizada uma análise descritiva dos dados coletados para entender melhor a distribuição dos casos de dengue. As estatísticas descritivas fornecem um resumo dos dados e ajudam a identificar padrões e tendências significativas. Abaixo estão os cálculos das estatísticas descritivas realizadas: 


imagem

<br>


# Testes Estatísticos  
## Teste t de Student 

O teste t de Student é uma ferramenta estatística utilizada para comparar as 
médias de dois grupos e verificar se há uma diferença significativa entre eles. Neste caso estamos comparando a média das idades dos homens e das mulheres infectados com dengue. 

- Estatística t (t-stat): -34.22
  
Este valor indica a diferença entre as médias dos dois grupos em termos de 
unidades de erro padrão. Um valor negativo indica que a média do primeiro grupo 
(homens) é menor que a do segundo grupo (mulheres). 

- p-valor (p-value):4.71e-256 (ou seja, 0.000...471, um número extremamente 
pequeno)

O p-valor nos diz a probabilidade de observar uma diferença tão extrema entre 
as médias, ou mais extrema, se a hipótese nula (de que não há diferença real entre os grupos) for verdadeira. 
Um p-valor tão pequeno (quase zero) indica que é extremamente improvável 
que a diferença observada seja devida ao acaso. 
Ou seja, entre Hipótese Nula (H0H_0), onde não há diferença significativa entre as médias das idades dos homens e das mulheres, e Hipótese Alternativa (H1H_1), onde há uma diferença significativa entre as médias das idades dos homens e das mulheres, rejeitamos a Hipótese Nula.

Como o p-valor é muito pequeno, menor que qualquer nível de significância 
comum (como 0.05 ou 0.01), rejeitamos a hipótese nula. Isso significa que há uma diferença estatisticamente significativa entre as médias das idades dos homens e das mulheres.

<br>


## Teste Qui-Quadrado

A aplicação do teste qui-quadrado é para verificar se há uma diferença significativa na 
incidência de dengue entre diferentes faixas etárias e sexos. 

imagem

- Chi-Quadrado (χ2): 653.38 
- p-valor: 4.35e-127 (0.000...435, um valor extremamente pequeno) 

Ou seja, rejeitamos a Hipótese Nula. Um p-valor extremamente pequeno, 
sugere que a distribuição de casos de dengue por faixa etária está associada ao sexo dos infectados. 

<br>
<br>

## Códigos Python

<br>

```python

# Limpeza dos dados retirando NaN e coluna DATA

import pandas as pd
import numpy as np
import scipy.stats as stats
import matplotlib.pyplot as plt
import seaborn as sns


dt_dengue = pd.read_csv('Dengue_2024_final.csv')
dt_dengue = dt_dengue.dropna()
dt_dengue = dt_dengue.drop('DATA', axis=1)
print(dt_dengue.isnull().sum())
```


# Análise dos Dados

## O que eu descobri?

### Distribuição das Idades 

A análise da distribuição das idades das pessoas infectadas mostrou uma 
variação significativa entre as diferentes faixas etárias. 
De 21-30 anos apresenta o maior número de casos de dengue, seguida pelas 
faixas de 31-40 e 41-50 anos. Isso sugere que adultos jovens e de meia-idade são os mais afetados. As faixas etárias extremas, ou seja, os muito jovens (0-10 anos) e os muito idosos (81-90 e 91-100 anos), têm menos casos de dengue. Isso pode indicar maior proteção ou menos exposição a fatores de risco, ou pode refletir práticas de prevenção mais rigorosas para esses grupos.


 imagem

 Observa-se um declínio geral no número de casos conforme a idade avança, 
especialmente após os 60 anos. Isso pode ser devido a vários fatores, incluindo mudanças no comportamento de exposição, imunidade adquirida ao longo do tempo, ou diferenças na vigilância e notificação. 

<br>
<br>

### Diferença Entre Gêneros

O número de casos entre mulheres (F) é maior (128.779 casos) comparado ao 
número de casos entre homens (M) (106.873 casos). Isso sugere que a dengue pode estar afetando mulheres em uma proporção maior que homens. 
Há uma pequena quantidade de casos onde o sexo não foi identificado ou é 
indeterminado (I), totalizando 465 casos. Esse número é relativamente pequeno 
comparado ao total, mas ainda é importante para assegurar a qualidade e a 
completude dos dados.


imagem


A diferença na incidência entre homens e mulheres pode ser atribuída a fatores biológicos, comportamentais ou sociais. Por exemplo, mulheres podem ter mais interação com ambientes domésticos onde o mosquito Aedes aegypti tende a proliferar. A maior incidência em mulheres pode impactar de forma diferente o sistema de saúde, especialmente considerando questões de saúde reprodutiva e cuidados infantis, onde a presença feminina é mais forte.


<br>
<br>

### Distribuição Geográfica 

imagem


- A região Sudeste apresenta o maior número de casos, com 135.037 
notificações. Isso pode ser atribuído à alta densidade populacional, maior 
urbanização e condições climáticas que favorecem a proliferação do mosquito 
Aedes aegypti. 
- A região Centro-Oeste é a segunda mais afetada, com 48.319 casos. Esta 
região possui características que favorecem o desenvolvimento do mosquito, 
como temperaturas altas e períodos de chuva. 
- A região Sul, com 38.196 casos, também apresenta um número significativo de 
notificações. Embora a região tenha um clima mais temperado, os verões 
quentes e úmidos podem favorecer surtos de dengue. 
- A região Norte registra 8.918 casos. Apesar das condições climáticas 
favoráveis à proliferação do mosquito, a menor densidade populacional em 
algumas áreas pode contribuir para o menor número de casos. 
- A região Nordeste é a menos afetada, com 5.647 casos. Essa distribuição pode estar associada a fatores socioeconômicos, diferentes estratégias de controle do mosquito e possíveis variações na notificação dos casos. 

<br>
<br>



### Correlação Entre Variáveis

imagem

A dengue afeta pessoas de todas as idades, mas a maior concentração de 
casos está em adultos jovens e de meia-idade (20 a 50 anos). As regiões apresentam padrões semelhantes de distribuição etária, o que pode indicar que fatores ambientais e sociais influenciam a transmissão da dengue de maneira semelhante em todo o Brasil. O grande número de outliers sugere que há casos extremos (provavelmente idosos), o que pode ser relevante para políticas de saúde pública focadas em grupos mais vulneráveis. 


## Recomendações


Com base nessas descobertas, sugerimos as seguintes ações: 
- Campanhas de Conscientização Focadas: - 
Desenvolver campanhas educativas específicas para adultos jovens e de 
meia-idade, especialmente em áreas urbanas densamente povoadas. 
- Programas de Prevenção Direcionados: - 
Implementar estratégias de prevenção direcionadas a mulheres, 
especialmente em áreas onde elas são mais afetadas. 
- Fortalecimento da Vigilância: - 
Aumentar a vigilância epidemiológica nas regiões Sudeste e Centro-Oeste 
para permitir uma resposta rápida e eficaz aos surtos de dengue. 
- Análises Regionais Detalhadas: - 
Conduzir análises adicionais para investigar as diferenças regionais e 
entender melhor os fatores subjacentes que contribuem para a distribuição 
dos casos. 
- Educação Comunitária: - 
Envolver as comunidades locais em programas de educação e prevenção 
para eliminar criadouros do mosquito Aedes aegypti.



<br>
<br>


## Plano de ação


Com base nas análises e descobertas feitas ao longo do estudo, propomos um 
conjunto de ações específicas para combater a dengue no Brasil. Estas ações são direcionadas a diferentes níveis de intervenção, desde campanhas educativas até melhorias nas 
infraestruturas de saúde. O objetivo é implementar medidas eficazes e adaptadas às necessidades específicas de cada grupo populacional e região. 

Campanhas Educativas:

- Foco em Adultos Jovens e de Meia-Idade 
Objetivo: Reduzir a incidência de dengue entre adultos jovens (21-30 anos) e  
de meia-idade (31-50 anos), que apresentam o maior número de casos. 
Ações: Desenvolver materiais educativos específicos para esses grupos, 
enfatizando a importância de medidas preventivas. Utilizar mídias sociais, 
aplicativos móveis e campanhas publicitárias para alcançar um público amplo e 
diversificado.

- Foco em Mulheres 
Objetivo: Reduzir a maior incidência de dengue entre mulheres. 
Ações: Implementar programas de conscientização em comunidades e locais 
de trabalho onde a presença feminina é maior. Promover workshops e 
seminários voltados para a saúde da mulher, destacando a prevenção da 
dengue. 

Programas de Prevenção e Controle:

- Fortalecimento da Vigilância Epidemiológica 
Objetivo: Monitorar e responder rapidamente aos surtos de dengue nas regiões mais afetadas. 
Ações: Estabelecer sistemas de monitoramento contínuo que utilizem 
tecnologias de geolocalização e big data para identificar áreas de alto risco. 
Capacitar equipes de saúde locais para realizar inspeções regulares e eliminar 
criadouros do mosquito. 
  
- Intervenções Focadas por Região 
Objetivo: Adaptar as estratégias de prevenção e controle às necessidades 
específicas de cada região. 
Ações: No Sudeste e Centro-Oeste: Implementar programas intensivos de 
controle do mosquito, especialmente em áreas urbanas densamente povoadas. 
No Norte e Nordeste: Fortalecer as infraestruturas de saúde para garantir uma 
resposta rápida e eficaz aos surtos de dengue. 

Melhoria das Infraestruturas de Saúde:

-Reforço das Unidades de Saúde 
Objetivo: Garantir que as unidades de saúde estejam preparadas para lidar 
com surtos de dengue. 
Ações: Equipar unidades de saúde com os recursos necessários para diagnóstico e tratamento da dengue. 
Treinar profissionais de saúde em práticas de manejo clínico e tratamento 
adequado dos pacientes com dengue. 

- Monitoramento e Avaliação 
Objetivo: Avaliar continuamente a eficácia das medidas implementadas. 
Ações: Estabelecer indicadores de desempenho para monitorar o progresso 
das ações de controle e prevenção. 
Realizar avaliações periódicas para ajustar as estratégias conforme 
necessário.

Envolvimento da Comunidade: 

-Educação Comunitária 
Objetivo: Envolver as comunidades locais na prevenção da dengue. 
Ações: Organizar mutirões de limpeza e eliminação de criadouros do mosquito 
nas comunidades. 
Promover programas de educação nas escolas, incentivando estudantes a disseminar informações sobre prevenção em suas famílias e comunidades. 

- Participação Ativa dos Cidadãos 
Objetivo: Incentivar a participação ativa dos cidadãos nas ações de prevenção. 
Ações: Criar plataformas de comunicação, como aplicativos móveis, para que 
os cidadãos possam reportar focos de mosquito e colaborar com as 
autoridades de saúde.















