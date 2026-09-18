# FFillBack

## Description
Procedure FFillBack returns the current fill background color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE FFillBack(
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.FFillBack():
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Examples
#### VectorScript ####
```pascal
FFillBack(redValue,greenValue,blueValue);
```
#### Python ####
```python
redValue,greenValue,blueValue = vs.FFillBack()
```

```pascal
BEGIN
	FFillFore (R, G, B);
	SetFillFore (objectH, R, G, B);
	FFillBack (R, G, B);
	SetFillBack (objectH, R, G, B);
END;

structCompsNeedUpdate	:= ((structMaterialIDNum = updatedMaterialID)	& (textureByMaterial = false)) | ((structMaterialIDNum = 0) & materialDeleted);
{AlrtDialog(concat(' Inside HandleMaterialChange(), textureNeedsUpdate = ', textureNeedsUpdate, '  ,  archMaterialIDNum = ', archMaterialIDNum, '  , structMaterialIDNum = ', structMaterialIDNum,
												'  , updatedMaterialID =', updatedMaterialID, ' , archCompsNeedUpdate = ', archCompsNeedUpdate, ' , structCompsNeedUpdate = ', structCompsNeedUpdate)); }
FFillFore(redValue,		greenValue,		blueValue);
FFillBack(redValueBack, greenValueBack, blueValueBack);

begin
	FFillBack(redValue,greenValue,blueValue);
	SetFillBack(LNewObj, redValue,greenValue,blueValue);
end;
```
```python
import vs

# Procedure FFillBack returns the current fill background color.
red, green, blue = vs.FFillBack()
vs.Message('FFillBack returned: ' + str((red, green, blue)))
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
