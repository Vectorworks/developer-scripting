# GetClUseTexture

## Description
Function GetClUseTexture returns whether a classes' texture attributes will be used at object creation.

```pascal
FUNCTION GetClUseTexture(className : STRING): BOOLEAN;
```

```python
def vs.GetClUseTexture(className):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|

## Remarks
Returns whether the class is set to use its texture attributes at object creation.

Respective [SetClUseTexture](SetClUseTexture.md).

## Examples
```pascal
LandruTextureByClass := ((AssignedClGlbTxtr <> 0) & (GetClUseTexture(Concat(TestClass))));

IF (NOT(GetPref(531)))&((NOT ((gClassFFLegs<>'')&(gClassFFLegs<>' ')))|(((gClassFFLegs<>'')&(gClassFFLegs<>' '))&(NOT GetClUseTexture(wrkClsLegs)))) THEN
	BEGIN
		LegAlumHnd := GetObject(intTnmvsSilSatTexture);
		IF (LegAlumHnd <> NIL) THEN
			BEGIN
				IF (GetTypeN(LegAlumHnd) = 97) THEN LegTextIndex := Name2Index(intTnmvsSilSatTexture)
					ELSE
```
```python
import vs

# Function GetClUseTexture returns whether a classes' texture attributes will
# be used at object creation.
className = 'None'

ok = vs.GetClUseTexture(className)
if ok:
    vs.Message('GetClUseTexture succeeded')
else:
    vs.Message('GetClUseTexture failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
