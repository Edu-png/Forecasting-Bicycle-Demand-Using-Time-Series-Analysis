# Forecasting Bicycle Demand Using Time Series Analysis and prediction 🚲🚲

## Sumário:
- [Resumo](#resumo)
- [Introdução](#introdução)
- [Objetivo](#objetivo)
- [Métodos](#métodos)
- [Conclusões](#conclusões)
- [Considerações finais](#considerações-finais)
- [Referências](#referências)
- [Documentação](#documentação)
- [Agradecimentos](#agradecimentos)
- [Contato](#contato)

## Resumo 🏃‍♀️
Este projeto tem como objetivo analisar a demanda por bicicletas utilizando técnicas de análise de séries temporais. A análise é realizada a partir de dados de aluguel de bicicletas, buscando identificar os principais fatores que influenciam a demanda e desenvolver um modelo preditivo para estimar o número de bicicletas que serão alugadas em períodos futuros.

## Introdução
O aluguel de bicicletas tem se tornado uma alternativa popular de transporte urbano. Para empresas que oferecem este serviço, entender a demanda é crucial para otimizar a disponibilidade das bicicletas e melhorar a satisfação dos clientes. Este projeto utiliza dados históricos de aluguel de bicicletas para analisar padrões e prever a demanda futura.

### Objetivo
Desenvolver um modelo de previsão da demanda por bicicletas, capaz de estimar o número de bicicletas alugadas diariamente e mensalmente. Além disso, identificar os principais fatores que influenciam essa demanda.

## Métodos
### Coleta dos dados 🎲
Os dados foram obtidos a partir de um dataset público disponibilizado no GitHub. A base de dados contém informações diárias sobre o aluguel de bicicletas, incluindo variáveis como temperatura, umidade, velocidade do vento, entre outras.

### Limpeza dos dados 🧹
Os dados foram pré-processados para remover valores ausentes e outliers. Além disso, foram criadas novas variáveis a partir das existentes para enriquecer a análise.

### Análise exploratória 🤿
Realizou-se uma análise exploratória dos dados (EDA) para identificar padrões sazonais e tendências na demanda por bicicletas. Visualizações gráficas foram utilizadas para facilitar a compreensão dos dados.

### Modelos de Machine Learning 🔮
Foram testados diversos modelos de séries temporais, incluindo ARIMA, SARIMA e Prophet. O desempenho dos modelos foi avaliado utilizando métricas como RMSE e MAPE.

### Bibliotecas utilizadas e suas respectivas funções 🐍
- **Pandas:** Manipulação de dados
- **NumPy:** Operações numéricas
- **Matplotlib:** Visualização de dados
- **Seaborn:** Visualização de dados
- **scikit-learn:** Ferramentas de machine learning
- **fbprophet:** Modelo de previsão de séries temporais

## Conclusões 💡
A análise mostrou que a demanda por bicicletas apresenta padrões sazonais, com picos durante os meses mais quentes. O modelo Prophet foi o que apresentou o melhor desempenho, sendo capaz de capturar tanto a tendência quanto a sazonalidade dos dados.

## Considerações finais 🚀
Ferramentas de previsão como as utilizadas neste projeto são essenciais para empresas que buscam otimizar seus recursos e melhorar a experiência do cliente. Continuar refinando esses modelos com mais dados e variáveis adicionais pode aumentar ainda mais sua precisão.

## Referências 📄
- Documentação do Prophet: https://facebook.github.io/prophet/docs/quick_start.html
- Pandas Documentation: https://pandas.pydata.org/pandas-docs/stable/
- Matplotlib Documentation: https://matplotlib.org/stable/contents.html
- Seaborn Documentation: https://seaborn.pydata.org/
- scikit-learn Documentation: https://scikit-learn.org/stable/

## Documentação 📚
- **[Notebook da Limpeza dos Dados](link_do_notebook_limpeza)**
- **[Notebook da Análise Exploratória dos Dados](link_do_notebook_eda)**
- **[Notebook das Previsões com Machine Learning](link_do_notebook_ml)**

Para uma experiência melhor, eu recomendo que esses notebooks sejam abertos pelo Google Colaboratory 😉

## Agradecimentos 👏
Gostaria de agradecer a todos os instrutores e colegas que contribuíram para a realização deste projeto. Em especial, agradeço ao curso "Data Science: analisando e prevendo séries temporais" da Alura, ministrado pela professora Valquíria Alencar.

## Contato 📪
- **LinkedIn:** [Eduardo Coqueiro](https://www.linkedin.com/in/eduardocoqueiro/)
- **Site:** [Eduardo Coqueiro](https://dataguy.my.canva.site/eduardo-coqueiro)
- **Kaggle:** [Eduardo Coqueiro](https://www.kaggle.com)
