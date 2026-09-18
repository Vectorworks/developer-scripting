# Index2Name

## Description
Function Index2Name returns the name of the object with specified index number.

```pascal
FUNCTION Index2Name(index : LONGINT): STRING;
```

```python
def vs.Index2Name(index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|LONGINT|Object index number.|

## Remarks
Returns the name of the object with the internal index specified.

## Examples
```pascal
BEGIN
	resHand	:= GetObject(Index2Name(-patID));
	resType	:= GetTypeN(resHand);
	IF (resType = 108{kTileDefNode}) OR (resType = 119{kImageDefNode}) OR (resType = 120{kGradientDefNode}) THEN
		SetFPat(objHand,1);
END;

SetElement(xmlID, 'CreateJoistsFromPoly/FramingFillFore', 		Num2StrF(FramingFillFore));
SetElement(xmlID, 'CreateJoistsFromPoly/FramingFillBack', 		Num2StrF(FramingFillBack));
SetElement(xmlID, 'CreateJoistsFromPoly/FramingPenColor', 		Num2StrF(FramingPenColor));
IF (FramingPenLine <> 2) THEN
	SetElement(xmlID, 'CreateJoistsFromPoly/FramingPenLine', 	Index2Name(-FramingPenLine))
ELSE
	SetElement(xmlID, 'CreateJoistsFromPoly/FramingPenLine', 	'');

BEGIN
	TempTextRef := GetTextureRef(h,0,TRUE);
	ChairTexture := Index2Name(TempTextRef);
	FoundTexture := TRUE;
END;
```
```python
import vs

# Function Index2Name returns the name of the object with specified index number.
index = 1

name = vs.Index2Name(index)
vs.Message('Index2Name returned: ' + str(name))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Names](../Categories/Object%20Names.md)
