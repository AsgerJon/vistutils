# vistutils

vistutils is a collection of modules providing helpful utility functions. The latest release includes the following functions:

## waila - what am I looking at?

Instead of writing something like:
~~~
for item in dir(obj):
  print(item)
~~~
Simply use waila(obj)! This prints the name of each entry like above including the documentation associated with the object. 
waila supports the following keyword arguments

### dunder
Includes dunder methods of the objects (default False)

### magic 
alias for dunder (default False)

### getReturn
if True, waila(obj) returns items as a list of dictionaries with keys: 'name', 'type' and 'help' (default False)

### fid 
saves the results to a text file of this name.

### save
if True, saves results to textfile, ignored if fid is given, otherwise a filename is generated, which includes the name of the object and the time of save. (default False)

## insistType

Instead of writing something like:
~~~
if not isinstance(obj, type_):
  raise TypeError('Wrong type!')
~~~
use insistType:
~~~
insistType(obj, reqType, msg=None)
~~~
This utility raises a type error unless obj is an instance of reqType. This is only for development, as type hinting is the correct method.
