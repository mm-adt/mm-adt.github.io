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

### mm-lang Operators

There are unary and binary operators. Every unary operator token can be used as a binary operator.

| token | name  | unary                | binary                              |
|:------|:------|:---------------------|:------------------------------------|
| `+`   | plus  | `+2  = [plus,2]`     | `1+2      = [start,1][plus,2]`      |
| `-`   | minus | `-2  = [map,2][neg]` | `1-2      = [start,1][minus,2]`     |
| `*`   | mult  | `*2  = [mult,2]`     | `1*2      = [start,1][mult,2]`      |
| `/`   | div   | `/2  = [div,2]`      | `1/2      = [start,1][div,2]`       |
| `>`   | gt    | `>2  = [gt,2]`       | `1>2      = [start,1][gt,2]`        |
| `<`   | lt    | `<2  = [lt,2]`       | `1<2      = [start,1][lt,2]`        |
| `>=`  | gte   | `>=2 = [gte,2]`      | `1>=2     = [start,1][gte,2]`       |
| `=<`  | lte   | `=<2 = [lte,2]`      | `1=<2     = [start,1][lte,2]`       |
| `==`  | eq    | `==2 = [eq,2]`       | `1==2     = [start,1][eq,2]`        |
| `=>`  | as    | `=>2 = [as,2]`       | `1=>1     = [start,1][as,2]`        |
| `<-`  | get   | `<-2 = [get,2]`      | `[2:3]<-2 = [start,[2:3]][get,2]`   |
| `->`  | put   | N/A                  | `1->2     = [start,[:]][put,1,2]`   |
| `<=`  | ref   | N/A                  | `1<=[a]   = [a][as,1]`              |


