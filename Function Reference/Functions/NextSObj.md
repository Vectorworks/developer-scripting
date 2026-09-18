# NextSObj

## Description
Function NextSObj returns the next selected object in a list. If the end of the list is reached, the function returns NIL.

```pascal
FUNCTION NextSObj(h : HANDLE): HANDLE;
```

```python
def vs.NextSObj(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
```pascal
	itemHandle := NextSObj(itemHandle);
END;

locHandle := NextSObj( locHandle ); { go to next selected. }

		begin
	ProcessSelectedChoice;
	ResetObject(gPluginH);
		end;
	gPluginH := NextSObj(gPluginH);
END;
```
```python
import vs

# Function NextSObj returns the next selected object in a list.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.NextSObj(h)
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
