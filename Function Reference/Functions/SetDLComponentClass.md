# SetDLComponentClass

## Description
Sets the class of the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLComponentClass(
				index          : INTEGER;
				componentClass : LONGINT): BOOLEAN;
```

```python
def vs.SetDLComponentClass(index, componentClass):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|componentClass|LONGINT|The class of the component.|

## Remarks
CJG 3-23-07

## Examples
```pascal
resultOK := SetDLComponentClass(1, 2);
```
```python
import vs

# Sets the class of the component at index in the Double Line Preferences.
index = 1
componentClass = 1

ok = vs.SetDLComponentClass(index, componentClass)
if ok:
    vs.Message('SetDLComponentClass succeeded')
else:
    vs.Message('SetDLComponentClass failed')
```

## See Also
VS Functions:
[GetDLComponentClass](GetDLComponentClass.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
