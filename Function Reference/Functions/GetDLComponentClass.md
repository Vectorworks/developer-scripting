# GetDLComponentClass

## Description
Gets the class of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentClass(
				index              : INTEGER;
				VAR componentClass : LONGINT): BOOLEAN;
```

```python
def vs.GetDLComponentClass(index):
    return (BOOLEAN, componentClass)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|componentClass|LONGINT|Returns the class of the component.|

## Remarks
CJG 3-23-07

## Examples
```pascal
resultOK := GetDLComponentClass(1, 2);
```
```python
import vs

# Gets the class of the component at index in the Double Line Preferences.
index = 1

ok, componentClass = vs.GetDLComponentClass(index)
vs.Message('GetDLComponentClass returned: ' + str((ok, componentClass)))
```

## See Also
VS Functions:
[SetDLComponentClass](SetDLComponentClass.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
