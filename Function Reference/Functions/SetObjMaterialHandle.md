# SetObjMaterialHandle

```pascal
FUNCTION SetObjMaterialHandle(
				VAR objectHandle : HANDLE;
				materialHandle   : HANDLE): BOOLEAN;
```

```python
def vs.SetObjMaterialHandle(objectHandle, materialHandle):
    return (BOOLEAN, objectHandle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|   |
|materialHandle|HANDLE|   |

## Examples
```pascal
BEGIN
	IF (objH <> NIL) THEN BEGIN
		bMaterialOK := SetObjMaterialHandle(objH, archCompMaterialH);
		{AlrtDialog( concat('@ SET_ARCH_Material(), textureByMaterial = ', textureByMaterial, ', archCompTextureID = ', archCompTextureID) );}
		if (textureByMaterial = false) then
			SetTextureRef (objH, archCompTextureID, kTexturePart_Overall );
	END;
```
```python
import vs

objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
materialHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok, objectHandle = vs.SetObjMaterialHandle(objectHandle, materialHandle)
vs.Message('SetObjMaterialHandle returned: ' + str((ok, objectHandle)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
