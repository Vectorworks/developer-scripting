# GetClVectorFill

## Description
Returns the name of the hatch pattern setting of the specified class.

The function return value will be TRUE if the class uses a hatch pattern, and will be FALSE if the class does not use a hatch pattern.

```pascal
FUNCTION GetClVectorFill(
				className     : STRING;
				VAR hatchName : STRING): BOOLEAN;
```

```python
def vs.GetClVectorFill(className):
    return (BOOLEAN, hatchName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|hatchName|STRING|Name of active hatch pattern (if it exists).|

## Version
Availability: from VectorWorks9.0

## Category
* [Classes](../Categories/Classes.md)
