---
layout: default
---

# mm-ADT
## A Multi-Model Abstract Data Type

<a href="https://github.com/mm-adt"><img src="assets/images/github-icon.png" alt="GitHub" width="35" /></a>
<a href="http://twitter.com/_mmadt"><img src="assets/images/twitter-icon.png" alt="Twitter" width="35" /></a>

<img src="assets/images/mm-adt-logo.png" alt="mm-ADT" width="175" style="float:right;"/> mm-ADT&#8482; is a distributed virtual machine designed to integrate data-oriented technologies. This is accomplished via three language-agnostic interfaces. When a technology implements a respective interface, the technology is considered _mm-ADT compliant_ and can communicate with any other mm-ADT compliant technologies. In this manner, query language developers can develop languages irrespective of the underlying storage system that will ultimately be manipulated by the language. Processing engines can be programmed by any query language and used over any storage system. Finally, data storage systems automatically support all mm-ADT compliant query languages and processors.

<img src="assets/images/lang-proc-store.png" alt="mm-ADT Components" width="600" />

From relational to graph query languages, real-time to batch analytics, and from single machine to cluster-oriented databases, mm-ADT enables users to generate _synthetic data infrastructures_ tailored to the requirements of their application.

---

## Founding Purpose

mm-ADT was originally going to be released under the Apache2 license. However, after some reflection, it was deemed that "free software" is perhaps not the best means of distributing technology within our industry at this point in time. In order to create a more responsible relationship between OSS and business, mm-ADT provides a mechanism for compensating open source developers who write free software for the Apache Software Foundation, Cloud Native Computing Foundation, and other similar OSS foundations. The intention is _not_ to have developers abandon their foundation affiliations, but instead to encourage them to also integrate their projects with mm-ADT. By doing so, their technology is given a commercial outlet, where the revenue generated from product licensing goes directly to the developers.

For more information, please review: <a href="model.html">The mm-ADT Open Source Model</a>.

---

## Components

The mm-ADT virtual machine integrates query languages, processors, and storage systems. Engineers developing these projects are invited to join the mm-ADT VM public mailing list and propose an mm-ADT integration project (see <a href="model.html">The mm-ADT Open Source Model</a>).

### Query Languages

* [Facebook GraphQL](http://graphql.org/): a path-based query language for tree-structured data.
* [ISO GQL](http://www.gqlstandards.org/): a hybrid relational/traversal query language for graph-structured data.
* [ISO SQL](https://en.wikipedia.org/wiki/SQL): a popular relational query languages.
* [TinkerPop Gremlin](http://tinkerpop.apache.org/gremlin.html): a traversal query language for graph-structured data.
* [W3C SPARQL](http://www.w3.org/TR/sparql11-query/): a pattern-matching query language for triple and quad-based data.

### Processing Engines

* [Apache Apex](http://apex.apache.org): A unified stream and batch processing engine.
* [Apache Beam](http://beam.apache.org): A unification framework for stream processors.
* [Apache Flink](http://flink.apache.org): A near-time analytics processor for cluster-oriented computing.
* [Apache Hadoop](http://hadoop.apache.org): A batch analytics processor for cluster-oriented computing.
* [Apache Spark](http://spark.apache.org): A batch analytics processor for cluster-oriented computing.
* [Lightbend Akka](http://akka.io): A message-passing processor for co-located computing.
* [ReactiveX](http://reactivex.io/): A push-based stream processor for multi-threaded data processing.

### Storage Systems

* [Apache Arrow](http://arrow.apache.org): A cross-system data layer for columnar in-memory analytics.
* [Apache Cassandra](http://cassandra.apache.org): A masterless, wide-column distributed database.
* [Apache HBase](http://hbase.apache.org): A wide-column distributed database built on Hadoop's HDFS.
* [Apache Ignite](http://ignite.apache.org): A distributed key-value/relational database.
* [Apache TinkerPop](http://tinkerpop.apache.org): A unification framework for graph databases and processors.
* [MongoDB](https://www.mongodb.com/): A document-oriented database for storing and querying JSON.
* [Facebook RocksDB](https://rocksdb.org/): An embedded key/value storage system.

The long term technological goal is to enable engineers to focus on their specific expertise whether it be in, for example, language design and compilers, distributed processing, or cluster-oriented file storage and indexing. Through the mm-ADT virtual machine, disparate technologies in the data processing stack can integrate in a plug-and-play manner enabling project outreach with the benefit of economic compensation.

---

## Licensing

mm-ADT is dual licensed: [AGPL3](https://www.gnu.org/licenses/agpl-3.0.txt) and a commercial license through [RReduX,Inc](http://rredux.com). 
