# GetNumberOfDLComponents

## Description
Gets the number of components in the Double Line Preferences.

```pascal
FUNCTION GetNumberOfDLComponents(VAR numComponents : INTEGER): BOOLEAN;
```

```python
def vs.GetNumberOfDLComponents():
    return (BOOLEAN, numComponents)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|numComponents|INTEGER|Returns the number of components.|

## Remarks
CJG 6-27-06

## Examples
```pascal
resultOK := GetNumberOfDLComponents(1);
```
```python
import vs

# Gets the number of components in the Double Line Preferences.
ok, numComponents = vs.GetNumberOfDLComponents()
vs.Message('GetNumberOfDLComponents returned: ' + str((ok, numComponents)))
```

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
