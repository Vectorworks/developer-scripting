# GetComponentName

## Description
Gets the name of a component in an object.

```pascal
FUNCTION GetComponentName(
				obj            : HANDLE;
				componentIndex : INTEGER): STRING;
```

```python
def vs.GetComponentName(obj, componentIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component, 1-based.|

## Examples
```pascal
BEGIN
	slabName[ctr2] := GetComponentName( temp_h, ctr2 );
	IF slabName[ctr2] = '' THEN
	BEGIN
		slabName[ctr2] := Concat( num2str( 0, ctr2 ), GetPluginString(5008) );
	END;
```
```python
import vs

# Gets the name of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

name = vs.GetComponentName(obj, componentIndex)
vs.Message('GetComponentName returned: ' + str(name))
```

## See Also
VS Functions:
[SetComponentName](SetComponentName.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
