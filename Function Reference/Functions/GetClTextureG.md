# GetClTextureG

## Description
Function GetClTextureG returns the generic texture of the specified class.

```pascal
FUNCTION GetClTextureG(className : STRING): LONGINT;
```

```python
def vs.GetClTextureG(className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|

## Remarks
Returns the generic texture of the class named className.

## Examples
```pascal
BEGIN
TextureIDX := GetClTextureG(pHidden);
IF TextureIDX <> 0 THEN
	 SetTextureRef(parmHand,TextureIDX,0);
END;

BEGIN
regtex := GetClTextureG(roof_class);
rooftex := GetClTextureT(roof_class);
IF ((rooftex = 0) & (regtex <> 0)) THEN SetClTextureT(roof_class,regtex);
END;

	IF ( gActStringerPane < 2 ) THEN stringerClassStr := gLStringerClassData.strClassActualName
	ELSE                             stringerClassStr := gRStringerClassData.strClassActualName;
	{by:PP set texture part overall = 3}
	IF stringerClassStr <> '' THEN
		SetTextureRef( resultH, GetClTextureG( stringerClassStr ), 3 )
	ELSE
		SetTextureRef( resultH, -1, 3 );
END;
```
```python
import vs

# Function GetClTextureG returns the generic texture of the specified class.
className = 'None'

resultN = vs.GetClTextureG(className)
vs.Message('GetClTextureG returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
