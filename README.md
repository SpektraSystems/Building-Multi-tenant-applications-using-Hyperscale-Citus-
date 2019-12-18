# Multi-tenant Applications

This experience will take you through the process of creating a multi-tenant application on Hyperscale(Citus) on Azure Database for PostgreSQL.

If you’re building a Software-as-a-service (SaaS) application, you probably already have the notion of tenancy built into your data model. Typically, most information relates to tenants / customers / accounts and the database tables capture this natural relation.
For SaaS applications, each tenant’s data can be stored together in a single database instance and kept isolated from and invisible to other tenants. This is efficient in three ways. Firstly, application improvements apply to all clients. Secondly, sharing a database between tenants uses hardware efficiently. Finally, it is much simpler to manage a single database for all tenants than a different database server for each tenant.

However, a single relational database instance has traditionally had trouble scaling to the volume of data needed for a large multi-tenant application. Developers were forced to relinquish the benefits of the relational model when data exceeded the capacity of a single database node.

Hyperscale(Citus) allows users to write multi-tenant applications as if they are connecting to a single PostgreSQL database, when in fact the database is a horizontally scalable cluster of machines. Client code requires minimal modifications and can continue to use full SQL capabilities.

This guide takes a sample multi-tenant application and describes how to model it for scalability with Hyperscale(Citus). Along the way we examine typical challenges for multi-tenant applications like isolating tenants from noisy neighbors, scaling hardware to accommodate more data, and storing data that differs across tenants. Hyperscale(Citus) on Azure Database for PostgreSQL provides all the tools needed to handle these challenges, so let’s get building.

1. Click **Next** at the bottom right of this window.

