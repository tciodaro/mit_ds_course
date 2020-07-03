# Relatório de Modelagem

Documento para registrar as análises e a modelagem desenvolvida.


## Análise de Dados

Foram feitas análises de distribuição agrupadas pela variável alvo (quality).


### Distribuição

Na análise da distribuição foi verificado que as variáveis volatile acidity, residual sugar e principalmente alcohol possuem caudas maiores, enquanto as outras ficam mais próximas de uma distribuição normal.

Foi analisada a distribuição das variáveis agrupadas por qualidade, e nota-se que as variáveis volatile acidity, citric acid, density, ph e alcohol possuem visualmente uma maior diferenciação entre os valores de qualidade.

### Correlação com a variável alvo

Foi analisada a correlação entre as variáveis com a variável alvo (quality) e as variáveis com maior correlação são volatile acidity, chlorides, density e alcohol, seguidas por fixed acidity e citric acid. 

Também foi criado um pair plot entre as variáveis com maior correlação agrupadas pela qualidade.

## Próximos passos

Após a análise preliminar, devemos seguir com o treinamento dos modelos de classificação, utilizando validação cruzada como forma de estimar os hiper-parâmetros do modelo que conseguem a melhor generalização possível.

