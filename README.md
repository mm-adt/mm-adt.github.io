# mm-ADT
## A Multi-Model Abstract Data Type

<img src="https://raw.githubusercontent.com/mm-adt/mm-adt.github.io/master/images/mm-adt-logo.png" alt="mm-ADT" width="150" />

mm-ADT is a distributed computing virtual machine aimed at integrating data storage systems, processing engines, and query languages. A collection of language-agnostic interfaces is made available to each technology community and when a valid implementaiton of said interfaces is created, the interfacing component is considered mm-ADT compliant and can faithfully interoperate with any other mm-ADT compliant component. In this manner, query language developers can develop languages irrespective of the underlying storage system that will ultimately be manipulated by the language. Similarly, processing engine developers can have their processors programmed by any query language for data stored in any storage system. Finally, storage systems (such as databases) immediately support any all mm-ADT compliant query languages and processors in support of the varigated requirements of their end users' data processing requirements.

<img src="https://raw.githubusercontent.com/mm-adt/mm-adt.github.io/master/images/lang-proc-store.png" alt="mm-ADT Components" width="600" />

## Mission

mm-ADT is focused on integrating the many open source data projects currently sponsored by the Apache Software Foundation, Cloud Native Computing Foundation, and other related OSS foundations. Integration is accomplished by creating mm-ADT bindings that enable the mm-ADT VM to control these components. Each binding will be dual licensed in the same manner as the mm-ADT VM, with the developers of those bindings earning the revenue their work generates from license sales.

## Licensing

mm-ADT is dual licensed: AGPL3 and a commercial license through RReduX,Inc. 

---

mm-ADT is a trademark of RReduX,Inc.