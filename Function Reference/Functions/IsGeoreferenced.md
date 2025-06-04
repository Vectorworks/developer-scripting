# IsGeoreferenced

## Description
Check if the layer is georeferenced. Pass NIL to check the document.

```pascal
FUNCTION IsGeoreferenced(hLayer : HANDLE): BOOLEAN;
```

```python
def vs.IsGeoreferenced(hLayer):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|Pass NIL for Vectorscript and None for Python if you want to manage the document.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
var
isGeoref: BOOLEAN;
BEGIN
RemoveGeoref(NIL);
isGeoref := IsGeoreferenced(NIL);
if (isGeoref) then 
	AlrtDialog('The file is georeferenced.')
else
	AlrtDialog('The file is not georeferenced.');
end;
run(Test);
```
#### Python ####
```python
vs.RemoveGeoref(None)
isGeoref	= vs.IsGeoreferenced(None)
if isGeoref:
	vs.AlrtDialog('The file is georeferenced.')
else:
	vs.AlrtDialog('The file is not georeferenced.')
```

## Version
Availability: from Vectorworks 2012

## Category
* [GIS](../Categories/GIS.md)
