# SetVectorFillDefault

## Description
Function SetVectorFillDefault sets the default vector fill pattern for the document. The function returns TRUE if the operation was successful.

```pascal
FUNCTION SetVectorFillDefault(VAR vectorFillName : STRING): BOOLEAN;
```

```python
def vs.SetVectorFillDefault(vectorFillName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|vectorFillName|STRING|Name of vector fill.|

## Remarks
Returns true if the active document's default hatch was succesfully set to the hatch with the name specified by vectorFillName.  vectorFillName may retrun with a different name than passed in because there may be a name conflict.

## Version
Availability: from MiniCAD7.0.1

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
