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

## Version
Availability: from Vectorworks 2014

## Category
* [GIS](../Categories/GIS.md)
