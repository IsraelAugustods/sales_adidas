[![author](https://img.shields.io/badge/author-IsraelAugustods-red.svg)](https://www.linkedin.com/in/israelaugustoalmeida/) ![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)
# Vendas Adidas 

<p align="center">
  <img alt="adidas" width="50%" src="https://github.com/user-attachments/assets/b22b1139-b7be-423a-8144-8c0b717ad16a">
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
  <img alt="g2" width="70%" src="https://github.com/user-attachments/assets/302a5d11-58fe-4388-801f-78f58a1cbdb5">
</p>

### Faturamento por Meses

Neste gráfico, temos duas linhas do tempo relacionadas ao faturamento, correspondentes aos anos de 2020 e 2021. Podemos observar que, em 2020, o faturamento foi menor em comparação a 2021, de acordo com este dataset.

Em 2020, o mês com maior faturamento foi abril, enquanto em 2021 foi julho, seguido de perto por dezembro.

<p align="center">
  <img alt="g3" width="70%" src="https://github.com/user-attachments/assets/699fb3b3-0116-4948-af56-4ba19905525d">
</p>

### Com qual revendedor a Adidas teve o maior lucro operacional, em média?

Neste gráfico de barras, temos o valor médio do lucro operacional por revendedor. Observa-se que o revendedor com o qual a Adidas obteve maior lucro foi o Walmart, seguido pelo Sports Direct.

<p align="center">
  <img alt="g4" width="70%" src="https://github.com/user-attachments/assets/b265bda5-0b79-4319-80b3-c1670b413dd0">
</p>

## Estatística

### Existe diferença no faturamento médio entre os produtos "Women's Apparel" e "Men's Apparel"?

<p align="center">
  <img alt="j1" width="35%" src="https://github.com/user-attachments/assets/cc19e76a-d74f-4996-90d8-a94d13e4ac89">
</p>

Ao observar a tabela acima, percebe-se uma aparente diferença na média de faturamento entre as duas categorias de produto. No entanto, realizei uma análise estatística para verificar se essa diferença é estatisticamente significativa.

Para investigar se há diferença no faturamento médio entre "Men's Apparel" e "Women's Apparel", apliquei o **teste t**. Esse teste possui pressupostos, como a **distribuição normal dos dados** e a **homogeneidade das variâncias**, e diferentes variações podem ser usadas dependendo dos resultados desses pressupostos.

Primeiro, verifiquei a normalidade dos dados com o **teste de Kolmogorov-Smirnov**, obtendo o seguinte resultado:

<p align="center">
  <img alt="j2" width="35%" src="https://github.com/user-attachments/assets/5e9cf654-074c-40d6-9090-ac9b0f9d3f88">
</p>

Conforme a tabela, os dados **não seguem uma distribuição normal**, pois o p-valor foi menor que 0,05, levando-me a rejeitar a hipótese nula de normalidade.

Escolhi o teste de **Kolmogorov-Smirnov** devido ao tamanho da amostra. Para amostras menores, o **teste de Shapiro-Wilk** seria mais apropriado.

Em seguida, testei a **homogeneidade das variâncias** com o **teste de Levene**, e o resultado foi:

<p align="center">
  <img alt="j3" width="35%" src="https://github.com/user-attachments/assets/80e0dab3-ab55-4943-b44d-9608498e8716">
</p>

O teste indicou que as variâncias dos dois grupos **não são homogêneas**, pois o p-valor também foi menor que 0,05, rejeitando a hipótese nula de homogeneidade.

É importante destacar que as amostras são **independentes**, ou seja, estou comparando dois grupos distintos: **Women's Apparel** e **Men's Apparel**.

Diante desses resultados (dados não normais e variâncias diferentes), utilizei o **teste U de Mann-Whitney**, uma alternativa não paramétrica ao teste t para amostras independentes que não atendem aos pressupostos de normalidade. O resultado foi o seguinte:

<p align="center">
  <img alt="j4" width="35%" src="https://github.com/user-attachments/assets/bde355e8-0c21-47d8-8aba-8360988a3e14">
</p>

Com base no teste, concluo que **o faturamento médio da categoria Women's Apparel é maior que o da Men's Apparel**. O p-valor do **U de Mann-Whitney** foi menor que 0,05, rejeitando a hipótese nula de que não há diferença significativa entre os faturamentos médios dessas categorias.

## Considerações finais

Este estudo teve como objetivo principal responder a perguntas de negócio e gerar insights a partir dos dados. Com uma base de dados rica como esta, muitos insights podem ser extraídos. Trouxe aqui quatro dos principais que considerei mais relevantes para esta apresentação. Além disso, incluí algumas análises estatísticas para validar as informações de forma mais precisa.

Alguns insights e detalhes adicionais ficaram de fora desta apresentação. Para acessar o projeto completo, confira neste [link](https://docs.google.com/spreadsheets/d/15_zfHNMMUMyUoOAIOYxoutmLrqxe_eggvPRvByrEGNc/edit?usp=sharing).

Vale destacar que futuras análises podem ser realizadas, como a aplicação de modelos de **machine learning** para prever o faturamento em anos futuros.

Espero que tenham gostado do meu trabalho! Estou sempre aberto a sugestões e melhorias.

Entre em contato comigo pelo:

💼 [LinkedIn](https://www.linkedin.com/in/israelaugustoalmeida/)

E também acesse meu portfólio para conferir outros projetos:

🖥️ [Portfólio](https://sites.google.com/view/portfolioisraelaugusto/in%C3%ADcio).

Obrigado!

