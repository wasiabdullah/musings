## Ternary operator in python

` min = a if a<b else b `

**Syntax: [on_true] if [expression] else [on_false]**

*expression : conditional_expression | lambda_expr*


``` python
min = print("a is less than b" is a<b else " ais greater than b" isf a>b else "both are equal")


print( (b, a) [a < b] )

print({True: a, False: b} [a < b])

print((lambda: b, lambda: a)[a < b]())

# [statement_on_True] if [condition] else [statement_on_false] 
print(a,"is greater") if (a>b) else print(b,"is Greater")
```

## using os module in python 

### to get all png files in a folder

``` python

import os
dir_path = "/home/user/documents"
files = [
os.path.join(dir_path, f)
for f in os.listdir(dir_path)
if os.path.isfile(os.path.join(dir_path, f)) and f.endswith(".png")
]


```