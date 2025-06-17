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
|texLayerID|LONGINT|Texture layer ID, 0 for base, &gt;0 for decals|
|resolveByClass|BOOLEAN|   |

## Remarks
*\_c\_* (2017.12.30): This was always a cryptical call, below an example from my own notes:
<code lang="vs">
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

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
