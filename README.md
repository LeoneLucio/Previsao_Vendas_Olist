# Previsão de Quantidade de Itens Vendidos por Categoria de Produto

Este projeto visa prever a quantidade de itens vendidos por categoria de produto utilizando dados históricos de pedidos realizados em um e-commerce brasileiro. Para isso, foram utilizados diversos modelos de aprendizado de máquina e técnicas de pré-processamento de dados.

## Objetivo

O objetivo principal deste projeto é prever as quantidades de itens vendidos em categorias específicas de produtos, com base em dados históricos de pedidos. Esse tipo de previsão pode ser útil para melhorar a gestão de estoques, planejar campanhas promocionais e otimizar a experiência do cliente em plataformas de e-commerce.

## Dados

Os dados utilizados neste projeto são provenientes de uma base de e-commerce brasileiro, que contém informações sobre pedidos, como:
- **Preço do produto**
- **Frete**
- **Cidade e estado do cliente**
- **Quantidade de itens adquiridos por categoria**

Esses dados foram utilizados para treinar e testar modelos preditivos com o intuito de prever a quantidade de itens vendidos por categoria.

## Pré-processamento de Dados

Durante o processo de pré-processamento, foram realizadas as seguintes etapas:

1. **Limpeza de Dados**: Colunas irrelevantes foram removidas e colunas com valores faltantes foram verificadas.
2. **Conversão de Variáveis Categóricas**: As variáveis categóricas como cidade e estado do cliente foram convertidas para valores numéricos usando a técnica de codificação `factorize`.
3. **Conversão de Data**: A coluna `order_purchase_timestamp` foi convertida para o formato de data.
4. **Transformação dos Dados**: As variáveis categóricas foram transformadas em variáveis numéricas, e os dados foram normalizados para garantir que o modelo tivesse uma melhor performance.

## Modelos Utilizados

Foram testados os seguintes modelos de aprendizado supervisionado:

1. **Regressão Linear**
2. **Random Forest Regressor**
3. **XGBRegressor**
4. **Gradient Boosting Regressor**
5. **KNeighbors Regressor**

Todos os modelos foram avaliados utilizando o **coeficiente R²**, **MAE (Mean Absolute Error)**, **MSE (Mean Squared Error)**, e **RMSE (Root Mean Squared Error)** para comparar a precisão das previsões.

## Resultados

O **Gradient Boosting Regressor** foi o modelo que apresentou os melhores resultados, com um **coeficiente R² de 0.79** nas bases de treinamento e teste, o que indica uma boa capacidade de previsão. Além disso, os erros absolutos e quadráticos foram relativamente baixos, mostrando que o modelo foi eficaz na previsão da quantidade de itens vendidos.

## Como Executar o Projeto

Para rodar este projeto em seu ambiente local, siga os passos abaixo:

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/previsao-itens-vendidos.git
   ```

2. **Instale as dependências**:
   Crie um ambiente virtual e instale as bibliotecas necessárias:
   ```bash
   pip install -r requirements.txt
   ```

3. **Execute o script principal**:
   O script principal do projeto é `previsao.py`. Para rodá-lo, use:
   ```bash
   python previsao.py
   ```

4. **Verifique os resultados**:
   Após a execução do script, você verá os resultados das previsões e as métricas de avaliação no terminal.

## Bibliotecas Utilizadas

- **Pandas**: Para manipulação e análise de dados.
- **Numpy**: Para operações matemáticas.
- **Scikit-learn**: Para treinamento dos modelos e avaliação de desempenho.
- **XGBoost**: Para o modelo XGBRegressor.
- **Matplotlib** e **Seaborn**: Para visualização de gráficos.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para fazer *fork* deste repositório, enviar *pull requests* ou sugerir melhorias.

