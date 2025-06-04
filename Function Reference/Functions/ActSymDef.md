# ActSymDef

## Description
Function ActSymDef returns a handle to the currently active symbol.

```pascal
FUNCTION ActSymDef : HANDLE;
```

```python
def vs.ActSymDef():
    return HANDLE
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR HandleToActiveSym : HANDLE;
BEGIN
HandleToActiveSym:=ActSymDef;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	HandleToActiveSym = vs.ActSymDef()
Example()
```

## See Also
VS Functions:
[ActLayer](ActLayer.md) 
| [ActiveClass](ActiveClass.md)

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
