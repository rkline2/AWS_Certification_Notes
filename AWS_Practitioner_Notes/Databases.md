## NoSQL Database Services

**[DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html)** ***(When we want a massively scalable database)*** - is a serverless NoSQL key/value and document database. It is designed to scale to billions of records with guaranteed consistent data return in at least a second. You don’t have to worry about managing shards! 

    DynamoDB is AWS’s flagship database service meaning whenever we think of a database service that just scales, is cost effective and very fast we should think DynamoDB 

**[DocumentDB](https://aws.amazon.com/documentdb/)** ***(When you want a MongoDB database)***- is a NoSQL document database that is “MongoDB compatible”​

    MongoDB is very popular NoSQL among developers. There were open-source licensing issues around using open-source MongoDB, so AWS got around it by just building their own MongoDB database.​ 

**[Amazon Keyspaces](https://docs.aws.amazon.com/keyspaces/latest/devguide/what-is-keyspaces.html)** ***(When you want to use Apache Casandra)***- is a fully managed Apache Cassandra database. Cassandra is an open-source NoSQL key/value database similar to DynamoDB in that is columnar store database but has some additional functionality. When you want to use Apache Casandra.

----

## Relational Database Services

**[Relational Database Service (RDS)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)** - is a relational database service that supports multiple SQL engines. Relational is synonymous with SQL and Online Transactional Processing (OLTP). Relational database are the most commonly used type of database among tech companies and start-ups. ​

RDS Supports the following SQL Engines: ​

* **MySQ**L – The most popular open-source SQL database that was purchased and now owned by Oracle.​

* **MariaDB** – When Oracle bought MySQL a fork (copy) of MySQL was made under a different open-source license.​

* **Postgres (PSQL)** – Most popular open-source SQL database among developers. Has rich-features over MySQL but at added complexity​

* **Oracle** – Oracle’s proprietary SQL database. Well used by Enterprise companies. You have to buy a license to use it.​

* **Microsoft SQL Server** – Microsoft’s proprietary SQL database. You have to buy a license to use it.​

* **Aurora** – Fully managed database.

**[Aurora](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html)** - is a fully managed database of either MySQL (5x faster) and PSQL (3x faster) database.​ When you want a highly available, durable, scalable and secure relational database for Postgres or MySQL​

**[Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html)** - is the serverless on-demand version of Aurora. When you want “most” of the benefits of Aurora but can trade to have cold-starts or you don’t have lots of traffic demand​

**[RDS on VMware](https://aws.amazon.com/rds/vmware/)** - allows you to deploy RDS supported engines to on an-premise data-center. The datacenter must be using VMware for server virtualization. When you want databases managed by RDS on your own datacenter​

----

**[Relational Database Service (RDS)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)** - is a relational database service that supports multiple SQL engines. Relational is synonymous with SQL and Online Transactional Processing (OLTP). Relational database are the most commonly used type of database among tech companies and start-ups. ​

RDS Supports the following SQL Engines: ​

* MySQL – The most popular open-source SQL database that was purchased and now owned by Oracle.​

* MariaDB – When Oracle bought MySQL a fork (copy) of MySQL was made under a different open-source license.​

* Postgres (PSQL) – Most popular open-source SQL database among developers. Has rich-features over MySQL but at added complexity​

* Oracle – Oracle’s proprietary SQL database. Well used by Enterprise companies. You have to buy a license to use it.​

* Microsoft SQL Server – Microsoft’s proprietary SQL database. You have to buy a license to use it.​

* Aurora – Fully managed database.

**[Aurora](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html)** - is a fully managed database of either MySQL (5x faster) and PSQL (3x faster) database.​ ***When you want a highly available, durable, scalable and secure relational database for Postgres or MySQL​***

**[Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html)** - is the serverless on-demand version of Aurora. ***When you want “most” of the benefits of Aurora but can trade to have cold-starts or you don’t have lots of traffic demand​***

**[RDS on VMware](https://aws.amazon.com/rds/vmware/)** - allows you to deploy RDS supported engines to on an-premise data-center. The datacenter must be using VMware for server virtualization. ***When you want databases managed by RDS on your own datacenter​***

----

## Other Database Services

**[Redshift](https://docs.aws.amazon.com/redshift/latest/gsg/getting-started.html)** - is a petabyte-size data-warehouse. Data-warehouses are for Online Analytical Processing (OLAP)​ Data-warehouses can be expensive because they are keeping data “hot”. Meaning that we can run a very complex query and a large amount of data and get that data back very fast.​ ***When you want to quickly generate analytics or reports from a large amount of data.​***

**[ElastiCache](https://aws.amazon.com/elasticache/)** - is a managed database of the in-memory and caching open-source databases Redis or Memcached. ***When you need to improve the performance of application by adding a caching layer in-front of web-server or database.​***

**[Neptune](https://aws.amazon.com/neptune/)** - is a managed graph database. Data is represented as interconnected nodes.​ ***When you need to understand the connections between data eg. Mapping Fraud Rings or Social Media relationships​.***

**[Amazon Timestreams](https://aws.amazon.com/timestream/)** - is a fully managed time series database. Think of devices that send lots of data that are time-sensitive such as IoT devices. ***When you need to measure how things change over time.​***

**[Amazon Quantum Ledger Database](https://aws.amazon.com/qldb/)** - is a fully managed ledger database that provides transparent, immutable and cryptographically variable transaction logs. ​

**[Database Migration Service (DMS)](https://aws.amazon.com/dms/)** - is database migration service. You can us it to migrate from:​

* on-premise database to AWS​

* from two database in different or the same AWS accounts using different SQL engines​

* from an SQL to NoSQL database​

