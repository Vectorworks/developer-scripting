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
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	ok : BOOLEAN;
BEGIN
	ok := IFC_DMResetToDef();
END;

RUN(Test);
```
#### Python ####
```python
ok	= vs.IFC_DMResetToDef()
```

```pascal
resultOK := IFC_DMResetToDef;
```
```python
import vs

# Resets the data mapping to the default values.
ok = vs.IFC_DMResetToDef()
if ok:
    vs.Message('IFC_DMResetToDef succeeded')
else:
    vs.Message('IFC_DMResetToDef failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
