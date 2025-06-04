# GetCVis

## Description
Returns the visibility status of the specified class.

```pascal
FUNCTION GetCVis(className : STRING): INTEGER;
```

```python
def vs.GetCVis(className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
Also, though a warning is generated, passing a string to a non-existent class returns 0.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
BEGIN
Message(GetCVis('Dimension'));
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	vs.Message(vs.GetCVis('Dimension'))
Example()
```

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
