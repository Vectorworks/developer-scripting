# GetParametricRecord

## Description
Returns the handle to the parametric record attached the referenced object.<BR>
<BR>
Parametric record is a hidden record format containing the parameter values of the parametric object.<BR>
Only parametric objects have parametric records.

```pascal
FUNCTION GetParametricRecord(h : HANDLE): HANDLE;
```

```python
def vs.GetParametricRecord(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to a parametric object|

## Examples
```pascal
{find site model}
obj	:= FSActLayer;
while ( (obj <> NIL) & notFound ) do begin
	rec	:= GetParametricRecord( obj );
	if GetName(rec) = 'DTM6' then notFound := false;
	obj	:= NextObj( obj );
end;

numHeliodons := numHeliodons + 1;
city[numHeliodons] := GetRField(objectHandle, GetName(GetParametricRecord(objectHandle)), 'City');
rotationAngle := GetSymRot(objectHandle);

BEGIN
	paramRecord 	:= GetParametricRecord ( objHandle );
	numberFields	:= NumFields( paramRecord );
	result 			:= FALSE;
```
```python
import vs

# Returns the handle to the parametric record attached the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetParametricRecord(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
