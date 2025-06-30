# ResolveByClassTextureRef

## Description
Function ResolveByClassTextureRef returns the internal index, or name, of the texture assigned to the referenced object. 

Primary, secondary, or tertiary texture assignments can be returned for objects that support multiple textures, such as roofs or walls. For objects that do not support multiple textures, pass 0 to the partID parameter.

* Table - Object Texture Reference

| Texture | Index Value |
|---------|-------------|
| Primary | 0 |
| Secondary | 1 |
| Tertiary | 2 |

```pascal
FUNCTION ResolveByClassTextureRef(
				obj    : HANDLE;
				partID : INTEGER): LONGINT;
```

```python
def vs.ResolveByClassTextureRef(obj, partID):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Primary, secondary, or tertiary texture ID to be returned.|

## Remarks
If the texture ref for an object is set to -1, it will use the texture of its class.  This routine will look up the object's class and return the class' texture ref.

Julian Carr [25 April 2014]: I don't believe this works as described. If you create an extrude, put it in a class that has a texture applied in the Other tab, then run this code:

    Message(ResolveByClassTextureRef(FSActLayer, -1));

it will only return a value if the selected extrude has the Texture popup set to Class Texture in the OIP. Otherwise it returns 0. It does not apply the class texture to the object

## Examples
#### VectorScript ####
```pascal
textureID := ResolveByClassTextureRef(handleToObject, 0);
```
#### Python ####
```python

```

## See Also
VS Functions:
[SetTextureRef](SetTextureRef.md) 
| [GetTextureRef](GetTextureRef.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
