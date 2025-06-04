# GetProjectionProj4

## Description
Get the projection information in Proj4 format.

```pascal
FUNCTION GetProjectionProj4(
				hLayer       : HANDLE;
				esriStyle    : BOOLEAN;
				VAR outProj4 : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.GetProjectionProj4(hLayer, esriStyle):
    return (BOOLEAN, outProj4)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|   |
|esriStyle|BOOLEAN|   |
|outProj4|DYNARRAY[] of CHAR|   |

## Version
Availability: from Vectorworks 2014

## Category
* [GIS](../Categories/GIS.md)
