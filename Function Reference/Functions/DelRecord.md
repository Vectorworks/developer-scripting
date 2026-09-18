# DelRecord

## Description
Procedure DelRecord removes an attached record from the referenced object.

```pascal
PROCEDURE DelRecord(
				h    : HANDLE;
				name : STRING);
```

```python
def vs.DelRecord(h, name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|name|STRING|Name of record to be removed.|

## Examples
```pascal
IF attached THEN
	DelRecord (symDefH, gRecordName);

BEGIN
DelRecord(hObj,ChStr6);
END;

BEGIN
	DelRecord (h, kOriginalObjRec);
END;
```
```python
import vs

# Procedure DelRecord removes an attached record from the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
name = 'Example'

vs.DelRecord(h, name)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
