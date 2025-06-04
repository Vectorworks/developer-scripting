# SetVectorFill

## Description
Function SetVectorFill assigns the specified vector fill to the referenced object. The function returns TRUE if the operation was successful.

```pascal
FUNCTION SetVectorFill(
				theObj    : HANDLE;
				hatchName : STRING): BOOLEAN;
```

```python
def vs.SetVectorFill(theObj, hatchName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theObj|HANDLE|Handle to object.|
|hatchName|STRING|Name of vector fill to be assigned.|

## Remarks
Returns true if theObj was assigned the hatch specified by hatchName.

## Version
Availability: from MiniCAD7.0.1

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
