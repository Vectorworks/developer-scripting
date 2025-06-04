# SetClLW

## Description
Sets the line weight of the specified class.

```pascal
PROCEDURE SetClLW(
				className : STRING;
				LW        : INTEGER);
```

```python
def vs.SetClLW(className, LW):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|LW|INTEGER|Line weight value (in mils).|

## Remarks
Assigns the specified line style to the class named className.

## Examples
==== VectorScript ====
```pascal
SetClLW('To Be Demolished',28);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
