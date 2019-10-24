---
layout: default
---

# mm-ADT
## A Cluster-Oriented Virtual Machine Architecture

---

The mm-ADT virtual machine has two primary functions. The first is to coordinate any number of processing engines and storage systems within a compute cluster. The second is to enable users to specify computations (i.e. queries or programs) to be executed across the cluster.

## The Obj

The most fundamental structure in mm-ADT is `obj`&mdash;object. There are 7 built-in/fundamental types that all behave as an `obj`, but also have their own characteristics. All other types are derived from these base types via combination or constraint. The mm-ADT standard library comes with a collection of common types such as `short`,`long`,`varchar`,`complex` and are defined by users that typically reflect their application domain such as `person`, `product`, etc.

<img src="assets/images/theory/obj-types.png" width="500"/>



## The Inst

There is special `obj` called `inst`&mdash;instruction.

```groovy
mmadt> 'mar' + 'ko'
==>'marko'
mmadt> 'mar' * [plus,'ko']
==>'marko'
```

## The Model
