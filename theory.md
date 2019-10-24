---
layout: default
---

# mm-ADT
## A Cluster-Oriented Virtual Machine Architecture

---

The mm-ADT virtual machine has two primary functions. The first is to coordinate processors and and storage engines with an distributed, multi-machine compute cluster. The second is to enable users to specify computations (i.e. queries or programs) to be executed across the cluster.

## The Obj

The most fundamental structure in mm-ADT is `obj`&mdash;object. There are 7 fundamental, _built-in_ types that extend `obj`. New _derived types_ can be created by combining and constraining the 7 built-in types. The mm-ADT standard library provides a collection of generally useful types such as `short`,`long`,`varchar`,`complex`,`pair`,etc. Finally, mm-ADT users will typically define domain-specific types such as `person` or `product` in order to model the constructs in their application.

<img src="assets/images/theory/obj-types.png" width="500"/>

Every `obj` is a _carrier_ in an algebraic structure. The set of operators that each type draws from are denoted by the symbols `*`, `+`, `/`, `-`, `&`, `|`, and `!`. Along with operators, a type can specify a `0` and/or `1` instance. The meaning of these symbols is _overloaded_ in that each type specifies a type-specific operator semantics. The default algebraic structures for the built-in types are provided in the table below.

| type   | algebraic structure         | operators               | members               |
| :------|:--------------------------- | :---------------------- | :-------------------- |
| `bool` | commutative ring with unity | `*`,`+`,`-`,`&`,`|`,`!` | `0=>false`,`1=>true`  |
| `int`  | commutative ring with unity | `*`,`+`,`-`             | `0=>0`,`1=>1`         |
| `real` | field                       | `*`,`+`, `/`, `-`       | `0=>0.0`,`1=>1.0`     |
| `str`  | group                       | `+`,`-`,?               | `0=>''`               |
| `list` | ...                         | `+`,`-`,?               | `0=>[]`               |
| `rec`  | ...                         | `+`,`-`,?               | `0=>[:]`              |
| `inst` | a ring with unity           | `*`,`+`,`-`,`&`,`|`     | `0=>[none]`,`1=>[id]` |

Every algebraic structure has a set of axioms that can be used to define theorems. In mm-ADT, algebraic theorems are used in type inference and program optimization.

## The Inst

An mm-ADT object is a static structure. A process is required to mutate objects. All processes are described by the `inst` commutative ring, where `*` is serial instruction composition (compose) and `+` is parallel instruction composition (branch). Thus, `inst` is a unique object in that it bridges the static world of structure to the dynamic world of processes&mdash;computation.

There is special `obj` called `inst`&mdash;instruction.

```groovy
mmadt> 'mar' + 'ko'
==>'marko'
mmadt> 'mar' * [plus,'ko']
==>'marko'
```

## The Model
