# Project Charter

## Entendimento de negócio

Divino é uma empresa que vende vinhos pela internet, com larga experiência no ramo, e frequentemente aposta em vinhos novos que acrescenta à lista de produtos disponíveis na plataforma. Esses vinhos são oferecidos aos clientes por campanhas de marketing e são divulgados no site como lançamentos. As campanhas de marketing são direcionadas aos clientes com base no perfil consumidor daquele cliente.

## Escopo

A empresa gostaria de investir numa solução para fazer avaliações sobre a qualidade dos novos vinhos na plataforma, que ainda não foram avaliados pelos clientes. Com esses resultados pretende orientar as campanhas de marketing e ofertar novos produtos aos clientes a partir de seu perfil consumidor. Para isso a empresa fez uma listagem de seus produtos com suas características físico químicas a partir de sua base de vinhos já comercializados e avaliados pelos clientes.

* A solução deve observar as características dos vinhos conhecidos e estimar a qualidade dos novos vinhos.
* Os dados serão coletadas através de arquivos CSV de um servidor FTP.
* O resultado da previsão será exportado como arquivo CSV.
* O resultado pode ser consumido por um webservice.

## Pessoal
* Quem está no projeto:
	* Consultoria:
		* Project lead (Thiago)
		* PO (Thiago)
		* Data scientist(s) (Edmilson Prata)
		* Account manager (Oliveira)
	* Retail Co:
		* Data administrator
		* Business contact

## Métricas
* Objetivo qualitativo: estimar a qualidade de novos vinhos em baixa e alta.
* Figura de mérito: precisão.
* Benchmarking: processo atual trabalha com uma precisão de aproximadamente 50%.
* Métrica deve ser medida sobre todo o histórico de teste.


## Planejamento
O projeto deve ser realizado em 2 meses. Está prevista uma sessão de design thinking para o entendimento e a passagem de conhecimento entre os especialistas do negócio e a equipe de cientistas de dados (representada pelo PO).
* Semana 1: entendimento de negócio, sessões de transferencia de conhecimento e planejamento desenho da solução.
* Semana 2-6: ciclos de desenvolvimento da solução inicial (sprints).
* Semana 7: geração de relatórios e documentação.
* Semana 8: apresentação dos resultados finais e transferência de conhecimento.

## Arquitetura

* Dados:
  * Os dados são entregues através de 2 arquivos CSV, lidos de uma conexão FTP. Os dados coletados são processados para saneamento e avaliação da sua qualidade.
  * Os arquivos serão unificados em um único contendo todos os vinhos.
  * A série possui 6497 linhas.
  * São coletadas 12 variáveis.

* Modelos:
  * Será desenvolvido um modelo de classificação para classificar o vinho entre alta e baixa qualidade.
  * Os modelos serão desenvolvidos utilizando o Anaconda em ambiente local.
  * O treinamento dos modelos aproveitará blibliotecas em python.

* Relatórios:
  * Os relatórios serão feitos após o processamento do treinamento dos modelos.
  * Os relatórios são disponibilizados como exportações HTML dos notebooks utilizados.

## Comunicação
* Equipe de desenvolvimento com reuniões diárias em modelo Scrum.
* Reuniões de status executivos a cada 3 semanas.
* Pontos de contato:
  * Retail Co.: Soares
  * Consultoria: Edmilson Prata
