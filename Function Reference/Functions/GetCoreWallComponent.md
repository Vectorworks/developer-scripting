# GetCoreWallComponent

## Description
Gets the core wall component of an object.

```pascal
FUNCTION GetCoreWallComponent(obj : HANDLE): INTEGER;
```

```python
def vs.GetCoreWallComponent(obj):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|

## Examples
```pascal
BEGIN
result := GetNumberOfComponents( extStyle_h, numberOfComponents );
coreComponentIndex := GetCoreWallComponent( extStyle_h );
IF coreComponentIndex <> 0 THEN
	BEGIN
	for cnt:= 1 to numberOfComponents DO
		BEGIN

wallStyleName := GetWallStyle(wall_h);
wallStyleHand := GetObject(wallStyleName);
IF wallStyleHand <> NIL THEN BEGIN
	result := GetNumberOfComponents( wallStyleHand, numberOfComponents );
	coreComponentIndex := GetCoreWallComponent( wallStyleHand );
	temp_r := 0;
	IF coreComponentIndex <> 0 THEN BEGIN 					{ there is core component in the current wall style}
		for cnt:= 1 to numberOfComponents DO BEGIN 			{ traverse wall style components }
			result := GetComponentWidth( wallStyleHand, cnt, currTMPOffset );
```
```python
import vs

# Gets the core wall component of an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetCoreWallComponent(obj)
vs.Message('GetCoreWallComponent returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetCoreWallComponent](SetCoreWallComponent.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
