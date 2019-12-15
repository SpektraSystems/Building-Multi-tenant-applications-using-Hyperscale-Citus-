# Connecting to Hyperscale(Citus) on Azure Database for PostgreSQL

When you create your Hyperscale(Citus) cluster, a default database named citus is created. To connect to your database server, you need a connection string and the admin password. Initial connections to Postgres may take up to 2 minutes. If for any reason your shell times out and you restart it you will need to perform the curl -s https://ifconfig.co command again and ensure the firewall is updated with the new IP address.

## **Lab 3: Connect to the database using Psql**

1.Click the **Maximize square** in the upper right of the Cloud Shell click to make it full screen.

2.At the bash prompt, connect to your Azure Database for PostgreSQL server with the Psql utility. Copy and paste the following command in a text editor.

```
psql "host=srvxxx.postgres.database.azure.com port=5432 dbname=citus user=citus sslmode=require" 
```

3.Replace **host** with - Go to Azure Database for PostgreSQL server,open your **postgrexxxx** server,then from the top-right corner copy **Coordinator Name** or **PostgreSQL Database hostname** given in **environment details** tab.

4.The final command should look similar to the one shown below. Paste the command in bash console and press **enter**.
```
psql "host=srv131057.postgres.database.azure.com port=5432 dbname=citus user=citus sslmode=require"
```

5.When asked for password, enter **Password.1!!** and press **enter**.

6.Now you will get connected to **Hyperscale(Citus)** database server.

   ![](Images/quey1.png)

7.Click **Next** on the bottom right of this page.
  
