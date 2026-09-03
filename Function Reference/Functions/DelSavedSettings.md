# DelSavedSettings

## Description
Delete all saved settings in the specified category.

```pascal
FUNCTION DelSavedSettings(category : STRING): BOOLEAN;
```

```python
def vs.DelSavedSettings(category):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|category|STRING|The category to be deleted.|

## Examples
```pascal
BEGIN
	B := DelSavedSettings(kSavSetCat);
	B := DelSavedSettings(kOldSavSetCat);
```
```python
import vs

# Delete all saved settings in the specified category.
category = 'Example'

ok = vs.DelSavedSettings(category)
if ok:
    vs.Message('DelSavedSettings succeeded')
else:
    vs.Message('DelSavedSettings failed')
```

## See Also
VS Functions:
[DelSavedSetting](DelSavedSetting.md) 
| [SetSavedSetting](SetSavedSetting.md) 
| [GetSavedSetting](GetSavedSetting.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
