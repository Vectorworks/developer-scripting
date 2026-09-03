# GetProjectionWKT

## Description
Get the projection information in Well Known Text (WKT) format..

```pascal
FUNCTION GetProjectionWKT(
				hLayer     : HANDLE;
				esriStyle  : BOOLEAN;
				VAR outWKT : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.GetProjectionWKT(hLayer, esriStyle):
    return (BOOLEAN, outWKT)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|   |
|esriStyle|BOOLEAN|   |
|outWKT|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultOK := GetProjectionWKT(hLayer, TRUE, outWKT);
```
```python
import vs

# Get the projection information in Well Known Text (WKT) format.
hLayer = vs.ActLayer()  # handle to the active design layer
esriStyle = True

ok, outWKT = vs.GetProjectionWKT(hLayer, esriStyle)
vs.Message('GetProjectionWKT returned: ' + str((ok, outWKT)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [GIS](../Categories/GIS.md)
