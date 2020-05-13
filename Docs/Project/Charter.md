# Project Vivino AI

## Entendimento de negócio

Um cliente importador de vinhos portugueses deseja aumentar as suas vendas e para isso necessita de classificar alguns vinhos por nota de 0 a 10 de acordo com uma base de avaliação de vinhos portugueses. 

## Escopo

A empresa gostaria de investir numa solução baseada em dados para auxiliar os consultores da empresa em suas decisões de planejamento de vendas e logística. Para isso, a empresa utilizou uma base histórica, em conjunto com um grupo de variáveis que são consideradas interessantes para o entendimento do volume de vendas.

* A solução deve observar o histórico de dados e prover uma avaliação, por nota de qualidade para cada vinho
* Os dados serão coletadas através de arquivos CSV.
* O resultado da previsão será exportado como arquivo CSV.
* O resultado pode ser consumido em relatórios estáticos.

## Pessoal
* Quem está no projeto:
	* Consultoria:
		* Project lead (Marcelo)
		* PO (Camilla)
		* Data scientist(s) (Octavio)
		* Account manager (Edimilson)
	* Vivino:
		* Data administrator (Maria José)
		* Business contact (Anderson)

## Métricas
* Objetivo qualitativo: Acurácia igual ou superior a 90%. Quantidade de acertos de avaliação por quantidade de existentes
* Figura de mérito: erro absoluto percentual médio (MAPE)
* Benchmarking: processo atual trabalha com um MAPE de aproximadamente 50%.
* Métrica deve ser medida sobre todo o histórico de teste.


## Planejamento
O projeto deve ser realizado em 1 mes. Está prevista a passagem de conhecimento entre os especialistas do negócio e a equipe de cientistas de dados (representada pelo PO).
* Semana 1: entendimento de negócio, sessões de transferencia de conhecimento e planejamento desenho da solução.
* Semana 2 e 3: ciclos de desenvolvimento da solução inicial (sprints).
* Semana 4: geração de relatórios e documentação e apresentação dos resultados finais e transferência de conhecimento.

## Arquitetura

* Dados:
  * Os dados são entregues através de 2 arquivos CSV, entregues por uma empresa especializada em pesquisas. Os dados coletados são processados para saneamento e avaliação da sua qualidade.
  * A série histórica possui aproximadamente 7000 registros.
  * São coletadas 12 variáveis exógenas.

* Modelos:
  * Será desenvolvido um modelo de ML para a previsão da qualidade dos vinhos.
  * Os modelos serão desenvolvidos utilizando jupyter notebooks.

* Relatórios:
  * Os relatórios serão feitos após o processamento do treinamento dos modelos.
  * Os relatórios são disponibilizados como exportações HTML dos notebooks utilizados.



## Comunicação
* Equipe de desenvolvimento com reuniões diárias em modelo Scrum.
* Reuniões de status executivos a cada semana.
* Pontos de contato:
  * Vivino Co.: Anderson 
  * Consultoria: Edimilson
