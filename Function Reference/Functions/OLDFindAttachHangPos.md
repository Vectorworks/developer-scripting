# OLDFindAttachHangPos

## Description
Searches for a Hanging Position for the Hang Points of the given load index. Returns the Position handle if found, NIL otherwise.

```pascal
FUNCTION OLDFindAttachHangPos(
				handle    : HANDLE;
				loadIndex : INTEGER): HANDLE;
```

```python
def vs.OLDFindAttachHangPos(handle, loadIndex):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |

## Examples
```pascal
	IF gCreated THEN
		hl := OLDFindAttachHangPos( ghParm, 0 );
END;
```
```python
import vs

# Searches for a Hanging Position for the Hang Points of the given load index.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1

objHandle = vs.OLDFindAttachHangPos(handle, loadIndex)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
