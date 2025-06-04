# SetCustomObjectSelectionGroup

## Description
Set selection indication geometry for a parametric object.

See [[VS:Parametric Custom Selection Indication]] for more info.

```pascal
FUNCTION SetCustomObjectSelectionGroup(
				objectHand : HANDLE;
				selGroup   : HANDLE): BOOLEAN;
```

```python
def vs.SetCustomObjectSelectionGroup(objectHand, selGroup):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to parametric object.|
|selGroup|HANDLE|Handle to object or group that contains geometry for selection indication.|

## Version
Availability: from Vectorworks14.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
