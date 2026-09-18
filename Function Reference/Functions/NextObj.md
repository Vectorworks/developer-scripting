# NextObj

## Description
Function NextObj returns the next object in any list . If the end of the list is reached, the function returns NIL. This procedure can be used with other handle routines such as FirstIn3D,FInGroup, FirstInSymDef, or FLayer.

```pascal
FUNCTION NextObj(h : HANDLE): HANDLE;
```

```python
def vs.NextObj(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object,  group, or  symbol definition.|

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

```pascal
			gFolderN [gNumSymFolders] := GetName (itemHdl);
	  	 	getSymbolFolderNames (FInFolder (itemHdl));
	   END;
	END;
	itemHdl := NextObj (itemHdl);
END;

			END;
			slab_h := nextobj(slab_h);
		END ;
END;

SetRField(hobj,kRecName,kStatName,StatVal);
WHILE (hobj <> NIL) DO BEGIN
	SetPenFore(hobj,r,g,b);
	hobj := NextObj(hobj);
	END;
```
```python
import vs

# Function NextObj returns the next object in any list.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.NextObj(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```
See also in tutorials: [10. Iterate the Drawing and Report a Summary](ai%20examples/10_IterateAndReport.md)

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
