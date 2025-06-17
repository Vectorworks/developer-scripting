# SetTextureRefN

## Description
Sets the texture reference for a specified object

```pascal
PROCEDURE SetTextureRefN(
				obj        : HANDLE;
				textureRef : LONGINT;
				texPartID  : LONGINT;
				texLayerID : LONGINT);
```

```python
def vs.SetTextureRefN(obj, textureRef, texPartID, texLayerID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|textureRef|LONGINT|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|0 for base, &gt;0 for decals|

## Remarks
[[User:CBM-c-| _c_]], 2021.02.21:
This actually creates the part if it wasn't there before.

textureRef:
* index = texture index 
* 0 = None  
* -1 = Class Texture  

texPartID flags, check the VS:Function_Reference_Appendix#Tex: Texture Part ID or more completely the SDK file RenderOptionsValues.h:

* 3: overall for any kind of object 
* 4: top in extrudes/sweeps 
* 5: bottom in extrudes/sweeps 
* 6: sides in extrudes/sweeps 
* 7: left in walls 
* 8: right in walls 
* 9: start cap in walls 
* 10: end cap in walls 
* 11: top in walls 
* 12: bottom in walls 
* 13: holes in walls 
* 14: top in roof faces/slabs 
* 15: bottom in roof faces/slabs 
* 16: sides in roof faces/slabs 
* 17: top in roofs 
* 18: bottom in roofs 
* 19: sides in roofs 
* 20: gable in roofs 
* 21: fascia in roofs 
* 22: attic in roofs 
* 23: soffit in roofs 
* 24: dutch walls in roofs 
* 25: dormer walls in roofs 
* 26: frame cap in curtain walls 
* 27: panel face in curtain walls 

Examples:
```pascal
 SetTextureRefN(obj, textureIndex, texPartID, texLayerID) { sets texture to an index }

 { texLayerID is always 0, if there are no decals }
 SetTextureRefN(obj, 0, 7, 0) { sets left texture (7) to inherit from parent container, excluding if it's by class }
 SetTextureRefN(obj, 0, 3, 0) { sets overall texture (3) to inherit from parent container, excluding if it's by class }
 SetTextureRefN(obj, -1, 3, 0) { sets overall (3) texture to by class according to part }
 SetTextureRefN(obj, -2, 3, 0) { sets overall (3) texture to "none" }
```

([[User_talk:Ptr|Ptr]], 2020 Sep. 8):
<code lang="py">
vs.SetTextureRefN(obj, textureRef, texPartID, texLayerID)
```
<lineList ident=1>
<line>textureRef: texture index, -1 for by class</line>
<line>texPartID: 3 = overall part</line>
<line>texLayerID: 0 for no decals</line>

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
