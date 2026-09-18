# vsoButtonGetResource

## Description
Show a resource popup from the current shape pane button (while handing action 35: {ParametricUIButtonHitMessage::kAction}). Parameter name is a string that will receive the resource name.

```pascal
FUNCTION vsoButtonGetResource(
				paramName  : STRING;
				objectType : INTEGER;
				folderSpec : INTEGER;
				folderName : STRING): BOOLEAN;
```

```python
def vs.vsoButtonGetResource(paramName, objectType, folderSpec, folderName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paramName|STRING|   |
|objectType|INTEGER|   |
|folderSpec|INTEGER|   |
|folderName|STRING|   |

## Examples
```pascal
BEGIN
	IF vsoButtonGetResource('TypeSymbol',16,gATSSpeakersFldIdx,gATSSpeakersFldNam) THEN BEGIN END;
	IF (ghParm = NIL) THEN
		BEGIN
			ghparm := GetObject(kPIOName);
			SpkrUsrType := GetRField(ghParm,kPIOName,'TypeSymbol');

IF vsoButtonGetResource('projectors',16,gPJModIdx,gPJModFolder) THEN BEGIN END;

			machinename := GetRField( ghParm, kPIOName, 'PJModel');
			SetRField (ghParm, kPIOName, '__StoredPJ',Concat(machinename));
			ForEachObjectInLayer (StoredPJWrite,	kFOILSelectedOnly,	kFOILTraverseGroups,	kFOILEditableLayers);
		END;
IF vsoButtonGetResource('PJModel',16,gPJModIdx,gPJModFolder) THEN BEGIN END;
```
```python
import vs

# Show a resource popup from the current shape pane button (while handing
# action 35: {ParametricUIButtonHitMessage::kAction}).
paramName = 'Example'
objectType = 0
folderSpec = 1
folderName = 'C:/Temp'

ok = vs.vsoButtonGetResource(paramName, objectType, folderSpec, folderName)
if ok:
    vs.Message('vsoButtonGetResource succeeded')
else:
    vs.Message('vsoButtonGetResource failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [Object Events](../Categories/Object%20Events.md)
