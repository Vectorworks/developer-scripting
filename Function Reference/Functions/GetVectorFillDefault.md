# GetVectorFillDefault

## Description
Function GetVectorFillDefault returns TRUE if the the active document contains a default vector fill, and returns the name of the vector fill pattern.

```pascal
FUNCTION GetVectorFillDefault(VAR vectorFillName : STRING): BOOLEAN;
```

```python
def vs.GetVectorFillDefault():
    return (BOOLEAN, vectorFillName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|vectorFillName|STRING|Returns name of vector fill.|

## Remarks
Returns true if the the active document contains a default hatch.  vectorFillName contains a string with the name of the default hatch.

## Version
Availability: from MiniCAD7.0.1

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
