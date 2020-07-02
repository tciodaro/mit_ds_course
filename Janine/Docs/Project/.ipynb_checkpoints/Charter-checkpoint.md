
https://www.youtube.com/watch?v=zafw717Jhx0
## Project Charter

### Entendimento de negócio
Todos nós reconhecemos a importância da energia elétrica que ilumina e proporciona qualidade de vida
aos 200 milhoes de brasileiros que vivem neste país. Esta energia é produzida nas Usinas
e transportadas pelas linhas de transmissão que forma uma rede básica, cruzam por subestações,
percorrem a rede de distribuição até, por fim, chegar as residências, industriais e comércios das cidades.

Esta rede é composta por diversos equipamentos, como linhas de transmissão, disjuntores, transformafores, 
chaves e outros, que em harmonia, permitem que a energia seja gerada, transportada para ser consumida. 
Estes equipamentos são dispositivos mecânicos ou motores, que tem uma vida finita e precisam de manutenção periódica.

Dentre os equipamentos, parte tem seu funcionamento supervisionado por uma empresa que opera esta rede básica,
e a outra parte tem a sua supervisão realizada pelo proprietário do equipamento elétrico. 
As manutenções realizadas, como mencionado acima, tem um texto descritivo associado.

Assim, o projeto consiste em utilizar os textos descritivos, e a partir da avaliação da grafia,
estimar quem seria o responsável pela supervisão do equipamento que está em manutenção.

Em analogia a estimação de sentimentos, a construção da base de dados considerou que 
os equipamentos supervisionados serão classificados como *Positivo*(**POS**), e os outros *Negativo*(**neg**) 
de acordo com o texto avaliados.

Deseja-se utilizar a informação dos comentários escritos nas avaliações para prever o sentimento do 
avaliador pelo filme (**pos** ou **neg**). 




## Escopo

O problema de análise de sentimento pode ser abordado como um problema de classificação. Como as bases já estão avaliadas previamente, trata-se de um problema para algoritmos de treinamento supervisionado. A quantidade de possíveis valores para as classes indica que é um problema de classificação binária.

* **Problema**: classificação binária
* **Algoritmo**: treinamento supervisionado
* **Base de dados**: arquivo csv com comentários de texto livre
* **Variável alvo**: Sentimento positivo ou negativo

## Métricas
* Objetivo qualitativo: estimar o sentimento de comentários sobre filmes.
* Figura de mérito: f1-score.
* Benchmarking: melhor que o aleatório de 50%.
* Métrica deve ser medida sobre um conjunto de teste de 20% dos dados para cada classe.


## Planejamento
* Sprint 1: entendimento de negócio e preparação dos dados.
* Sprint 2: Análise de dados e construção de features.
* Sprint 3: Modelagem dos classificadores e avaliação dos resultados
* Sprint 4: Relatório dos resultados do modelo

## Arquitetura

* Dados:
  * Os dados são entregues através de 1 arquivo CSV
  * Relatório de dados disponível [aqui](../DataReport/Report.md "Relatório de dados")

* Modelos:
  * Classificador binário para estimar a probabilidade do comentário ter sentimento positivo.
  * Será utilizado um modelo linear de Regressão Logística.
  * Serão utilizados dois modelos não-lineares: RandomForest e SVM.
  * Os hiper-parâmetros dos modelos serão ajustados segundo uma busca exaustiva em grid-search.
  * A base de dados será dividida em treino (80%) e teste (20%), mantendo a proporção de classes nos dois conjuntos de dados.
  * Os modelos serão avaliados considerando o conjunto de teste.
  * Os modelos e as análises sobre os dados podem ser estudadas [aqui](../Model/Report.md "Relatório de modelagem")
  
  
* Entregáveis:
  * Apresentação com os resultados mais relevantes.
  * Base de dados de teste com a probabilidade de sentimento positivo dos comentários, em arquivo Excel.



## Comunicação
* Equipe de desenvolvimento com reuniões diárias em modelo Scrum.
* Reuniões de status executivos a cada 3 semanas.
* Pontos de contato:
  * Retail Co.: Soares
  * Consultoria: Thiago
