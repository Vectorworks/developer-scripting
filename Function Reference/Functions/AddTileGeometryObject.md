# AddTileGeometryObject

## Description
Adds the specified object to the specified tile resource.

```pascal
FUNCTION AddTileGeometryObject(
				tileHandle   : HANDLE;
				objectHandle : HANDLE): BOOLEAN;
```

```python
def vs.AddTileGeometryObject(tileHandle, objectHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The handle to the tile resource.|
|objectHandle|HANDLE|The handle to the object to add.|

## Examples
```pascal
return := AddTileGeometryGroup(tileHandle, objectHandle);
```

```pascal
resultOK := AddTileGeometryObject(tileHandle, objectHandle);
```
```python
import vs

# Adds the specified object to the specified tile resource.
tileHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
objectHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.AddTileGeometryObject(tileHandle, objectHandle)
if ok:
    vs.Message('AddTileGeometryObject succeeded')
else:
    vs.Message('AddTileGeometryObject failed')
```

## See Also
VS Functions:
[CreateTile](CreateTile.md) 
| [ShowEditTileDialog](ShowEditTileDialog.md) 
| [ShowEditTileSettingsDialog](ShowEditTileSettingsDialog.md) 
| [ShowNewTileDialog](ShowNewTileDialog.md) 
| [GetTileGeometryGroup](GetTileGeometryGroup.md) 
| [BeginGroupN](BeginGroupN.md) 
| [AddTileGeometryObject](AddTileGeometryObject.md) 
| [GetTileGroupParent](GetTileGroupParent.md) 
| [IsTileGroupContainedObject](IsTileGroupContainedObject.md) 
| [GetTileBackgroundColor](GetTileBackgroundColor.md) 
| [SetTileBackgroundColor](SetTileBackgroundColor.md) 
| [GetTileRepetitionPoint](GetTileRepetitionPoint.md) 
| [SetTileRepetitionPoint](SetTileRepetitionPoint.md) 
| [GetTileOffsetPoint](GetTileOffsetPoint.md) 
| [SetTileOffsetPoint](SetTileOffsetPoint.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
