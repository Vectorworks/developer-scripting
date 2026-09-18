# WSScript_AddHandleId

## Description
Add a handle with id for a worksheet script usage. This is most notable used for scripts that generate object database for worksheets.

```pascal
PROCEDURE WSScript_AddHandleId(
				h  : HANDLE;
				id : INTEGER);
```

```python
def vs.WSScript_AddHandleId(h, id):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The handle of an object to be added|
|id|INTEGER|The id of the handle|

## Examples
```pascal
WSScript_AddHandleId(h, 1);
```
```python
import vs

# Add a handle with id for a worksheet script usage.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
id = 1

vs.WSScript_AddHandleId(h, id)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Worksheets](../Categories/Worksheets.md)
