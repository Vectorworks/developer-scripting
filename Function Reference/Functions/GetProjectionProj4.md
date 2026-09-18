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

## Examples
```pascal
resultOK := GetProjectionProj4(hLayer, TRUE, outProj4);
```
```python
import vs

# Get the projection information in Proj4 format.
hLayer = vs.ActLayer()  # handle to the active design layer
esriStyle = True

ok, outProj4 = vs.GetProjectionProj4(hLayer, esriStyle)
vs.Message('GetProjectionProj4 returned: ' + str((ok, outProj4)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [GIS](../Categories/GIS.md)
