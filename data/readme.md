Passo a passo para subir arquivos no HDFS desse container

Passo 1: Copiar o arquivo do host para dentro do container
docker cp orders.csv hive:/tmp/orders.csv

Passo 2: Criar uma pasta no HDFS
hdfs dfs -mkdir -p /user/hive/warehouse/orders

Passo 3: Fazer o upload do arquivo
hdfs dfs -put /tmp/orders.csv /user/hive/warehouse/orders/

Passo 4: Verificar se subiu
hdfs dfs -ls /user/hive/warehouse/
