# GetClass

## Description
Function GetClass returns the class assigned to the referenced object. None is returned if the object has no class assigned to it.

```pascal
FUNCTION GetClass(h : HANDLE): STRING;
```

```python
def vs.GetClass(h):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
==== VectorScript ====
```pascal
ObjectClass:=GetClass(handleToObject);
```
==== Python ====
```python
ObjectClass = vs.GetClass(handleToObject)
```

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
