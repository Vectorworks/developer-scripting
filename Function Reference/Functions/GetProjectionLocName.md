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

## Examples
```pascal
IF GetProjectionLocName( NIL, projectionFormat ) THEN
	SetItemText( dlogID , kGeoreferencingSecText, projectionFormat );
```
```python
import vs

# Get the projection format localized name.
hLayer = vs.ActLayer()  # handle to the active design layer

ok, outProj = vs.GetProjectionLocName(hLayer)
vs.Message('GetProjectionLocName returned: ' + str((ok, outProj)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [GIS](../Categories/GIS.md)
