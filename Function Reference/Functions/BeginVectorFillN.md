# BeginVectorFillN

## Description
Procedure BeginVectorFillN creates a new vector fill definition in a VectorWorks document. The value of vectorFillName will change only if the hatch name already exists.

A color table listing with associated index values can be found in the [[VS:Function Reference Appendix#Color Palette|Appendix]].

```pascal
PROCEDURE BeginVectorFillN(
				VAR vectorFillName : STRING;
				pageSpace          : BOOLEAN;
				rotateInWall       : BOOLEAN;
				colorIndex         : INTEGER);
```

```python
def vs.BeginVectorFillN(vectorFillName, pageSpace, rotateInWall, colorIndex):
    return vectorFillName
```

## Parameters
|Name|Type|Description|
|---|---|---|
|vectorFillName|STRING|Name of new vector fill pattern.|
|pageSpace|BOOLEAN|Sets page or world space for vector fill.|
|rotateInWall|BOOLEAN|Sets rotate in wall option for vector fill.|
|colorIndex|INTEGER|Background color of vector fill.|

## Remarks
Begins a hatch definition.  vectorFillName will return with a different name if the input name already is being used in the document.

This is a new version of BeginVectorFill which returns the actual name of the hatch in the VAR STRING.


We have found a problem with the VectorScript function BeginVectorFillN in that it is currently impossible to create a hatch that has an opaque white (color 0) background.  We would like to change this so that any hatches it creates always has an opaque background.  To give a hatch a transparent background, there is already a SetObjectVariableBoolean call (value 661) to do this.

## Examples
dHatchToResource}}

## See Also
VS Functions:
[AddVectorFillLayer](AddVectorFillLayer.md) 
| [EndVectorFill](EndVectorFill.md)

## Version
Availability: from VectorWorks8.0

## Category
* Hatches @ Vector Fills

