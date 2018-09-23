## ElasticSearch
**ElasticSearch** is **an Open-source Enterprise REST based Real-time Search and Analytics Engine**. It’s *core Search Functionality* is built using Apache Lucene, but supports many other features.

Elasticsearch is a **highly scalable open-source full-text search and analytics engine**. It *allows you to store, search, and analyze big volumes of data quickly* and in near real time. It is generally used as the underlying engine/technology that powers applications that have complex search features and requirements.

It is *written in Java Language*. It **supports Store, Index, Search and Analyze Data in Real-time**. *Like MongoDB*, **ElasticSearch is also a Document-based NoSQL Data Store**.

#### ElasticSearch Features
- An Open-source
- Supports Full-text Simple and Powerful Search
- Supports REST Based API (JSON over HTTP)
- Supports Real-time Search and Analytics
- By Definition, Distributed
- Supports Multi Tenancy Feature
- Support Cloud and Big Data Environments
- Supports Cross-platform
- Denormalized NoSQL Data Store

#### Advantages or Benefits of ElasticSearch
- An Open-source
- Light Weight with REST API
- Highly Available. Easily and Highly Scalable
- Supports Caching Data
- Schema Free
- Fast Search Performance
- Supports both Structured and UN-Structured Data
- Supports Distributed, Sharding, Replication, Clustering and Multi-Node Architecture
- Supports Bulk Operations
- Build Charts and Dashboards within no time

#### Drawbacks or Limitations of ElasticSearch
- Does NOT support MapReduce operations
- Not useful as a Primary Data Store
- Not an ACID compliant Data Store
- Does not support Transactions and Distributed Transactions
- Does NOT have built-in authentication or authorization feature

#### Popular Clients who are using ElasticSearch
- Github.com, Quora.com, Stackoverflow.com
- eBay, DELL, Cisco, Mozilla, Wikimedia
- Netflix, Symatics, Facebook
- UK HMRC (HM Revenue & Customs)

For instance, Github.com uses ElasticSearch to search files, history, ticket numbers etc. Most of the companies uses ELK stack to manage their logs and to monitor their systems. ELK stands for ElasticSearch Logstash and Kibana

**NOTE** You can find a more Customer’s use-cases at https://www.elastic.co/use-cases

#### *Sample use-cases** that Elasticsearch could be used for
- You run an online web store where you allow your customers to search for products that you sell. In this case, you can use Elasticsearch to store your entire product catalog and inventory and provide search and autocomplete suggestions for them.

- You want to collect log or transaction data and you want to analyze and mine this data to look for trends, statistics, summarizations, or anomalies. In this case, you can use Logstash (part of the Elasticsearch/Logstash/Kibana stack) to collect, aggregate, and parse your data, and then have Logstash feed this data into Elasticsearch. Once the data is in Elasticsearch, you can run searches and aggregations to mine any information that is of interest to you.

- You run a price alerting platform which allows price-savvy customers to specify a rule like "I am interested in buying a specific electronic gadget and I want to be notified if the price of gadget falls below $X from any vendor within the next month". In this case you can scrape vendor prices, push them into Elasticsearch and use its reverse-search (Percolator) capability to match price movements against customer queries and eventually push the alerts out to the customer once matches are found.
- You have analytics/business-intelligence needs and want to quickly investigate, analyze, visualize, and ask ad-hoc questions on a lot of data (think millions or billions of records). In this case, you can use Elasticsearch to store your data and then use Kibana (part of the Elasticsearch/Logstash/Kibana stack) to build custom dashboards that can visualize aspects of your data that are important to you. Additionally, you can use the Elasticsearch aggregations functionality to perform complex business intelligence queries against your data.
- For the rest of this tutorial, you will be guided through the process of getting Elasticsearch up and running, taking a peek inside it, and performing basic operations like indexing, searching, and modifying your data. At the end of this tutorial, you should have a good idea of what Elasticsearch is, how it works, and hopefully be inspired to see how you can use it to either build sophisticated search applications or to mine intelligence from your data.

## ElasticSearch REST API URL Basics
![elasticsearch-rest_url](https://user-images.githubusercontent.com/36996525/45923517-53b6d480-bf06-11e8-929b-eb51bb7a1949.png)

**Here**
- Server means any server name or host name like “myserver”. Sometimes we use Node + Port number like “myhost:9999”.
- Index must be in lower case, otherwise it throws an Exception.
- It is recommended to use Type also in lower case.

**Basic Concepts**
There are a few concepts that are core to Elasticsearch. Understanding these concepts from the outset will tremendously help ease the learning process.

**Near Realtime (NRT)** Elasticsearch is a near real time search platform. What this means is there is a slight latency (normally one second) from the time you index a document until the time it becomes searchable.

**Cluster** A cluster is a collection of one or more nodes (servers) that together holds your entire data and provides federated indexing and search capabilities across all nodes. A cluster is identified by a unique name which by default is "elasticsearch". This name is important because a node can only be part of a cluster if the node is set up to join the cluster by its name.

Make sure that you don’t reuse the same cluster names in different environments, otherwise you might end up with nodes joining the wrong cluster. For instance you could use logging-dev, logging-stage, and logging-prod for the development, staging, and production clusters.

Note that it is valid and perfectly fine to have a cluster with only a single node in it. Furthermore, you may also have multiple independent clusters each with its own unique cluster name.

**Node** A node is a single server that is part of your cluster, stores your data, and participates in the cluster’s indexing and search capabilities. Just like a cluster, a node is identified by a name which by default is a random Universally Unique IDentifier (UUID) that is assigned to the node at startup. You can define any node name you want if you do not want the default. This name is important for administration purposes where you want to identify which servers in your network correspond to which nodes in your Elasticsearch cluster. 
A node can be configured to join a specific cluster by the cluster name. By default, each node is set up to join a cluster named elasticsearch which means that if you start up a number of nodes on your network and—assuming they can discover each other—they will all automatically form and join a single cluster named elasticsearch.

In a single cluster, you can have as many nodes as you want. Furthermore, if there are no other Elasticsearch nodes currently running on your network, starting a single node will by default form a new single-node cluster named elasticsearch.

**Index** An index is a collection of documents that have somewhat similar characteristics. For example, you can have an index for customer data, another index for a product catalog, and yet another index for order data. An index is identified by a name (that must be all lowercase) and this name is used to refer to the index when performing indexing, search, update, and delete operations against the documents in it.
In a single cluster, you can define as many indexes as you want.

**Document** A document is a basic unit of information that can be indexed. For example, you can have a document for a single customer, another document for a single product, and yet another for a single order. This document is expressed in JSON (JavaScript Object Notation) which is a ubiquitous internet data interchange format.

Within an index/type, you can store as many documents as you want. Note that although a document physically resides in an index, a document actually must be indexed/assigned to a type inside an index.
