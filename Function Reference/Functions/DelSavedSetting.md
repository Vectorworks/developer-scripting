# DelSavedSetting

## Description
Delete saved settings.

```pascal
FUNCTION DelSavedSetting(
				category : STRING;
				setting  : STRING): BOOLEAN;
```

```python
def vs.DelSavedSetting(category, setting):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|category|STRING|The category for the setting.|
|setting|STRING|The setting to be deleted.|

## Examples
```pascal
resultOK := DelSavedSetting('Example', 'Example');
```
```python
import vs

# Delete saved settings.
category = 'Example'
setting = 'Example'

ok = vs.DelSavedSetting(category, setting)
if ok:
    vs.Message('DelSavedSetting succeeded')
else:
    vs.Message('DelSavedSetting failed')
```

## See Also
VS Functions:
[DelSavedSettings](DelSavedSettings.md) 
| [SetSavedSetting](SetSavedSetting.md) 
| [GetSavedSetting](GetSavedSetting.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
