# GetWSImage

## Description
Returns a handle to the on-drawing object (image) of the referenced worksheet.

```pascal
FUNCTION GetWSImage(worksheet : HANDLE): HANDLE;
```

```python
def vs.GetWSImage(worksheet):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|

## Examples
```pascal
BEGIN
RecalculateWS(GetObject(kRLwkshtName));
ResetObject(GetObject(kRLwkshtName));
ShowWS(GetObject(kRLwkshtName),TRUE);
WSImage := GetWSImage(GetObject(kRLwkshtName));
IF WSImage <> NIL THEN ResetObject(WSImage);
END

BEGIN
RecalculateWS( MyWSHandle );
SetRField(objHand, objName, 'UpdateWS', 'FALSE');
ResetObject(MyWSHandle);
WSImage := GetWSImage(MyWSHandle);
IF WSImage <> NIL THEN ResetObject(WSImage);
END

	SetWSCellFormula(tempHandle,2,2,2,2,'1');
	ShowWS(tempHandle,TRUE);	{Show WS}
	RecalculateWS( tempHandle );
	ResetObject(tempHandle);
	WSImage := GetWSImage(tempHandle);
	IF WSImage <> NIL THEN ResetObject(WSImage);
	PopAttrs;
END;
```
```python
import vs

# Returns a handle to the on-drawing object (image) of the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet

objHandle = vs.GetWSImage(worksheet)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
