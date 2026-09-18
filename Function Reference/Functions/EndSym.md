# EndSym

## Description
Procedure EndSym completes symbol creation in VectorScript. When EndSym is called, the any procedure calls defined since a call to BeginSym are used to create the symbol.

```pascal
PROCEDURE EndSym;
```

```python
def vs.EndSym():
    return None
```

## Examples
```pascal
EndSym;
```
```python
import vs

# Procedure EndSym completes symbol creation in VectorScript.
vs.EndSym()
```

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
