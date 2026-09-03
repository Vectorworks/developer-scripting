# SetTopVisibleWS

## Description
Brings the referenced worksheet to the front of any open worksheet windows.

```pascal
PROCEDURE SetTopVisibleWS(worksheet : HANDLE);
```

```python
def vs.SetTopVisibleWS(worksheet):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|

## Examples
```pascal
BEGIN
	CASE gFindMode OF
	1:	BEGIN
			ShowWS( WSh, TRUE );
			SetTopVisibleWS( WSh );
			SetWSCurrentCell(WSh, row, col);
			ProcessFoundCell := TRUE;
		END;
```
```python
import vs

# Brings the referenced worksheet to the front of any open worksheet windows.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet

vs.SetTopVisibleWS(worksheet)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
