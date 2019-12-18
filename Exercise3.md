# Connecting to Hyperscale(Citus) on Azure Database for PostgreSQL

When you create your Hyperscale(Citus) cluster, a default database named citus is created. To connect to your database server, you need a connection string and the admin password. Initial connections to Postgres may take up to 2 minutes. If for any reason your shell times out and you restart it you will need to perform the curl -s https://ifconfig.co command again and ensure the firewall is updated with the new IP address.

## **Lab 3: Connect to the database using Psql**

1.Navigate to **Home** in Azure Portal. Then under Azure services click on **Azure Database for PostgreSQL servers**. 

  ![](Images/postgresql.png)

2.Select the pre-cretead database **postgresxxxx**.

  ![](Images/postgresql1.png)

3.Select **Connection Strings** under **Security** pane. Then copy the connection string given under **psql** and paste it in a text editor.

  ![](Images/connstr1.png)

4.Replace **{your_password}** with **Password123**. The final connection string should look similar to the one shown below. 

```
psql "host=srv135800.postgres.database.azure.com port=5432 dbname=citus user=citus password=Password123 sslmode=require"
```

5.Paste the connection string in bash console and press **enter**. You will get connected to **Citus** database server.

  ![](Images/citusnew.png)

7.Click **Next** on the bottom right of this page.
  
