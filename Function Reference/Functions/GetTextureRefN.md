# GetTextureRefN

## Description
Returns the texture reference for a specified object.

```pascal
FUNCTION GetTextureRefN(
				obj            : HANDLE;
				texPartID      : LONGINT;
				texLayerID     : LONGINT;
				resolveByClass : BOOLEAN): LongInt;
```

```python
def vs.GetTextureRefN(obj, texPartID, texLayerID, resolveByClass):
    return LongInt
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|Texture layer ID, 0 for base, >0 for decals|
|resolveByClass|BOOLEAN|   |

## Remarks
*\_c\_* (2017.12.30): This was always a cryptical call, below an example from my own notes:
```pascal
{ set texLayerID to 0, if you don't have decals you want to access }

GetTextureRefN(obj, 3, 0, FALSE); 
{ returns info on the overall part (3)
* texture index if the part is "texture"  
* 0 if the part is "None"   
* -1 if the part is "Class Texture"  
}

GetTextureRefN(obj, 3, 0, TRUE); 
{ returns info on the overall part (3)
* texture index if the part is "texture"  
* 0 if the part is "None"   
* index of the class texture if the part is "Class Texture"  
}
```

## Examples
```pascal
TextureID := GetTextureRefN(h,PartCount,0,FALSE);
```
```python
	# Attach a texture space to the object.
	vs.AttachDefaultTextureSpace( objectHand, 0 )
# Get the texture index assigned to the PIO.
partTexIndex = vs.GetTextureRefN( objectHand, 0, 0 False )
if partTexIndex in (-1, 0):
	# Attach the proper texture to the object.
	vs.SetTextureRefN( objectHand, TextureObjs.PIOTexIndex, 0, 0 )
```

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
