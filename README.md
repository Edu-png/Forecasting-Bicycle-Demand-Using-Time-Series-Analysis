# Forecasting Bicycle Demand Using Time Series Analysis and prediction 🚲🚲

<p align="center">
  <a href="https://github.com/Edu-png">
    <img src="https://img.shields.io/badge/Autor-Eduardo%20Coqueiro-purple?style=flat&logo=github" alt="Autor">
  </a>
  <a href="mailto:eduardocoqueiro@gmail.com">
    <img src="https://img.shields.io/badge/Email-eduardocoqueiro%40gmail.com-purple?style=flat&logo=gmail" alt="Email">
  </a>
  <a href="https://linkedin.com/in/eduardocoqueiro/">
    <img src="https://img.shields.io/badge/LinkedIn-Eduardo%20Coqueiro-purple?style=flat&logo=linkedin" alt="LinkedIn">
  </a>
  <a href="https://kaggle.com/EduardoCoqueiro">
    <img src="https://img.shields.io/badge/Kaggle-Eduardo%20Coqueiro-blue?style=flat&logo=kaggle" alt="Kaggle">
  </a>
</p>

![CAPAS - PROJETOS](https://github.com/user-attachments/assets/457651c6-f035-4357-8e3c-57d5718c0767)

## 📋 Sumário

## 📋 Resumo 
O objetivo principal deste projeto é entender os fatores que influenciam a demanda por bicicletas alugadas e desenvolver modelos preditivos para estimar a demanda futura, auxiliando na tomada de decisões estratégicas. O dataset utilizado inclui variáveis como:

- **Condições climáticas**: temperatura, sensação térmica, umidade e velocidade do vento.
- **Fatores sazonais**: estações do ano, feriados e finais de semana.
- **Horários e datas**: períodos diários, mensais e sazonais.

# 🌟 Introdução ao Projeto - Previsão da Demanda por Bicicletas

A previsão de demanda é uma tarefa essencial para empresas que operam sistemas de compartilhamento de bicicletas, permitindo um planejamento eficaz e a otimização de recursos. Este projeto explora o uso de técnicas de análise de séries temporais e machine learning para prever a demanda por bicicletas alugadas com base em dados históricos e fatores contextuais.

## 🎯 Objetivos do Projeto
1. **Compreender os fatores que influenciam a demanda por bicicletas alugadas**, incluindo variáveis climáticas, sazonais e comportamentais.
2. **Analisar padrões sazonais e temporais**:
   - Identificar horários de pico e períodos de maior demanda.
   - Avaliar a influência de estações do ano e feriados.
3. **Desenvolver modelos preditivos robustos**:
   - Utilizar séries temporais e técnicas de aprendizado de máquina para prever a demanda futura.
   - Comparar diferentes abordagens preditivas para maximizar a acurácia.
4. **Fornecer insights acionáveis** para ajudar empresas a otimizar sua operação, melhorando a alocação de bicicletas e a experiência dos usuários.

Com uma abordagem focada em dados, este projeto não só analisa tendências passadas, mas também projeta cenários futuros para apoiar decisões estratégicas no setor de mobilidade urbana.

# 🛠️ Pipeline do Projeto - Previsão da Demanda por Bicicletas

![1](https://github.com/user-attachments/assets/9385b002-c53c-41c4-84de-e06f221cae24)


A estrutura do projeto segue uma sequência lógica e modular, desde a coleta e exploração dos dados até a implementação e avaliação de modelos preditivos. Abaixo, apresentamos a pipeline detalhada:

---

## 1. **Coleta e Importação dos Dados**
### 1.1 Fonte dos Dados
- O conjunto de dados foi extraído de uma plataforma pública, contendo informações sobre aluguéis de bicicletas, condições climáticas, feriados e características temporais.

### 1.2 Importação
- Bibliotecas utilizadas:
  - `pandas` para manipulação de dados.
  - `numpy` para cálculos numéricos.
- O arquivo de dados em formato CSV foi carregado e verificado utilizando métodos como `.head()`, `.info()` e `.describe()`.

---

## 2. **Análise Exploratória de Dados (EDA)**
### 2.1 Estrutura e Estatísticas Descritivas
- Avaliação da estrutura do dataset:
  - Colunas disponíveis: `datetime`, `season`, `weather`, `temp`, `humidity`, `windspeed`, `holiday`, `workingday`, `demand`.
  - Identificação de tipos de dados e possíveis inconsistências.

### 2.2 Análise Gráfica
- Gráficos criados com `matplotlib` e `seaborn`:
  - Distribuição da demanda ao longo do tempo.
  - Correlações entre variáveis, como temperatura e demanda.
  - Padrões sazonais e temporais (diários, semanais e mensais).
  - Análise do impacto de feriados e dias úteis.

---

## 3. **Pré-processamento dos Dados**
### 3.1 Limpeza
- Tratamento de valores ausentes e inconsistências.
- Conversão de variáveis categóricas (e.g., estações e condições climáticas) para valores numéricos usando `LabelEncoder`.

### 3.2 Transformações
- **Criação de variáveis derivadas:**
  - Extração de componentes de data/hora, como ano, mês, dia, hora e dia da semana.
  - Identificação de horários de pico com base na demanda.
- **Normalização e padronização:**
  - Normalização de variáveis contínuas (`temp`, `humidity`, `windspeed`) usando `StandardScaler`.

---

## 4. **Análise de Séries Temporais**
### 4.1 Decomposição
- Uso da biblioteca `statsmodels` para decomposição aditiva da série temporal em:
  - **Tendência:** Direção geral da demanda ao longo do tempo.
  - **Sazonalidade:** Padrões recorrentes em diferentes períodos.
  - **Resíduos:** Componentes aleatórios.

### 4.2 Análise Autocorrelacional
- Gráficos de autocorrelação (ACF) e autocorrelação parcial (PACF) para identificar dependências temporais.

---

## 5. **Modelagem Preditiva**
### 5.1 Divisão do Conjunto de Dados
- Divisão em dados de **treinamento (80%)** e **teste (20%)**, mantendo a sequência temporal.

### 5.2 Modelos Implementados
1. **Modelos Clássicos de Séries Temporais:**
   - **ARIMA:** Para modelar a relação entre os componentes da série.
   - **SARIMA:** Extensão do ARIMA com ajuste de sazonalidade.
   - **Holt-Winters:** Para capturar tendências e padrões sazonais.

2. **Modelos Baseados em Machine Learning:**
   - **Random Forest Regressor:** Para capturar interações complexas entre variáveis.
   - **Gradient Boosting Machines (GBM):** Modelos como XGBoost para otimizar previsões.
   - **Rede Neural Recorrente (RNN):** Para aproveitar dependências temporais e melhorar a acurácia.

### 5.3 Hiperparâmetros e Validação
- Busca por hiperparâmetros com `GridSearchCV`.
- Validação cruzada com séries temporais (TimeSeriesSplit) para avaliar modelos sem vazamento de dados.

---

## 6. **Avaliação dos Modelos**
### 6.1 Métricas de Desempenho
- **Erro Absoluto Médio (MAE):** Média do erro absoluto entre previsões e valores reais.
- **Erro Médio Quadrático (MSE):** Penaliza diferenças maiores entre previsões e valores reais.
- **R² (Coeficiente de Determinação):** Mede a proporção da variabilidade explicada pelo modelo.

### 6.2 Comparação de Modelos
- Comparação de modelos com base nas métricas acima.
- Seleção do modelo final com melhor desempenho no conjunto de teste.

---

## 7. **Interpretação e Visualização dos Resultados**
### 7.1 Insights Gerais
- Padrões identificados na demanda de bicicletas:
  - Dias úteis versus finais de semana.
  - Impacto do clima e sazonalidade.
  - Tendências ao longo dos anos.

### 7.2 Visualizações
- Gráficos preditivos mostrando comparações entre valores reais e previstos:
  - Curvas temporais.
  - Resíduos dos modelos.

---

## 8. **Aplicações e Próximos Passos**
### 8.1 Aplicação dos Resultados
- Planejamento de alocação de bicicletas com base na demanda prevista.
- Ajuste de estratégias de marketing e operação em dias de alta ou baixa demanda.

### 8.2 Melhorias Futuras
- Inclusão de dados externos, como eventos locais e condições de tráfego.
- Teste de modelos mais avançados, como LSTM e Transformers, para previsões mais precisas.
- Ampliação do escopo temporal para incorporar mais anos de dados e tendências.

---

# 🧪 Metodologia

A metodologia adotada para este projeto foi cuidadosamente estruturada para garantir que todas as etapas fossem realizadas de forma sistemática e eficiente, desde a coleta de dados até a avaliação do desempenho dos modelos preditivos. 

---

## 📂 Coleta de Dados
1. **Fonte dos Dados**
   - O conjunto de dados foi obtido de uma plataforma pública e contém informações detalhadas sobre a demanda de bicicletas, incluindo:
     - Data e hora da coleta.
     - Variáveis climáticas: temperatura, umidade e velocidade do vento.
     - Informações sazonais: feriados, dias úteis e finais de semana.
   - Arquivo principal: `bikeshare_demand.csv`.

2. **Ferramentas Utilizadas**
   - Bibliotecas: `pandas` e `numpy` para carregar e manipular os dados.

---

## 🧹 Pré-processamento dos Dados
1. **Limpeza**
   - Remoção de valores ausentes e inconsistentes.
   - Conversão de variáveis categóricas, como `season` e `weather`, em valores numéricos usando `LabelEncoder`.

2. **Transformações**
   - Extração de variáveis temporais:
     - Componentes de data/hora: ano, mês, dia, hora e dia da semana.
     - Identificação de horários de pico com base na análise da demanda.
   - Normalização de variáveis contínuas (`temp`, `humidity`, `windspeed`) usando `StandardScaler`.

3. **Verificação**
   - Conferência das dimensões dos dados e consistência entre variáveis.
   - Análise visual para detectar outliers que poderiam distorcer os resultados.

---

## 📊 Análise Exploratória de Dados (EDA)
1. **Estatísticas Descritivas**
   - Resumo estatístico dos dados usando `.describe()`.
   - Identificação de padrões de distribuição, como média, desvio padrão e valores extremos.

2. **Visualizações**
   - Gráficos de linha e dispersão para explorar tendências e sazonalidades.
   - Correlação entre variáveis:
     - Uso de `heatmap` para analisar interações como temperatura versus demanda.
   - Gráficos de barras e histogramas para visualizar a distribuição de variáveis categóricas e contínuas.

---

## 📈 Modelagem Preditiva
1. **Divisão dos Dados**
   - Dados divididos em:
     - **Treinamento (80%)**: Para ajuste do modelo.
     - **Teste (20%)**: Para avaliação final.
   - Divisão temporal para preservar a sequência dos dados.

2. **Seleção de Modelos**
   - Modelos implementados:
     - **ARIMA**: Para prever a demanda com base em dependências temporais.
     - **SARIMA**: Extensão do ARIMA para ajustar sazonalidade.
     - **Redes Neurais Recorrentes (RNN)**: Para capturar padrões complexos em séries temporais.
     - **Random Forest** e **XGBoost**: Para modelagem preditiva baseada em variáveis independentes.

3. **Treinamento**
   - Ajuste de hiperparâmetros com `GridSearchCV` para modelos de aprendizado de máquina.
   - Uso de otimizadores, como Adam, para redes neurais.

4. **Validação**
   - Validação cruzada com séries temporais utilizando `TimeSeriesSplit`.
   - Avaliação de métricas de desempenho durante o treinamento.

---

## 📉 Avaliação e Interpretação dos Resultados
1. **Métricas de Avaliação**
   - **Erro Absoluto Médio (MAE):** Para medir a precisão geral.
   - **Erro Médio Quadrático (MSE):** Para penalizar grandes desvios.
   - **R² (Coeficiente de Determinação):** Para verificar a proporção de variabilidade explicada pelo modelo.

2. **Interpretação**
   - Comparação de modelos para identificar o mais adequado.
   - Análise dos resíduos para avaliar padrões não capturados pelos modelos.

---

## 🔮 Aplicações e Próximos Passos
1. **Implementação Prática**
   - Utilização dos modelos para prever a demanda futura e otimizar a alocação de bicicletas.

2. **Melhorias Futuras**
   - Testar novos modelos, como LSTM e Transformers, para prever séries temporais de forma mais eficiente.
   - Incluir dados externos, como eventos especiais e mudanças de políticas de transporte.

---

A metodologia garante que todas as etapas do projeto sejam realizadas de maneira estruturada, desde a coleta dos dados até a análise e implementação dos resultados. O foco em modelagem robusta e validação detalhada proporciona previsões precisas e insights valiosos.

# 📊 Resultados 

---

### Gráfico 1 - Bicicletas alugadas por hora no final de semana

![10](https://github.com/user-attachments/assets/ce741d41-0dc2-4fca-a324-d97866665d46)

- **Descrição:** Este gráfico de barras exibe o número total de bicicletas alugadas por hora durante os finais de semana.
- **Conclusão:** O maior número de aluguéis ocorre entre 13h e 16h, sugerindo um pico de atividade nesse período, provavelmente devido ao lazer ou transporte em horários mais convenientes.

---

### Gráfico 2 - Número de aluguéis de bicicletas por data

![12](https://github.com/user-attachments/assets/19b0daa9-d7dc-42f7-b0e8-a261cb4e95f4)


- **Descrição:** Este gráfico de linhas apresenta o número de bicicletas alugadas por data, cobrindo o período de 2015 a 2017.
- **Conclusão:** Há um padrão sazonal nos aluguéis, com picos durante os meses de verão e quedas nos meses de inverno, demonstrando a influência das condições climáticas na demanda.

---

### Gráfico 3 - Distribuição das variáveis meteorológicas
![2](https://github.com/user-attachments/assets/c74d97ab-82a9-4e26-ab67-e4f55a645794)

- **Descrição:** Histogramas para as variáveis meteorológicas: temperatura, umidade, velocidade do vento e sensação térmica.
- **Conclusão:** As distribuições mostram que:
  - A temperatura mais comum está em torno de 15°C.
  - A umidade geralmente é alta, acima de 70%.
  - Ventos leves predominam, com velocidades abaixo de 20 km/h.
  - A sensação térmica acompanha a distribuição da temperatura.

| Variável          | Faixa de Valores | Observação Mais Comum |
|--------------------|------------------|------------------------|
| Temperatura (°C)  | 0 - 30           | ~15°C                 |
| Umidade (%)       | 20 - 100         | ~80%                  |
| Velocidade do Vento (km/h) | 0 - 50 | ~10 - 20 km/h         |
| Sensação Térmica (°C) | -5 - 35      | ~15°C                 |

---

### Gráfico 4 - Relação entre contagem de aluguéis e variáveis meteorológicas

![3](https://github.com/user-attachments/assets/06fd0e44-7b95-4244-9be3-a246b7d80f8d)


- **Descrição:** Gráficos de dispersão para verificar a relação entre o número de aluguéis e variáveis como temperatura, umidade, velocidade do vento e sensação térmica.
- **Conclusão:** Os aluguéis mostram:
  - **Temperatura e Sensação Térmica:** Correlação positiva, indicando maior demanda em condições mais quentes.
  - **Umidade:** Correlação negativa, com menor demanda em condições muito úmidas.
  - **Velocidade do Vento:** Impacto reduzido na demanda.

---

### Gráfico 5 - Matriz de correlação

![4](https://github.com/user-attachments/assets/6c15512f-574a-4106-9294-4e9c5ef93763)


- **Descrição:** Uma matriz de correlação exibindo as relações entre as principais variáveis do dataset.
- **Conclusão:** A temperatura e a sensação térmica têm uma correlação extremamente alta (0,99), o que reflete sua interdependência. A umidade apresenta correlação negativa com o número de aluguéis, enquanto a temperatura tem uma relação positiva.

| Variáveis            | Contagem | Temperatura | Sensação Térmica | Umidade | Velocidade do Vento |
|----------------------|----------|-------------|------------------|---------|---------------------|
| **Contagem**         | 1        | 0.39        | 0.37             | -0.46   | 0.12                |
| **Temperatura**      | 0.39     | 1           | 0.99             | -0.45   | 0.15                |
| **Sensação Térmica** | 0.37     | 0.99        | 1                | -0.40   | 0.088               |
| **Umidade**          | -0.46    | -0.45       | -0.40            | 1       | -0.29               |
| **Velocidade do Vento** | 0.12  | 0.15        | 0.088            | -0.29   | 1                   |

---

### Gráfico 6 - Aluguel de bicicletas em dias normais e feriados
![5](https://github.com/user-attachments/assets/7b00bc1a-4a9a-4e05-8b08-9e2d7922f636)


- **Descrição:** Boxplot comparando o número de aluguéis em dias normais e feriados.
- **Conclusão:** Dias normais apresentam maior mediana de aluguéis em comparação com feriados, indicando que as bicicletas são mais usadas para transporte regular do que para lazer em feriados.

| Tipo de Dia | Mediana de Aluguéis | Quartil Inferior | Quartil Superior |
|-------------|---------------------|------------------|------------------|
| **Normal**  | ~1200              | ~800             | ~1600            |
| **Feriado** | ~1000              | ~600             | ~1300            |

---

### Gráfico 7 - Aluguel de bicicletas em dias de semana e finais de semana
![6](https://github.com/user-attachments/assets/d81be318-4544-45fa-8c23-1d0de335d0e7)


- **Descrição:** Boxplot comparando o número de aluguéis em dias de semana e finais de semana.
- **Conclusão:** Há uma mediana mais alta de aluguéis em dias úteis, refletindo maior uso durante o transporte regular. Os finais de semana mostram menor mediana, mas maior dispersão, indicando uso variado para lazer.

| Tipo de Dia     | Mediana de Aluguéis | Quartil Inferior | Quartil Superior |
|------------------|---------------------|------------------|------------------|
| **Dias Úteis**   | ~1500              | ~1000            | ~1800            |
| **Finais de Semana** | ~1100         | ~800             | ~1400            |

---

### Gráfico 8 - Aluguel de bicicletas em diferentes condições climáticas
![7](https://github.com/user-attachments/assets/da8fad36-c882-4a36-b39d-426d77528d69)


- **Descrição:** Gráfico de barras mostrando o número total de aluguéis em diferentes condições climáticas.
- **Conclusão:** Condições de céu limpo e parcialmente nublado têm o maior número de aluguéis, enquanto climas extremos como neve e tempestades têm a menor demanda.

| Clima               | Total de Aluguéis |
|---------------------|-------------------|
| Céu Limpo           | ~7.000.000       |
| Parcialmente Nublado | ~6.000.000       |
| Nublado             | ~4.000.000       |
| Chuva Leve          | ~1.500.000       |
| Neve                | ~100.000         |

---

### Gráfico 9 - Bicicletas alugadas por hora

![9](https://github.com/user-attachments/assets/b17a39d1-f84a-464b-9e2e-ae8ba40a9fa6)

- **Descrição:** Gráfico de barras mostrando o total de bicicletas alugadas por hora durante todo o período analisado.
- **Conclusão:** Os picos de aluguel ocorrem durante as horas de deslocamento matinal (7h-9h) e à tarde (17h-19h), reforçando o uso das bicicletas para transporte.

---

### Gráfico 10 - Bicicletas alugadas por hora no final de semana
![10](https://github.com/user-attachments/assets/9f9c6141-6cf8-4d2b-ac18-d87bbc4cd50a)


- **Descrição:** Gráfico de barras mostrando o número de bicicletas alugadas por hora durante finais de semana.
- **Conclusão:** O uso é mais concentrado entre 10h e 16h, com um pico em torno das 13h, indicando maior uso para atividades recreativas e sociais.

---

### Gráfico 11 - Número de aluguéis de bicicletas por data

![12](https://github.com/user-attachments/assets/34d5577f-541c-4ba3-b88e-777dbb40f48f)

- **Descrição:** Este gráfico de linha apresenta a contagem diária de aluguéis de bicicletas ao longo do tempo, abrangendo o período de 2015 a 2017. A linha mostra as flutuações na demanda por bicicletas com tendências sazonais evidentes.
- **Conclusão:**
  - Observa-se um padrão sazonal consistente, com picos nos meses de verão (julho) e quedas significativas nos meses de inverno (janeiro).
  - A demanda aumenta gradativamente até meados de 2015 e 2016, mas apresenta variações mais acentuadas durante o mesmo período.
  - Esses dados são fundamentais para prever a demanda futura e identificar tendências de comportamento dos usuários.

---
### Gráfico 13 - Número de Aluguéis de Bicicletas por Mês

![13](https://github.com/user-attachments/assets/0921bc07-a4f1-440d-b4bc-c27989037981)


- **Descrição:** Apresenta a contagem total de aluguéis de bicicletas ao longo dos meses do ano.
- **Conclusão:**
  - Há uma clara sazonalidade no uso de bicicletas, com picos em julho e junho, que coincidem com os meses de clima mais ameno e favorável para atividades ao ar livre.
  - Os meses de inverno (novembro, dezembro e janeiro) apresentam uma redução considerável na contagem de aluguéis.

---

### Gráfico 14 - Média de Aluguel Diário de Bicicletas por Mês

![14](https://github.com/user-attachments/assets/6d51be90-383b-43f7-8aa5-aef72cf2aa2d)

- **Descrição:** Mostra a média diária de aluguéis de bicicletas distribuída ao longo dos meses de dois anos consecutivos.
- **Conclusão:**
  - As médias diárias acompanham o padrão de sazonalidade observado no gráfico anterior, confirmando o aumento no verão e a queda nos meses de inverno.
  - Em julho de 2015 e junho de 2016, o número médio de aluguéis diários alcançou os valores mais altos, reforçando o impacto do clima e do período de férias.

---

### Gráfico 15 - Comparação entre Dados Reais e Ajustes do Modelo (Primeiro Modelo)

![15](https://github.com/user-attachments/assets/c4afc404-09bf-4485-9b2e-64da42edfdc4)


- **Descrição:** Exibe a comparação entre os valores reais (pontos pretos) e as previsões ajustadas pelo primeiro modelo.
- **Conclusão:**
  - O modelo captura bem as tendências sazonais e cíclicas, mostrando uma boa aderência aos dados reais.
  - No entanto, há algumas discrepâncias notáveis, especialmente nos picos e vales, indicando oportunidades de melhoria na precisão do modelo.
 

### Gráfico 16 - Tendências de longo prazo e padrões sazonais

![16](https://github.com/user-attachments/assets/6f461700-0a0f-410c-b3f0-f81c620750ff)


- **Descrição:** Este gráfico apresenta a tendência geral, o padrão semanal e o padrão anual na contagem de bicicletas alugadas.
- **Conclusão:**
  - A tendência mostra uma recuperação constante após uma queda inicial no aluguel de bicicletas.
  - Os padrões semanais indicam que os alugueis aumentam no início da semana e caem no final.
  - A sazonalidade anual revela uma maior demanda nos meses de verão e uma queda durante o inverno.

---

### Gráfico 17 - Previsão de série temporal com Prophet

![17](https://github.com/user-attachments/assets/7bfb39f1-6feb-4597-b738-dfd1c8b7b216)


- **Descrição:** Este gráfico mostra as previsões do modelo Prophet em relação aos dados reais, com intervalos de confiança.
- **Conclusão:**
  - O modelo Prophet captura com precisão a sazonalidade e a tendência geral.
  - Os intervalos de confiança cobrem adequadamente a maioria dos pontos reais, demonstrando um bom ajuste.

---

### Gráfico 18 - Previsão de longo prazo com Prophet

![18](https://github.com/user-attachments/assets/4475ec89-e30c-4811-986f-07fccf8d0193)


- **Descrição:** Este gráfico mostra as previsões de longo prazo feitas pelo modelo Prophet, destacando padrões semanais e tendências gerais.
- **Conclusão:**
  - As previsões indicam uma recuperação significativa na demanda ao longo do tempo.
  - O modelo prevê um crescimento na contagem de bicicletas alugadas durante os meses de verão, com variações sazonais claras.
 
### Gráfico 19 - Previsão com Modelo Prophet

![19](https://github.com/user-attachments/assets/9ae00b09-659a-46f6-9d0c-1e47e1622844)

- **Descrição:** Este gráfico apresenta a decomposição do modelo Prophet, mostrando a tendência (trend), sazonalidade semanal (weekly) e sazonalidade anual (yearly).
- **Conclusão:**
  - O modelo captura uma tendência decrescente ao longo do tempo.
  - A sazonalidade semanal evidencia uma queda significativa nos alugueis aos domingos e um aumento gradual até quintas-feiras.
  - A sazonalidade anual indica maior volume de alugueis durante os meses de primavera e verão.

---

### Gráfico 20 - Previsão com Redes Neurais (RNN)

![20](https://github.com/user-attachments/assets/363ebc72-26e4-4d6d-a132-b7c5541ed682)


- **Descrição:** Apresenta as previsões geradas pelo modelo de Redes Neurais Recorrentes em comparação com os dados reais.
- **Conclusão:**
  - O modelo RNN mostra excelente desempenho em capturar padrões complexos e não lineares.
  - As previsões estão muito próximas dos valores reais, indicando alta precisão, mesmo em momentos de maior variabilidade.

---

### Gráfico 21 - Previsão com Intervalos de Confiança

![21](https://github.com/user-attachments/assets/5793ec3a-3e40-4906-ab77-d7a68e4c0512)

- **Descrição:** Exibe a previsão de demanda de aluguel de bicicletas com intervalos de confiança gerados pelo modelo Prophet.
- **Conclusão:**
  - O modelo consegue estimar a demanda futura com intervalos de confiança apropriados.
  - A maior variabilidade das previsões aparece nas extremidades dos dados, onde há menor volume de informação histórica.


### Conclusões Gerais

- **Padrões Sazonais e Tendências:**
  - A demanda por bicicletas tem forte componente sazonal, com picos nos meses de verão e queda no inverno.
  - Horários de pico estão associados a deslocamentos para o trabalho (manhã e tarde) nos dias úteis e a atividades de lazer nos finais de semana.

- **Fatores que Influenciam a Demanda:**
  - **Temperatura** é a variável mais influente, com demanda aumentando em climas mais quentes.
  - **Hora do dia** e **estação do ano** também têm impacto significativo.
  - **Condições climáticas adversas** (chuva, neve) reduzem a demanda.

- **Desempenho dos Modelos:**
  - Modelos baseados em aprendizado de máquina (Random Forest e RNN) superam os modelos tradicionais de séries temporais em precisão.
  - **RNN** é particularmente eficaz em capturar padrões complexos e não lineares.

- **Aplicações Práticas:**
  - Os insights obtidos podem ajudar na alocação eficiente de bicicletas, planejamento de manutenção e estratégias de marketing.
  - Previsões precisas permitem otimizar recursos e melhorar a satisfação do cliente.

---

Este conjunto de resultados reforça a importância de considerar múltiplos fatores ao prever a demanda por bicicletas e demonstra a eficácia de modelos avançados de machine learning nesse contexto.


## Agradecimentos 👏
Gostaria de agradecer a todos os instrutores e colegas que contribuíram para a realização deste projeto. Em especial, agradeço ao curso "Data Science: analisando e prevendo séries temporais" da Alura, ministrado pela professora Valquíria Alencar.

<div align="center">
  <img src="https://github.com/user-attachments/assets/54afb33c-97be-40b6-8c96-0f12852e946f" alt="thank-you" width="500">
</div>

## 📞 Contato
- **LinkedIn:** [Eduardo Coqueiro](https://www.linkedin.com/in/eduardocoqueiro/)
- **Site:** [Eduardo Coqueiro](https://dataguy.my.canva.site/eduardo-coqueiro)
- **Kaggle:** [Eduardo Coqueiro](https://www.kaggle.com/eduardocoqueiro)

