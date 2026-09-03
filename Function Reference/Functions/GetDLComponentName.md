# GetDLComponentName

## Description
Gets the name of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentName(index : INTEGER): STRING;
```

```python
def vs.GetDLComponentName(index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|

## Remarks
CJG 3-23-07

## Examples
```pascal
resultStr := GetDLComponentName(1);
```
```python
import vs

# Gets the name of the component at index in the Double Line Preferences.
index = 1

name = vs.GetDLComponentName(index)
vs.Message('GetDLComponentName returned: ' + str(name))
```

## See Also
VS Functions:
[SetDLComponentName](SetDLComponentName.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
