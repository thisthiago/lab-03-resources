
cd /home/thiago/work/lab-03-resources/hadoop/hive/data

docker cp . hive:/tmp/

# Cria pastas no HDFS
hdfs dfs -mkdir -p /user/hive/warehouse/categories
hdfs dfs -mkdir -p /user/hive/warehouse/customers
hdfs dfs -mkdir -p /user/hive/warehouse/employee_territories
hdfs dfs -mkdir -p /user/hive/warehouse/employees
hdfs dfs -mkdir -p /user/hive/warehouse/order_details
hdfs dfs -mkdir -p /user/hive/warehouse/orders
hdfs dfs -mkdir -p /user/hive/warehouse/products
hdfs dfs -mkdir -p /user/hive/warehouse/regions
hdfs dfs -mkdir -p /user/hive/warehouse/shippers
hdfs dfs -mkdir -p /user/hive/warehouse/suppliers
hdfs dfs -mkdir -p /user/hive/warehouse/territories

# Move os arquivos pra HDFS
hdfs dfs -put /tmp/categories.csv /user/hive/warehouse/categories/
hdfs dfs -put /tmp/customers.csv /user/hive/warehouse/customers/
hdfs dfs -put /tmp/employee-territories.csv /user/hive/warehouse/employee_territories/
hdfs dfs -put /tmp/employees.csv /user/hive/warehouse/employees/
hdfs dfs -put /tmp/order-details.csv /user/hive/warehouse/order_details/
hdfs dfs -put /tmp/orders.csv /user/hive/warehouse/orders/
hdfs dfs -put /tmp/products.csv /user/hive/warehouse/products/
hdfs dfs -put /tmp/regions.csv /user/hive/warehouse/regions/
hdfs dfs -put /tmp/shippers.csv /user/hive/warehouse/shippers/
hdfs dfs -put /tmp/suppliers.csv /user/hive/warehouse/suppliers/
hdfs dfs -put /tmp/territories.csv /user/hive/warehouse/territories/
