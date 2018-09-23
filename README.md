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


