[![author](https://img.shields.io/badge/author-IsraelAugustods-red.svg)](https://www.linkedin.com/in/israelaugustoalmeida/) ![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)
# Vendas Adidas 

<p align="center">
  <img alt="data" width="50%" src="https://github.com/user-attachments/assets/b22b1139-b7be-423a-8144-8c0b717ad16a">
</p>

## Objetivo do Estudo
Este estudo tem como foco a análisar os dados de vendas de produtos adidas para outros revendedores, com o objetivo de gerar insights e responder a perguntas de negócio.

## Fonte dos Dados

Todos os dados utilizados neste projeto foram obtidos de um dataset disponível no [***Kaggle***](https://www.kaggle.com/), acessível [neste link](https://www.kaggle.com/datasets/heemalichaudhari/adidas-sales-dataset?select=Adidas+US+Sales+Datasets.xlsx).

O ***Kaggle*** é uma plataforma online voltada para a comunidade de ciência de dados e aprendizado de máquina. Fundada em 2010, o Kaggle permite que usuários de todos os níveis de habilidade participem de competições, acessem datasets gratuitos, pratiquem e desenvolvam habilidades em ciência de dados, além de colaborar com outros membros da comunidade.

## Tecnologias Utilizadas
<p align="left">  
  <a href="https://www.microsoft.com/pt-br/microsoft-365/excel" rel="noreferrer"> <img src="https://marcas-logos.net/wp-content/uploads/2019/11/microsoft-excel-logo.jpg" alt="excel" width="30" height="30"/> </a> 
  <a href="https://www.jamovi.org/"> <img src="https://upload.wikimedia.org/wikipedia/commons/2/26/Jamovi_logo.png" alt="jamovi" width="30" height="30"/> </a> 

## Destaques do Projeto

### Número de Pedidos por Cliente

Este gráfico de funil mostra o número de pedidos realizados pelos revendedores neste dataset. É importante destacar que o revendedor com maior número de pedidos foi o Foot Locker, seguido pela West Gear, Kohl's, Amazon e, por último, o Walmart. 

<p align="center">
  <img alt="g1" width="70%" src="https://github.com/user-attachments/assets/d01d975b-0879-4e86-9aee-feab59030883">
</p>

### Faturamento por tipo de produto em todas as regiões

Neste gráfico, temos o faturamento das vendas por tipo de produto, dividido em seis categorias: Men's Apparel, Women's Apparel, Men's Athletic Footwear, Women's Athletic Footwear, Men's Street Footwear e Women's Street Footwear. Além disso, os dados estão filtrados por quatro regiões: Midwest, Northeast, South, Southeast e West. 

Podemos observar que, em todas as regiões, a categoria de produto com o maior faturamento é a Men's Street Footwear.

<p align="center">
  <img alt="g1" width="70%" src="https://github.com/user-attachments/assets/302a5d11-58fe-4388-801f-78f58a1cbdb5">
</p>

### Faturamento por Meses

Neste gráfico, temos duas linhas do tempo relacionadas ao faturamento, correspondentes aos anos de 2020 e 2021. Podemos observar que, em 2020, o faturamento foi menor em comparação a 2021, de acordo com este dataset.

Em 2020, o mês com maior faturamento foi abril, enquanto em 2021 foi julho, seguido de perto por dezembro.

<p align="center">
  <img alt="g1" width="70%" src="https://github.com/user-attachments/assets/699fb3b3-0116-4948-af56-4ba19905525d">
</p>

### Com qual revendedor a Adidas teve o maior lucro operacional, em média?

Neste gráfico de barras, temos o valor médio do lucro operacional por revendedor. Observa-se que o revendedor com o qual a Adidas obteve maior lucro foi o Walmart, seguido pelo Sports Direct.

<p align="center">
  <img alt="g1" width="70%" src="https://github.com/user-attachments/assets/b265bda5-0b79-4319-80b3-c1670b413dd0">
</p>

## Estatística

### Existe diferença no faturamento entre os produtos "Women's Apparel" e "Men's Apparel", na média?

<p align="center">
  <img alt="t1" width="35%" src="https://github.com/user-attachments/assets/cc19e76a-d74f-4996-90d8-a94d13e4ac89">
</p>

Ao analisar a tabela acima, parece que existe uma diferença clara na média dos faturamentos entre as duas categorias de produto. No entanto, eu precisei realizar uma análise estatística para confirmar essa suposição.

Como meu objetivo é descobrir se, na média, existe diferença entre o faturamento entre as categorias Men's Apparel e Women's Apparel, apliquei o **teste t**. Esse teste possui alguns pressupostos, como a **distribuição normal dos dados** e a **homogeneidade das variâncias**. Dependendo do resultado desses pressupostos, diferentes variações do teste t podem ser aplicadas.

Primeiro, verifiquei a normalidade dos dados aplicando o teste de **Kolmogorov-Smirnov**, e obtive o seguinte resultado:

<p align="center">
  <img alt="r1" width="50%" src="https://github.com/user-attachments/assets/5e9cf654-074c-40d6-9090-ac9b0f9d3f88">
</p>

Com base nessa tabela, concluo que os dados **não possuem distribuição normal**, já que o p-valor foi menor que 0,05, o que me levou a rejeitar a hipótese nula (que os dados são normais).

Escolhi o teste de **Kolmogorov-Smirnov** devido à grande quantidade de dados. Caso eu estivesse trabalhando com menos amostras, o **teste de Shapiro-Wilk** seria mais adequado.

Em seguida, conferi a **homogeneidade das variâncias** utilizando o **teste de Levene**, e obtive o seguinte resultado:

<p align="center">
  <img alt="r3" width="50%" src="https://github.com/user-attachments/assets/80e0dab3-ab55-4943-b44d-9608498e8716">
</p>

O teste revelou que as variâncias dos dois grupos **não é homogenia**, já que o p-valor foi menor que 0,05, o que me levou a rejeitar a hipótese nula (de que há homogeneidade nas variâncias).

Gostaria de salientar que apliquei esses testes em **amostras independentes**, ou seja, estou comparando dois grupos distintos: **Data Scientists** e **Data Analysts**.

Diante dos resultados (distribuição não normal dos dado e  variâncias diferentes), optei por utilizar o **U de Mann-Whitney**, que é um teste não paramétrico utilizado para comparar duas amostras independentes e determinar se suas distribuições são significativamente diferentes. Ele é uma alternativa ao teste t para amostras independentes, quando os dados não atendem aos pressupostos de normalidade. Devido a esse 

<p align="center">
  <img alt="r4" width="50%" src="https://github.com/user-attachments/assets/82c1c0e4-105c-44f7-8123-7baa2df9f5d5">
</p>

Com isso, concluo que **os cientistas de dados ganham mais que os analistas de dados**, em média, nesse conjunto de dados. O p-valor do **teste t de Welch** foi menor que 0,05, o que me levou a rejeitar a hipótese nula (de que os cientistas de dados ganham menos ou igual aos analistas de dados).


## Considerações finais
