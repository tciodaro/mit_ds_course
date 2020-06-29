
# Relatório de Dados

Esse relatório das bases de dados do projeto.


## Bases de dados


| Nome Dataset | Origem   | Destino  | Script |
| ---:| ---: | ---: | ---: | -----: |
| Wine| Red Wine + White Wine | Processado para qualidade de dados | [data_prep.ipynb](../../Code/DataPrep/data_perp.ipynb) | 


* Base de Vinhos

Possui as seguintes colunas: 'fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', 'quality'

Os arquivos foram combinados e foram adicionadas duas colunas indicando o tipo do vinho: 'red' e 'white'

Todas as colunas exceto 'quality', 'red' e 'white' são do tipo float.




