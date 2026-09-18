# IsLocked

## Description
Returns is the object locked for edit.

```pascal
FUNCTION IsLocked(VAR hObject : HANDLE): BOOLEAN;
```

```python
def vs.IsLocked(hObject):
    return (BOOLEAN, hObject)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to the object|

## Examples
```python
isLocked := vs.IsLocked( object );
```

```pascal
BEGIN
	recordH := GetRecord (NIL, i);
	IF (NOT IsPluginFormat (recordH)) AND (NOT IsLocked(recordH)) THEN
	BEGIN
		recName := Copy( GetName( recordH ), 1, 5 );
		if  recName <> '__NNA'  THEN
		BEGIN
			j := j + 1;
			ALLOCATE gRecordH [1..j];
```
```python
import vs

# Returns is the object locked for edit.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, hObject = vs.IsLocked(hObject)
vs.Message('IsLocked returned: ' + str((ok, hObject)))
```

## Version
Availability: from Vectorworks 2025

## Category
* [Object Info](../Categories/Object%20Info.md)
