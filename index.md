---
layout: default
---

# mm-ADT
## A Multi-Model Abstract Data Type

---

<img src="assets/images/mm-adt-logo.png" alt="mm-ADT" width="25%" style="float:right;"/> mm-ADT&#8482; is a distributed virtual machine capable of integrating a diverse collection of data processing technologies. This is made possible via three language-agnostic interfaces: language, process, and storage. When a technology implements a respective interface, the technology is considered _mm-ADT compliant_ and is able to communicate with any other compliant technologies via the virtual machine. In this manner, query language developers can develop languages irrespective of the underlying storage system being manipulated. Processing engines can be programmed by any query language and executed over any storage system. Finally, data storage systems automatically support all mm-ADT compliant query languages and processors.

<img src="assets/images/lang-proc-store.png" alt="mm-ADT Components" width="100%" />

From relational to graph query languages, real-time to batch analytics, and from single machine to cluster-oriented data stores, mm-ADT can be used to generate _synthetic data infrastructures_ tailored to the problem at hand.

---

## Founding Purpose

<a href="assets/images/posters/protect-your-hands.jpg"><img src="assets/images/posters/protect-your-hands.jpg" class="rimg" width="180"/></a> mm-ADT was originally planned for release under the Apache2 free software license. However, after some reflection, it was deemed that free software is perhaps not the best means of distributing technology at this point in time in our industry. In order to create a more responsible relationship between OSS and business, mm-ADT provides a means of compensating open source developers for their efforts at the Apache Software Foundation, Cloud Native Computing Foundation, and other similar OSS foundations. The intention is _not_ to have developers abandon their foundation affiliations, but instead to encourage them to also integrate their projects with mm-ADT. By doing so, their technology is given a commercial outlet, where the revenue generated from product licensing goes directly to the developers.

For more information, please review: <a href="perspective.html">The mm-ADT Perspective</a>.

---

## Technologies
[](#technologies)

The mm-ADT virtual machine integrates query languages, processors, and storage systems. Engineers developing any of the projects below are invited to join the mm-ADT VM public mailing list and propose an mm-ADT integration project (see <a href="model.html">The mm-ADT Open Source Model</a>).

<div class="boxed">
<center>
The mm-ADT VM is currently in the initial stages of development. The itemized projects below will be compatible with the first release, where a subset is intended to be offered by mm-ADT.
</center>
</div>
<br/>
<a href="assets/images/posters/forging-ahead.jpg"><img src="assets/images/posters/forging-ahead.jpg" class="rimg" width="180"/></a> 

The mm-ADT virtual machine allows disparate data technologies to coordinate in both a static and dynamic, plug-and-play manner. By universally integrating the world's _defacto_ open source data technologies, mm-ADT becomes malleable enough to support contemporary use-cases, while remaining adaptable to future theoretical and applied advances. The mm-ADT architecture was designed to further specialize the developer expertise. It is hypothesized that individual projects will be simpler to manage and engineer, while the number of projects and their rate of evolution will increase. Because mm-ADT provides a collective focal point, individual projects are no longer responsible for developing every aspect of a data system which, historically, has yielded the monolithic, decade-long software projects we use today.

### Query Languages

[Apache Gremlin](http://tinkerpop.apache.org/gremlin.html): a traversal query language for graph-structured data.  
[ISO GQL](http://www.gqlstandards.org/): a hybrid relational/traversal query language for graph-structured data.  
[ISO SQL](https://en.wikipedia.org/wiki/SQL): a popular relational query languages.  
[Linux Foundation GraphQL](http://graphql.org/): a path-based query language for hierarchical data.  
[W3C SPARQL](http://www.w3.org/TR/sparql11-query/): a pattern-matching query language for triple and quad-based data.  
[W3C XPath](https://www.w3.org/TR/xpath/all/): a path-based query language for hierarchical data.

### Processing Engines

[Apache Apex](http://apex.apache.org): A unified stream and batch processing engine.  
[Apache Beam](http://beam.apache.org): A unification framework for stream processors.  
[Apache Flink](http://flink.apache.org): A near-time analytics processor for cluster-oriented computing.  
[Apache Hadoop](http://hadoop.apache.org): A batch analytics processor for cluster-oriented computing.  
[Apache Spark](http://spark.apache.org): A batch analytics processor for cluster-oriented computing.  
[Lightbend Akka](http://akka.io): A message-passing processor for co-located computing.  
[ReactiveX](http://reactivex.io/): A push-based stream processor for multi-threaded data processing.

### Storage Systems

[Apache Arrow](http://arrow.apache.org): A cross-system data layer for columnar in-memory analytics.  
[Apache Cassandra](http://cassandra.apache.org): A masterless, wide-column distributed database.  
[Apache HBase](http://hbase.apache.org): A wide-column distributed database built on Hadoop's HDFS.  
[Apache Ignite](http://ignite.apache.org): A distributed key-value/relational database.  
[Apache TinkerPop](http://tinkerpop.apache.org): A unification framework for graph databases and processors.  
[Facebook RocksDB](https://rocksdb.org/): An embedded key/value storage system.  
[MongoDB](https://www.mongodb.com/): A document-oriented database for storing and querying JSON.

While mm-ADT currently realizes three logical partitions of the data technology space: language, processor, and storage&mdash;once demonstrated viable, each partition may be further divided with, e.g., projects focused on disk-layouts and indexing structures, to projects exploring novel data models and respective language semantics necessary to address the upcoming challenges in our collective pursuit of the nature of structure and process.

---

## Licensing

mm-ADT is dual licensed: [AGPL3](https://www.gnu.org/licenses/agpl-3.0.txt) and a commercial license through [RReduX,Inc](http://rredux.com). 
