# Project Charter

## Entendimento de negócio

Homes North of Boston é uma empresa que presta consultoria para pessoas que querem vender ou comprar imóveis, fornecendo também suporte durante a transação. A Homes North of Boston realiza um atualização periódica do valor dos imóveis nas diversas regiões de Boston, para que possa repassar aos seus clientes valores que se aproximem ao máximo da realidade do mercado.  Além disso ela necessita de um método eficiente que lhe permita predizer o valor de um novo imóvel, tendo como base outros, cujos valores já sejam conhecidos. 



## Escopo

A empresa gostaria de investir numa solução baseada em dados para auxiliar os consultores a avaliar corretamente o valor do imóveis postos para venda.  A avaliação deverá ser feita tendo como base diversos parâmetros, vinculados a outras casas que já foram vendidas na região, como: área da casa, número de quartos, número de banheiros, etc. 

* Os dados serão coletadas através de arquivos CSV de um servidor FTP.
* O resultado da previsão será exportado como arquivo CSV.
* O resultado pode ser consumido em relatórios estáticos.

## Pessoal
* Quem está no projeto:
	* Consultoria:
		* Project lead (Thiago)
		* PO (Thiago)
		* Data scientist(s) (Nascimento, Cristiano)
		* Account manager (Oliveira)
	* Homes North of Boston:
		* Data administrator
		* Business contact

## Métricas
* Objetivo qualitativo: possibilitar avaliação mais precisa do valor de uma casa. 
* Figura de mérito: erro médio absoluto (MAE), erro quadrático médio (MSE) e raiz do erro quadrático médio (RMSE)
* Benchmarking: predição dos valores aceitam um RMSE de no máximo, 10% do valor médio dos imóveis. 


## Planejamento
O projeto deve ser realizado em 2 meses. Está prevista uma sessão de design thinking para o entendimento e a passagem de conhecimento entre os especialistas do negócio e a equipe de cientistas de dados (representada pelo PO).
* Semana 1: entendimento de negócio, sessões de transferencia de conhecimento e planejamento desenho da solução.
* Semana 2-6: ciclos de desenvolvimento da solução inicial (sprints).
* Semana 7: geração de relatórios e documentação.
* Semana 8: apresentação dos resultados finais e transferência de conhecimento.

## Arquitetura

* Dados:
  * Os dados são entregues através de 3 arquivos CSV, lidos de uma conexão FTP. Os dados coletados são processados para saneamento e avaliação da sua qualidade.
  * A série histórica possui aproximadamente 2 anos.
  * São coletadas 10 variáveis exógenas.

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
