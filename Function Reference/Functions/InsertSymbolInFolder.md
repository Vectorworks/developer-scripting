# InsertSymbolInFolder

## Description
Inserts a symbol definition into the referenced symbol folder.

```pascal
PROCEDURE InsertSymbolInFolder(
				targetFolder : HANDLE;
				symbolDef    : HANDLE);
```

```python
def vs.InsertSymbolInFolder(targetFolder, symbolDef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|targetFolder|HANDLE|Handle to symbol folder.|
|symbolDef|HANDLE|Handle to symbol definition.|

## Examples
```pascal
					ThrowAwayBool := SetParent(gSelobjHandles[SketchIndex], TmpSketchSymHandle);
				END;
			If LocHand <> NIL then DelObject(LocHand);
			{Place Sym in Sym Folder}
			InsertSymbolInFolder(SketchFolderHan, TmpSketchSymHandle);
			Symbol(TmpSketchName, 0, 0, 0);
			TmpSketchSymHandle := LNewObj;
		END; {SketchFolderHan <> NIL}
END; {Create Sketch Symbol}

transferdata(PIO2Duplicate,pio_temp_h);
transferattr(PIO2Duplicate,pio_temp_h);
symdef_h := getobject(symname_s);
setobjectvariableboolean(symdef_h,127,TRUE);
InsertSymbolInFolder(folder_h,symdef_h);
SetSelect(PIO2Duplicate);
redraw;
END;

	BEGIN
		folderName := GetFName;
		SymFolderHan := GetObject(folderName);
		IF SymFolderHan <> NIL THEN InsertSymbolInFolder(SymFolderHan, SymHan);
		SetActSymbol (SymName);
	END; {SymHan <> NIL}
END; {PutSymInBorderFolder}
```
```python
import vs

# Inserts a symbol definition into the referenced symbol folder.
targetFolder = vs.FSActLayer()  # handle to the first selected object on the active layer
symbolDef = vs.GetObject('MySymbol')  # handle to a symbol definition

vs.InsertSymbolInFolder(targetFolder, symbolDef)
```

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
