# Alterações na fonte de dados do relatótio de Indicadores da Assistência Técnica
Mudanças aplicadas para facilitar a atualização de inclusão de novas tabelas no serviço desktop do Power BI adquirindo e processando-as no ambiente Azure.

Incluiu-se cada tabela utilizada no Power BI em um DataFactory Azure a fim de as tabelas já chegarem prontas para serem aplicadas, sem necessidade de, ou pelo menos reduzindo, tratamentos dentro do BI.

<!-- Entretanto, algumas das tabelas, tais como f_TempoEntreManutencoes e f_Ttr, partem da mesma fonte de dados. Assim, não há necessidade de duplicar as entradas criando uma tabela no ambiente interno Azure para cada tabela no Power BI. -->

A aquisição de dados ocorreu por um pipeline conectando as fontes de dados originais ao DataLake implementado. Para facilitar o processo, foi criado um arquivo JSON com todas as tabelas presentes no BI, as suas consultas geradoras e seus destinos dentro do DataLake.