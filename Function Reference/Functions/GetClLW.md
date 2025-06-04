# GetClLW

## Description
Returns the line weight of the specified class.

```pascal
FUNCTION GetClLW(className : STRING): INTEGER;
```

```python
def vs.GetClLW(className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
Returns the line weight of the class named className.

## Examples
#### VectorScript ####
```pascal
pbLineWt:= GetClLW('Property Bounds');
```
#### Python ####
```python
pbLineWt = vs.GetClLW('Property Bounds')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
