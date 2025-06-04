# GetVectorFill

## Description
Function GetVectorFill returns if the referenced object has a vector fill assigned.

```pascal
FUNCTION GetVectorFill(
				theObj        : HANDLE;
				VAR hatchName : STRING): BOOLEAN;
```

```python
def vs.GetVectorFill(theObj):
    return (BOOLEAN, hatchName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theObj|HANDLE|Handle to object.|
|hatchName|STRING|Returns name of assigned vector fill pattern.|

## Remarks
Returns true if the theObj has a vectorfill. hatchName holds the name of the vector fill that theObj has.


This routine will also return names of Gradient or Image Fill definitions applied to theObj.

## Version
Availability: from MiniCAD7.0.1

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
