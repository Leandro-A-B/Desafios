# DESAFIOEA
GIT utilizado pela equipe data-tote na resolução do problema proposto 
 a solução consta com a seguinte arquitetura em AWS:
 
 1º) Dados são fornecidos via FTP do ministério do trabalho, os dados extraidos são referentes aos anos de 2010 até 2019.
 
 2º) Utiliza-se o GLUE (Schedulado) para extrair os dados via FTP, o mesmo extrai os arquivos para um bucket (porém os arquivos estão zipados)
 
 3º) A Lambda é triggada quando arquivos novos são totalmente baixados e inseridos no bucket, acionando a maquina para ser ligada.
 
 4º) Com ativação da maquina, ou conjunto de maquinas, pega os arquivos no bucket zipados os baixa, descomprime e os insere em um outro bucket
 
 5º) Com o bucket recebendo novos arquivos isso trigga o GLUE e o aciona para inserir os dados no redshift, conforme solicitado
 
 6º) Com os dados disponiveis no banco de dados, é possivel linkar a um serviço de Front End para visualização das informações.
 
 #PartirProAbraço #FaturaNoisGoverno 
 
 
