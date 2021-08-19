# Getting started with Hyperscale(Citus) extension for PostgreSQL

The Hyperscale(Citus) on Azure Database for PostgreSQL service uses a firewall at the server-level. By default, the firewall prevents all external applications and tools from connecting to the coordinator node and any databases inside. We must add a rule to open the firewall for a specific IP address range.

We pre-provisioned a basic production grade Hyperscale(Citus) cluster with 1 coordinator with 4 vCores and 16GB RAM and 2 workers with each 2 vCores and 16GB RAM for this lab.

## **Lab 2: Configure a server-level firewall rule**

1.Navigate to **Home** in Azure Portal. Then under Azure services click **Azure Database for PostgreSQL servers**. 

  ![](Images/postgresql.png)

2.Select the pre-cretead database **postgresxxxx**.

  ![](Images/postgresql1.png)

3.On the overview blade under **Settings** click **Networking** and **select** the **"Allow public access from Azure services and resources within Azure to this server group"** .

![](https://github.com/Shivashant25/Building-Multi-tenant-applications-using-Hyperscale-Citus-/blob/master/Images/l2%20s3.png?raw=true)

4.Now add **Firewall Rule**. Select **Add current client IP address**, this will add the client IP by creating a new rule. Then **save** the changes.

![](https://github.com/Shivashant25/Building-Multi-tenant-applications-using-Hyperscale-Citus-/blob/master/Images/l2%20s4.png?raw=true)

> **Note**: Hyperscale(Citus) server communicates over port 5432. If you are trying to connect from within a corporate network, outbound traffic over port 5432 may not be allowed by your network's firewall. If so, you cannot connect to your Hyperscale(Citus) server unless your IT department opens port 5432.

5.Click **Next** on the bottom right of this page.

