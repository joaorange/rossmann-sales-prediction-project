# Drugstore Chain Sales Prediction

![144940356-a00abf79-b51b-47ce-b458-c706e326fdb1](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/310c6e66-fe9d-4d92-b846-dc58ce65f711)

This project is fictitious, and seeks to extract insights and propose data-based business solutions for a chain of drugstores. The objectives of this project were to perform exploratory data analysis, develop an accurate sales forecast model for the stores in the next six weeks, and create a telegram bot that can be accessed by the CEO or any other interested party to see the predictions.

Data can be found at <a href="https://www.kaggle.com/c/rossmann-store-sales">Kaggle</a>.

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

# 1. Description

Rossmann is one of the largest drug store chains in Europe, with around 56,200 employees and more than 4000 stores. 
The stores will receive investment for renovation, and the CFO need to know how much each store will sell to see the amount of money that will be invested in each unity.
The data team was requested to develop a sales model prediction that forecast the sales for the next 6 weeks for every store. The telegram bot was made to inform these predictions.

# 2. Business Strategy Results

The model developed predicts a gross income of $221.70 MM in the next 6 months for the stores.
Based on the mean absolute percentage error that the model gave to the "train" dataset for the sales of the stores, the best scenario has a gross income of $243.30 MM and a worst scenario of $200.09 MM.

# 3. Business Assumptions
The following assumptions were considered:

* The data available is only from 2013-01-01 to 2015-07-31;

* The data set variables, and their respective descriptions, are as follows:

| Variável | Descrição |
| ------------- | :-------------: |
| id  | Identificação única de cada imóvel  |
| date | Data que o imóvel foi vendido |
| price  | Preço de venda de cada imóvel |
| bedrooms  | Número de quartos |
| bathrooms  | Número de banheiros  |
| sqft_living  | Medida, em pés quadrados, do espaço interior dos apartamentos |
| sqft_lot  | Medida, em pés quadrados, de todo o espaço terrestre do imóvel |
| floors  | Número de andares  |
| waterfront  | "1" se possui vista para a água e "0" se não  |
| view  | Índice que quantifica, de 0 a 4, o quão boa é a vista da propriedade |
| condition  | Índice que quantifica, de 1 a 5, a condição do apartamento  |
| grade  | Um índice que quantifica, de 1 a 13, o nivel da construção e do design do edifício. 1-3 = baixo, 7 = médio e 11-13 = alto
| sqft_above  | Medida, em pés quadrados, do espaço interior acima do solo  |
| sqft_basement  | Medida, em pés quadrados, do espaço interior abaixo do solo |
| yr_built  | Ano que o imóvel foi construído  |
| yr_renovated  | Ano em que a casa foi renovada pela última vez  |
| zipcode  | Código ZIP, ou CEP, do imóvel  |
| lat  | Latitude |
| long  | Longitude  |
| sqft_living15  | Medida, em pés quadrado, do espaço interno de habitação dos 15 imóveis vizinhos mais próximos |
| sqft_lot15 | Medida, em pés quadrado, do espaço terrestre dos 15 imóveis vizinhos mais próximos |

# 4. Solution Strategy

1. Data Description
2. Feature Engineering
3. Variable Filtering
4. Exploratory Data Analysis
5. Data Preparation
6. Feature Selection
7. Machine Learning Modeling
8. Hyperparameter Fine Tuning
9. Translation and interpretation of error, model-to-Business interpretation
10. Deploy model to production


# 5. Top 4 Data Insights

![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/0f82b5ed-5925-4551-8249-326f1b656c58)


# 6. Próximos Passos

* Tornar o dashboard mais informativo e entendível;
* Adicionar uma forma de visualizar o lucro potencial de um determinado imóvel no dashboard.
