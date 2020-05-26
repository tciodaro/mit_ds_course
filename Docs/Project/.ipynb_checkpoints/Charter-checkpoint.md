# Project Charter

## Entendimento de negócio

Vinho Verde é um produto único, produzido exclusivamente na região demarcada dos Vinhos Verdes, em Portugal. Uma empresa de revenda deseja aumentar as vendas ao melhorar a indicação dos vinhos, inferindo o n~ivel de qualidade dos vinhos a partir de algumas características.


## Escopo

A empresa gostaria de investir numa solução baseada em dados para auxiliar os consultores da empresa em suas decisões de recomendação de qualidade. Para isso, a empresa fez uma coleta de histórico das notas de qualidade, em conjunto com um grupo de variáveis que são consideradas interessantes para o entendimento da classificação.

* A solução deve observar o histórico de dados e fazer a previsão dos novos vinhos.
* Os dados serão coletadas através de arquivos CSV de um servidor FTP.
* O resultado da previsão será exportado como arquivo CSV.
* O resultado pode ser consumido em relatórios estáticos.

## Pessoal
* Quem está no projeto:
	* Consultoria:
		* Project lead (Marcelo)
		* PO (Camilla)
		* Data scientist(s) (Octavio)
		* Account manager (Oliveira)
	* Retail Co:
		* Data administrator
		* Business contact

## Métricas
* Objetivo qualitativo: obter uma acuracia de 90%.
* Figura de mérito: erro absoluto percentual médio (MAPE)
* Benchmarking: processo atual trabalha com um MAPE de aproximadamente 50%.
* Métrica deve ser medida sobre todo o histórico de teste, que possui o mesmo comprimento que o horizonte de previsão da ferramenta.


## Planejamento
O projeto deve ser realizado em 5 semanas. Está prevista uma sessão de design thinking para o entendimento e a passagem de conhecimento entre os especialistas do negócio e a equipe de cientistas de dados (representada pelo PO).
* Semana 1: entendimento de negócio, sessões de transferencia de conhecimento e planejamento desenho da solução.
* Semana 2 e 3: ciclos de desenvolvimento da solução inicial (sprints).
* Semana 4: geração de relatórios e documentação.
* Semana 5: apresentação dos resultados finais e transferência de conhecimento.

## Arquitetura

* Dados:
  * Os dados são entregues através de 2 arquivos CSV, lidos de uma conexão FTP. Os dados coletados são processados para saneamento e avaliação da sua qualidade.
  * A série histórica possui aproximadamente 2 anos.
  * Os arquivos possuem 11 atributos + output

* Modelos:
  * Será desenvolvido um modelo de auto ML para a previsão das séries temporais.
  * Os modelos serão desenvolvidos utilizando o Azure ML.
  * O treinamento dos modelos aproveitará a tecnologia Spark via utilização do ambiente Databricks.

* Relatórios:
  * Os relatórios serão feitos após o processamento do treinamento dos modelos.
  * Os relatórios são disponibilizados como exportações HTML dos notebooks utilizados.



## Comunicação
* Equipe de desenvolvimento com reuniões diárias em modelo Scrum.
* Reuniões de status executivos a cada 3 semanas.
* Pontos de contato:
  * Retail Co.: Soares
  * Consultoria: Thiago
