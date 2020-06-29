# Project Charter

## Entendimento de negócio

Vinho Verde é um produto único, produzido exclusivamente na região demarcada dos Vinhos Verdes, em Portugal. Uma empresa de revenda deseja aumentar as vendas ao melhorar a indicação dos vinhos, inferindo o n~ivel de qualidade dos vinhos a partir de algumas características.

A empresa gostaria de investir numa solução baseada em dados para auxiliar os consultores da empresa em suas decisões de recomendação de qualidade. Para isso, a empresa fez uma coleta de histórico das notas de qualidade, em conjunto com um grupo de variáveis que são consideradas interessantes para o entendimento da classificação.

## Escopo

O problema de análise de qualidade do vinho pode ser abordado como um problema de classificação. Como as bases já estão avaliadas previamente, trata-se de um problema para algoritmos de treinamento supervisionado. A quantidade de possíveis valores para as classes indica que é um problema de classificação binária (bom ou ruim).

* **Problema**: classificação binária
* **Algoritmo**: treinamento supervisionado
* **Base de dados**: arquivo csv com valores numéricos
* **Variável alvo**: qualidade do vinho (bom ou ruim)

## Métricas
* Objetivo qualitativo: estimar se o vinho será considerado bom ou ruim
* Figura de mérito: f1-score.
* Benchmarking: melhor que o aleatório de 50%.
* Métrica deve ser medida sobre um conjunto de teste de 30% dos dados para cada classe.


## Planejamento
* Sprint 1: entendimento de negócio e preparação dos dados.
* Sprint 2: Análise de dados e construção de features.
* Sprint 3: Modelagem dos classificadores e avaliação dos resultados
* Sprint 4: Relatório dos resultados do modelo

## Arquitetura

* Dados:
  * Os dados são entregues através de 2 arquivos CSV. Os dados coletados são processados para saneamento e avaliação da sua qualidade.
  * Relatório de dados disponível [aqui](../DataReport/Report.md "Relatório de dados")

## Comunicação
* Equipe de desenvolvimento com reuniões diárias em modelo Scrum.
* Reuniões de status executivos a cada 3 semanas.
* Pontos de contato:
  * Empresa de Vinhos: Thiago
  * Consultoria: Camilla
