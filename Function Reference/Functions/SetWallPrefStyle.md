# SetWallPrefStyle

## Description
Set the document default wall preferences to match the Wall Style identified by sysName.

```pascal
FUNCTION SetWallPrefStyle(sysName : STRING): BOOLEAN;
```

```python
def vs.SetWallPrefStyle(sysName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sysName|STRING|   |

## Remarks
NZH 5-10-05

## Examples
```pascal
OK := SetWallPrefStyle (wallPrefStyle);
SetZVals (zVal, defaultDz);

{Get the width of the exterior wall style.}
boo := SetWallPrefStyle(extStyle);
extWallWidth := GetWallWidth;

numNewSObjs := 0;
newSObjsCnt := 1;
WHILE (objsCnt <= numSObjs) DO BEGIN
solid_h := sObjs[objsCnt];
BSB := SetWallPrefStyle(StyleRefName);
rOffsetOrg := GetWallWidth;
```
```python
import vs

# Set the document default wall preferences to match the Wall Style
# identified by sysName.
sysName = 'Example'

ok = vs.SetWallPrefStyle(sysName)
if ok:
    vs.Message('SetWallPrefStyle succeeded')
else:
    vs.Message('SetWallPrefStyle failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
