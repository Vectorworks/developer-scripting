# SetClVectorFill

## Description
Sets the class fill style to use the specified hatch pattern. The function return value will be TRUE if the operation was successful.

```pascal
FUNCTION SetClVectorFill(
				className : STRING;
				hatchName : STRING): BOOLEAN;
```

```python
def vs.SetClVectorFill(className, hatchName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|hatchName|STRING|Name of hatch pattern.|

## Examples
```pascal
resultOK := SetClVectorFill('Wall', 'Example');
```
```python
import vs

# Sets the class fill style to use the specified hatch pattern.
className = 'None'
hatchName = 'Example'

ok = vs.SetClVectorFill(className, hatchName)
if ok:
    vs.Message('SetClVectorFill succeeded')
else:
    vs.Message('SetClVectorFill failed')
```

## Version
Availability: from VectorWorks9.0

## Category
* [Classes](../Categories/Classes.md)
