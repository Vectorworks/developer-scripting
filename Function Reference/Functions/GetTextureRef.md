# GetTextureRef

## Description
Function GetTextureRef returns the texture reference ID for the referenced object. The integer returned is the internal index of the texture node used by this object.

```pascal
FUNCTION GetTextureRef(
				obj            : HANDLE;
				partID         : INTEGER;
				resolveByClass : BOOLEAN): LONGINT;
```

```python
def vs.GetTextureRef(obj, partID, resolveByClass):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Identifies texture to be returned by part ID.|
|resolveByClass|BOOLEAN|Resolve texture reference by class.|

## Remarks
Returns the texture ref for this object, which is the internal index, or name, of the texture node used by this object.  The texture is specific to the partID part of the object (0 = Primary, 1 = Secondary, or 2 = Tertiary).  Walls can have three different textures and roofs can have two if they are 'expanded'.  Textures may be applied by class.  If resolveByClass is true then this function will return the texture ref for this object?s class.


I'd expected the 'resolveByClass' to be a VAR. Instead you can use GetTextureRef(obj, partID, FALSE). The longint returned will be -1, if the texture is by class:

<code lang="pas">
message(GetTextureRef(obj, partID, TRUE), ' * ', GetTextureRef(obj, partID, FALSE));
{ returns the id of the texture on the left call and -1 on the right call, if it is by class }
</code>

See [[VS:SetTextureRef]] remarks.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
