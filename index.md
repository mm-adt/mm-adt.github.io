# mm-ADT
## A Multi-Model Abstract Data Type

<img src="assets/images/mm-adt-logo.png" alt="mm-ADT" width="165" />

<a href="https://github.com/mm-adt"><img src="assets/images/github-icon.png" alt="GitHub" width="35" /></a>
<a href="http://twitter.com/_mmadt"><img src="assets/images/twitter-icon.png" alt="Twitter" width="35" /></a>

mm-ADT is a distributed virtual machine aimed at integrating the numerous open source projects in the data space. This is accomplished via three language-agnostic interfaces. When a technology implements the respective interface, the technology is considered _mm-ADT compliant_ and is able to communicate with any other mm-ADT compliant technologies. In this manner, query language developers can develop languages irrespective of the underlying storage system that will ultimately be manipulated by the language. Processing engines can be programmed by any query language and used over any storage system. Finally, storage systems (such as databases) automatically support all mm-ADT compliant query languages and processors.

From relational to graph query languages, real-time to batch analytics, and from single machine to cluster-oriented databases, mm-ADT enables users to create _synthetic data infrastructres_ tailored to the requirements of their application.

<img src="assets/images/lang-proc-store.png" alt="mm-ADT Components" width="600" />

## Founding Purpose

mm-ADT was initially going to be released under the Apache2 license. However, this path was retarded after some reflection, where perhaps "free software" is not the best  approach for our trade at this point in time. In order to create a more responsible relationship between OSS and business, mm-ADT seeks to engage open source developers writing software at the calibur of the Apache Software Foundation, Cloud Native Computing Foundation, and similar OSS foundations. The intention is not to turn developers away from developing free software, but to encourage them to build bindings from their projecs to mm-ADT as all mm-ADT technology will be dual licensed, where the revenue generated from license sales goes directly to the developers. 

For more information, please review: <a href="model.html">The mm-ADT Effect</a>.

## Components

The mm-ADT VM is the integration point of query languages, processors, and storage systems. The following itemizations outline the desired near-term components. Engineers from these projects are invited to contact RReduX,Inc. to discuss how they can participate in mm-ADT and earn revenue from license sales.

### Query Languages

* [ISO SQL](https://en.wikipedia.org/wiki/SQL): the most popular relational query languages.
* [Facebook GraphQL](http://graphql.org/): a path-based query language for tree-structured data.
* [TinkerPop Gremlin](http://tinkerpop.apache.org/gremlin.html): a traversal query language for graph-structured data.
* [ISO GQL](http://www.gqlstandards.org/): a hybrid relational/traversal query language for graph structured data.
* [W3C SPARQL](http://www.w3.org/TR/sparql11-query/): a pattern-matching query language for triple and quad-based data.

### Processing Engines

* [ReactiveX](http://reactivex.io/): A reactive stream processor for multi-threaded data processing.
* [Apache Spark](http://spark.apache.org): An batch analytics processor for cluster-oriented computing.
* [Apache Flink](http://flink.apache.org): A near-time analytics processor for cluster-oriented computing.
* [Apache Beam](http://beam.apache.org): A unification framework for popular stream processors.
* [Apache Hadoop](http://hadoop.apache.org): A batch analytics processor for cluster-oriented computing.
* [Lightbend Akka](http://akka.io): A message-passing processor for co-located computing.

### Storage Systems

* [Apache Cassandra](http://cassandra.apache.org): A master-less, wide-column distributed database.
* [Apache HBase](http://hbase.apache.org): A wide-column distributed database built on Hadoop's HDFS.
* [Apache Ignite](http://ignite.apache.org): A distributed key-value/relational database.
* [Apache TinkerPop](http://tinkerpop.apache.org): A unification framework for graph databases and processors.
* [MongoDB](https://www.mongodb.com/): A document-oriented database in for storing and querying JSON.
* [Facebook RocksDB](https://rocksdb.org/): An embedded key/value storage system.

The long term technological goal is to enable engineers to focus on their specific expertise whether it be in, for example, language design and compilers, distributed processing, or cluster-oriented file storage and indexing. Through the mm-ADT virtual machine, disparte technologies in the data processing stack can integrate in a plug-and-play manner enabling project outrearch with the benfits of economic security.


## Licensing

mm-ADT is dual licensed: [AGPL3](https://www.gnu.org/licenses/agpl-3.0.txt) and a commercial license through [RReduX,Inc](http://rredux.com). 