---
published : true

title : Python Functions
permalink : /py/func
layout : note
excerpt : 

alias : 
categories : "py"
tags : 

# date : 2022-04-14 00:00:00 +0000

showfooter : 
showgraph : 
---

### Passing Arguments 

- passing a [[py.list]] will get reference to original
- passing a [[py.variable]] will get a copy

```python
def f(v,val):
	v=1
	val[0]=99
a = 5
arr = [0,1,2]
f(a,arr)
print(a,arr) #3 99
```


### List of Built-In Functions

- [[py.func.abs|abs()]]
- [[py.func.all|all()]]
- [[py.func.any|any()]]
- [[py.func.ascii|ascii()]]
- [[py.func.bin|bin()]]
- [[py.func.bool|bool()]]
- [[py.func.byterarry|byterarry()]]
- [[py.func.bytes|bytes()]]
- [[py.func.callable|callable()]]
- [[py.func.chr|chr()]]
- [[py.func.classmethod|classmethod()]]
- [[python.func.compile|compile()]]
- [[python.func.complex|complex()]]
- [[python.func.delattr|delattr()]]
- [[python.func.dict|dict()]]
- [[python.func.dir|dir()]]
- [[py.func.divmod|divmod()]]
- [[python.func.enumerate|enumerate()]]
- [[python.func.eval|eval()]]
- [[python.func.exec|exec()]]
- [[python.func.filter|filter()]]
- [[python.func.float|float()]]
- [[python.func.format|format()]]
- [[python.func.frozenset|frozenset()]]
- [[python.func.getattr|getattr()]]
- [[python.func.globals|globals()]]
- [[python.func.hasattr|hasattr()]]
- [[python.func.hash|hash()]]
- [[python.func.help|help()]]
- [[python.func.hex|hex()]]
- [[python.func.id|id()]]
- [[python.func.input|input()]]
- [[python.func.int|int()]]
- [[python.func.isinstance|isinstance()]]
- [[python.func.issubclass|issubclass()]]
- [[python.func.iter|iter()]]
- [[python.func.list|list()]]
- [[python.func.locals|locals()]]
- [[python.func.map|map()]]
- [[py.func.max|max()]]
- [[python.func.memoryview|memoryview()]]
- [[python.func.min|min()]]
- [[python.func.next|next()]]
- [[python.func.object|object()]]
- [[python.func.oct|oct()]]
- [[python.func.open|open()]]
- [[python.func.ord|ord()]]
- [[python.func.pow|pow()]]
- [[python.func.print|print()]]
- [[python.func.property|property()]]
- [[python.func.range|range()]]
- [[python.func.repr|repr()]]
- [[python.func.reversed|reversed()]]
- [[python.func.round|round()]]
- [[python.func.set|set()]]
- [[python.func.setaatr|setaatr()]]
- [[python.func.slice|slice()]]
- [[py.func.sorted|sorted()]]
- [[python.func.staticmethod|staticmethod()]]
- [[python.func.str|str()]]
- [[python.func.sum|sum()]]
- [[python.func.super|super()]]
- [[python.func.tuple|tuple()]]
- [[python.func.type|type()]]
- [[python.func.vars|vars()]]
- [[python.func.zep|zep()]]

---

Return to [[py.python|python]]

---
