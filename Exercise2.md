# Getting started with Hyperscale (Citus) extension for PostgreSQL

The Hyperscale (Citus) on Azure Database for PostgreSQL service uses a firewall at the server-level. By default, the firewall prevents all external applications and tools from connecting to the coordinator node and any databases inside. We must add a rule to open the firewall for a specific IP address range.

We pre-provisioned a basic production grade Hyperscale (Citus) cluster with 1 coordinator with 4 vCores and 16GB RAM and 2 workers with each 2 vCores and 16GB RAM for this lab.

1. On the left side navigation of the overview pane under **Security** click **Networking**. Enter the IP address from your Cloud Shell in the **START IP** and **END IP** boxes and for Firewall Rule Name enter **CloudShell**.
Then click **Save** at the top left of the pane.

  ![](Images/firewall.png)
   
> **Note**: Hyperscale (Citus) server communicates over port 5432. If you are trying to connect from within a corporate network, outbound traffic over port 5432 may not be allowed by your network's firewall. If so, you cannot connect to your Hyperscale (Citus) server unless your IT department opens port 5432.

2. Click **Next** on the bottom right of this page.

