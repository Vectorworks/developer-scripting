# IFC_DMResetToDef

## Description
Resets the data mapping to the default values.

```pascal
FUNCTION IFC_DMResetToDef : BOOLEAN;
```

```python
def vs.IFC_DMResetToDef():
    return BOOLEAN
```

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	ok : BOOLEAN;
BEGIN
	ok := IFC_DMResetToDef();
END;

RUN(Test);
```
==== Python ====
```python
ok	= vs.IFC_DMResetToDef()
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
