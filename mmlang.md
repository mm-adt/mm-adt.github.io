---
layout: default
---

# mm-lang
## An mm-ADT Assembly Language

---

<a href="assets/images/posters/switzerland-travel.jpg"><img src="assets/images/posters/switzerland-travel.jpg" class="rimg" width="170"/></a> The mm-ADT virtual machine has an instruction set architecture. For a language to be mm-ADT compliant, it must compile to this instruction set. mmlang is a low-level, assembly language that is in near one-to-one correspondence with the logical structure of the mm-ADT virtual machine architecture. The capabilities of the mm-ADT virtual machine can be understood through a full understanding of mmlang.

---

## mm-ADT Obj Representation 

| type | zero   | one       | grammar                     | 
|:-----|:-------|:----------|:----------------------------|
|`bool`|`false` |`true`     |`bool | true | false`        |
|`int` |`0`     |`1`        |`int  | digit*`              |
|`real`|`0.0`   |`1.0`      |`real | digit*.digit*`       |
|`str` |`''`    |           |`str  | 'char*'`             |
|`rec` |`[:]`   |`[obj:obj]`|`rec  | [:] | [(obj:obj)*]`  |
|`lst` |`[;]`   |`[obj;obj]`|`lst  | [;] | [obj(;obj)*)]` |
|`inst`|`[none]`|`[id]`     |`inst | [str(,obj)*]`        |

<br/>

### mm-ADT Obj Modifiers

| name     | operation | signature      |example           |
|:---------|:----------|:---------------|:-----------------|
|bind      | `~`       | `obj~obj`      |`32~x`            |
|reference | `<=`      | `obj<=inst`    |`int <= [plus,2]` |
|quantifier| `{ }`     | `obj{obj,obj}` |`str{2,5}`        |

<br/>           

The example `obj` below denotes a stream of 1 to 10 records (`rec`) that are each bound to the structure of a `person` and can be accessed using the reference instructions `<=` which query a database for users named 'marko'.

```groovy
person~['name':'marko',age:int]{1,10} <=[=db][get,'users'][is,[get,'name'][eq,'marko']]
```

The console session below builds up this complex structure.

```groovy
mmlang> ['name':'marko']
==>['name':'marko']
mmlang> ['name':'marko','age':int]
==>['name':'marko','age':int]
mmlang> person~['name':'marko','age':int]
==>person~['name':'marko','age':int]
mmlang> person~['name':'marko','age':int]{1,10}
==>person~['name':'marko','age':int]{1,10}
mmlang> person~['name':'marko','age':int]{1,10} <=[=db][get,'users'][is,[get,'name']][eq,'marko']
==>person~['name':'marko','age':int]{1,10} <= [=,obj~db][get,'users'][is,[get,'name']][eq,'marko']
```


---

## Syntactic Sugar

