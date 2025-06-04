# GetSymbolType

## Description
Determines the type of the specified symbol instance.  The return values are:
0 - 2D Only
1 - 3D Only
2 - Hybrid

```pascal
FUNCTION GetSymbolType(objectHandle : HANDLE): INTEGER;
```

```python
def vs.GetSymbolType(objectHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to a symbol instance.|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
