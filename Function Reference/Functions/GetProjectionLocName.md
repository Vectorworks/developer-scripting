# GetProjectionLocName

## Description
Get the projection format localized name

```pascal
FUNCTION GetProjectionLocName(
				hLayer      : HANDLE;
				VAR outProj : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.GetProjectionLocName(hLayer):
    return (BOOLEAN, outProj)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|   |
|outProj|DYNARRAY[] of CHAR|   |

## Version
Availability: from Vectorworks 2014

## Category
* [GIS](../Categories/GIS.md)
