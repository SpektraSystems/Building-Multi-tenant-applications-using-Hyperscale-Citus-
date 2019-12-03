Connecting to Hyperscale (Citus) on Azure Database for PostgreSQL
When you create your Hyperscale (Citus) cluster, a default database named citus is created. To connect to your database server, you need a connection string and the admin password. Initial connections to Postgres may take up to 2 minutes. If for any reason your shell times out and you restart it you will need to perform the curl -s https://ifconfig.co command again and ensure the firewall is updated with the new IP address.
Connect to the database using Psql
1.	 
Click the Maximize "square" in the upper right of the Cloud Shell click to make it full screen
2.	 
At the bash prompt, connect to your Azure Database for PostgreSQL server with the Psql utility. Initial connections may take up to 2 minutes. Copy and paste the following command and press enter
psql "host=sg564758-c.postgres.database.azure.com port=5432 dbname=citus user=citus password='sp*q7nruskejja22' sslmode=require" 
•   
Click Next on the bottom right of this page
