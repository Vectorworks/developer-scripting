# PrevObj

## Description
Function PrevObj returns the object in any list which precedes the specified object.  If the end of the list is reached, the function returns NIL.

```pascal
FUNCTION PrevObj(h : HANDLE): HANDLE;
```

```python
def vs.PrevObj(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object,  group, or  symbol definition.|

## Examples
```pascal
BEGIN
boo := GetHole(h, cnt, hole);
hole := CopyPoly(hole,FALSE);
ClipSurface(poly, hole);
poly := PrevObj(hole);
DelObj(hole);
END;

		fieldName	:= GetFldName( hRec, j );
		SetRField( hNewObj, recName, fieldName, GetRField( handles[cnt], recName, fieldName ) );
	END;
END;
hNewObj	:= PrevObj( hNewObj );
{now delete this}
DelObject( handles[cnt] );
END;

FOR cnt := 1 TO holeCnt DO BEGIN
	boo := GetHole(h, cnt, hole);
	hole := CopyPoly(hole);
	ClipSurface(poly, hole);
	poly := PrevObj(hole);
	DelObj(hole);
END;
```
```python
import vs

# Function PrevObj returns the object in any list which precedes the
# specified object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.PrevObj(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
Relative calls:
* [NextObj](NextObj.md) | [PrevObj](PrevObj.md)
* [FObject](FObject.md) | [LObject](LObject.md)
* [FSActLayer](FSActLayer.md) | [LSActLayer](LSActLayer.md)
* [FSObject](FSObject.md)  | [LActLayer](LActLayer.md)
* [NextDObj](NextDObj.md) | [PrevDObj](PrevDObj.md)
* [NextSObj](NextSObj.md) | [PrevSObj](PrevSObj.md)

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
