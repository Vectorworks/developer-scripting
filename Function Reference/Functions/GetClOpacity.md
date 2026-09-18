# GetClOpacity

## Description
Gets the opacity of the specified class.

```pascal
FUNCTION GetClOpacity(className : STRING): INTEGER;
```

```python
def vs.GetClOpacity(className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|   |

## Examples
```pascal
BEGIN
	objectClass := GetClass(gTempH);
	shadowOpacity := GetClOpacity(objectClass);
END;
```
```python
import vs

# Gets the opacity of the specified class.
className = 'None'

resultN = vs.GetClOpacity(className)
vs.Message('GetClOpacity returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Classes](../Categories/Classes.md)
