# tutorial-wildfly-com-vscode
## Step 1:
  Dentro do diretorio do wildfly em: ```/modules/system/layers/base/org/``` deve ser criada uma pasta chamada ```/postgresql/main``` e colocado o jar do postgres nela junto de um arquivo .xml chamado module.xml .
## Step 2:
 Após, no diretorio ```/bin```, execute o arquivo ```.standalone``` e em outra aba do terminal rode o comando ```./jboss-cli.sh  --connect --controller=[endereço_de_onde_o_wildfly_esta_rodando]:9990 --commands="/subsystem=datasources/jdbc-driver=postgresql:add(driver-name=\"postgresql\", driver-module-name=\"org.postgresql\", driver-class-name=\"org.postgresql.Driver\", driver-xa-datasource-class-name=\"org.postgresql.xa.PGXADataSource\")"```.

## Step 3:
  Pare a aplicação, e no vscode start o wildfly
