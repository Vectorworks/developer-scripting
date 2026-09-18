# IFC_ExportWithUI

## Description
Exports IFC file, showing Export IFC Project dialog

```pascal
PROCEDURE IFC_ExportWithUI(bExpSingleObj : BOOLEAN);
```

```python
def vs.IFC_ExportWithUI(bExpSingleObj):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|bExpSingleObj|BOOLEAN|Set to False.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	ok : BOOLEAN;
BEGIN
	ok := IFC_ExportWithUI(FALSE);
END;

RUN(Test);
```
#### Python ####
```python
ok = vs.IFC_ExportWithUI(FALSE)
```

```pascal
IFC_ExportWithUI(TRUE);
```
```python
import vs

# Exports IFC file, showing Export IFC Project dialog.
bExpSingleObj = True

vs.IFC_ExportWithUI(bExpSingleObj)
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
