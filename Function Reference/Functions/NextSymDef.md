# NextSymDef

## Description
Function NextSymDef returns a handle to the next definition in the symbol library after the referenced symbol. If the end of the list has been reached, the function returns NIL.

```pascal
FUNCTION NextSymDef(symHd : HANDLE): HANDLE;
```

```python
def vs.NextSymDef(symHd):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symHd|HANDLE|Handle to symbol definition in library.|

## Remarks
If the symHd passed as argument is a symbol folder, the list ignores the symbol definitions. See: [FSymDef](FSymDef.md).

## Examples
```pascal
	h := NextSymDef( h );
END;

BEGIN
	temp_i := InsertImagePopupObjectItem(dialogID,PreviewItem,getSDName(hSymdef));
	hSymDef := nextsymdef(hSymdef);
END;

				IF GetName(ItemHdl) = FoldName THEN FoldHandle := ItemHdl;
	  	 		FindFolderHandle (FInFolder (itemHdl), FoldName, FoldHandle);
			END;
	END;
	itemHdl := NextSymDef (itemHdl);
END;
```
```python
import vs

# Function NextSymDef returns a handle to the next definition in the symbol
# library after the referenced symbol.
symHd = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.NextSymDef(symHd)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```
See also in tutorials: [28. Symbol Instance Schedule](ai%20examples/28_WorksheetSymbolSchedule.md)

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
