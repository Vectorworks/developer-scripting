# SelectSS

## Description
Procedure SelectSS opens the referenced worksheet and makes it active.

```pascal
PROCEDURE SelectSS(h : HANDLE);
```

```python
def vs.SelectSS(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|

## Remarks
OBSOLETE for Version 9: see new ShowWS. [VML 01/09/01]

## Examples
```pascal
	END;
2:	BEGIN
		ShowWS( WSh, TRUE );{activate and Open to Show single change}
		SetTopVisibleWS( WSh );
		{SelectSS(hWS);{activate and Open to Show single change}
		GetWSCellTextFormat( WSh, row, col, fontIdx, fontSize, fontStyle );
		ReplaceStr(str,gFindString,gReplString,gCase);
		SetWSCellFormula( WSh, row, col, row, col, gResultText );
		SetWSCellTextFormat(WSh,row,col,row,col,fontIdx,fontSize,fontStyle);
```
```python
import vs

# Procedure SelectSS opens the referenced worksheet and makes it active.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SelectSS(h)
```

## Version
SelectSS is obsolete as of VectorWorks9.0<P>

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
