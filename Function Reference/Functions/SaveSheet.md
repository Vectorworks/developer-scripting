# SaveSheet

## Description
Procedure SaveSheet saves current view, page, class, and layer settings in a new sheet with a specified name.   The saveView, saveClass and saveLayer parameters can be used to selectively not save an aspect of the view.  Also after the sheet is created, the SetObjectVariableBoolean function can be used to control whether to utilize the view, page, class or layer settings.

```pascal
PROCEDURE SaveSheet(
				name      : STRING;
				saveView  : BOOLEAN;
				saveClass : BOOLEAN;
				saveLayer : BOOLEAN);
```

```python
def vs.SaveSheet(name, saveView, saveClass, saveLayer):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of saved sheet.|
|saveView|BOOLEAN|Saves view settings.|
|saveClass|BOOLEAN|Saves class settings.|
|saveLayer|BOOLEAN|Saves layer settings.|

## Remarks
Saves the current view,  page, class, and layer settings in a new sheet with the given name. The saveView, saveClass, and saveLayer booleans can be used to selectively not save an aspect of the view.

[sd 8/18/98]

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
savedViewHandle  :HANDLE;
ovSheetSaveView	  :BOOLEAN;
ovSheetSavePage	  :BOOLEAN;
ovSheetSaveClass :BOOLEAN;
ovSheetSaveLayer :BOOLEAN;
BEGIN
savedViewHandle := GetObject('Untitled View');
IF savedViewHandle <> NIL THEN BEGIN
ovSheetSaveView  := GetObjectVariableBoolean(savedViewHandle, 450);
ovSheetSavePage  := GetObjectVariableBoolean(savedViewHandle, 451);
ovSheetSaveClass := GetObjectVariableBoolean(savedViewHandle, 452);
ovSheetSaveLayer := GetObjectVariableBoolean(savedViewHandle, 453);
AlrtDialog(Concat(
'handle type: ', GetType(savedViewHandle), Chr(13),
'save view: ',  ovSheetSaveView,  Chr(13),
'save page: ',  ovSheetSavePage,  Chr(13),
'save class: ', ovSheetSaveClass, Chr(13),
'save layer: ', ovSheetSaveLayer));
END;
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks8.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
