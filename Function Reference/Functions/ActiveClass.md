# ActiveClass

## Description
Returns the name of the active class of the document.

```pascal
FUNCTION ActiveClass : STRING;
```

```python
def vs.ActiveClass():
    return STRING
```

## Examples
#### VectorScript ####
```pascal
activeClName:= ActiveClass;
```
#### Python ####
```python
activeClName = vs.ActiveClass()
```

```pascal
resultStr := ActiveClass;
```
```python
activeClName = vs.ActiveClass()

if ( classHandle == vs.Handle() or (kObjTypeClassDef != vs.GetTypeN( classHandle )) ):
	strActiveClassName = vs.ActiveClass()
	vs.NameClass( strClassName )
	vs.NameClass( strActiveClassName )
	ok = True
```

## See Also
VS Functions:
[ActLayer](ActLayer.md) 
| [ActSymDef](ActSymDef.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Classes](../Categories/Classes.md)
