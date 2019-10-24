---
layout: default
---

# mm-ADT
## A Cluster-Oriented Virtual Machine Architecture

---

The mm-ADT virtual machine has two primary functions. The first is to coordinate processors and and storage engines with an distributed, multi-machine compute cluster. The second is to enable users to specify computations (i.e. queries or programs) to be executed across the cluster.

---

## The Structures of Obj

The base structure of mm-ADT is `obj`&mdash;object. There are 7 fundamental, [_built-in_ types](https://en.wikipedia.org/wiki/Primitive_data_type) that extend `obj` and are diagrammed below. Custom _derived types_ can be defined by combining and constraining the 7 built-in types. mm-ADT provides a collection of generally useful derived types such as `short`,`long`,`varchar`,`complex`,`pair`,etc. mm-ADT users will typically also define domain-specific types such as `person` or `company` for the purpose of modeling their applications' constructs.

<center>
<img src="assets/images/theory/obj-types.png" width="500"/>
</center>

<br/>
Every `obj` is a _carrier_ in an [algebraic structure](https://en.wikipedia.org/wiki/Algebraic_structure) (a set with operators). The set of operators that each type draws from are denoted by the symbols `*`, `+`, `/`, `-`, `&`, `|`, and `!`. Along with operators, a type can specify a `0` and/or `1` element. The meaning of these symbols is [_overloaded_](https://en.wikipedia.org/wiki/Operator_overloading) in that each type specifies a type-specific operator semantics. The default algebraic structures for the built-in types are provided in the table below.

| type   | algebraic structure         | operators               | identities              |
| :------|:--------------------------- | :---------------------- | :-------------------- |
| `bool` | commutative [ring](https://en.wikipedia.org/wiki/Ring_(mathematics)) with unity | `*`,`+`,`-`,`&`,`|`,`!` | `0=>false`,`1=>true`  |
| `int`  | commutative [ring](https://en.wikipedia.org/wiki/Ring_(mathematics)) with unity | `*`,`+`,`-`             | `0=>0`,`1=>1`         |
| `real` | [field](https://en.wikipedia.org/wiki/Field_(mathematics))                      | `*`,`+`, `/`, `-`       | `0=>0.0`,`1=>1.0`     |
| `str`  | synthetic [group](https://en.wikipedia.org/wiki/Group_(mathematics))            | `+`,`-`                 | `0=>''`               |
| `list` | synthetic [group](https://en.wikipedia.org/wiki/Group_(mathematics))            | `+`,`-`                 | `0=>[]`               |
| `rec`  | synthetic [group](https://en.wikipedia.org/wiki/Group_(mathematics))            | `+`,`-`                 | `0=>[:]`              |
| `inst` | a [ring](https://en.wikipedia.org/wiki/Ring_(mathematics)) with unity           | `*`,`+`,`-`,`&`,`|`     | `0=>[none]`,`1=>[id]` |

<br/>
Every algebraic structure has a set of axioms whose entailments yield theorems. In mm-ADT, theorems are used by the virtual machine to perform [type checking](https://en.wikipedia.org/wiki/Type_system#Type_checking), [type inference](https://en.wikipedia.org/wiki/Type_inference), and program optimization. Furthermore, via the construct of _model-ADTs_ and _embeddings_, different algebraic structures (ultimately using the same fundamental types as carriers) can be defined and mixed within the same computation. Models specify isolated algebraic environments and rules for moving between them. In the lexicon of [category theory](https://en.wikipedia.org/wiki/Category_theory), models are _categories_ and embeddings are [_functors_](https://en.wikipedia.org/wiki/Functor). Thus, the "default algebraic structures" specified in the table above are understood to be a collection of models denoted `mm`&mdash;the core model-ADT from which all other models are ultimately derived.

```groovy
mmadt> true | false             // bool or
==>true
mmadt> true + true              // bool exclusive or
==>false
mmadt> 'mar' + 'ko'             // str concatenation
==>'marko'
mmadt> ['a':1,'b':2] - ['a':1]  // rec retraction
==>['b':2]
mmadt> 'hey' + 42               // int is first embedded in str
==>'hey42'
```

---

## The Processes of Inst

An mm-ADT object is a static structure. A process is required to mutate objects. All processes are described by the `inst` commutative ring, where `*` is serial instruction composition (compose) and `+` is parallel instruction composition (branch). Thus, `inst` is a unique object in that it bridges the static world of structure and the dynamic world of processes to yield the phenomena of _computing_.

There is special `obj` called `inst`&mdash;instruction.

```groovy
mmadt> 'mar' + 'ko'
==>'marko'
mmadt> 'mar' * [plus,'ko']
==>'marko'
```

## The Model
