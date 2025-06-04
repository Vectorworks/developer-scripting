# SetClLS

## Description
Sets the line style of the specified class.

```pascal
PROCEDURE SetClLS(
				className : STRING;
				LS        : INTEGER);
```

```python
def vs.SetClLS(className, LS):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|LS|INTEGER|Line style index value.|

## Remarks
Assigns the specified line style to the class named className.

## Examples
#### VectorScript ####
```pascal
SetClLS('Property Parcels',-4);
```
#### Python ####
```python

```

## See Also
[GetClLSN|GetClLSN](GetClLSN|GetClLSN.md), [SetClLSN|SetClLSN](SetClLSN|SetClLSN.md) from Vectorworks 2013
[GetClLS|GetClLS](GetClLS|GetClLS.md)

## Version
Availability: from VectorWorks 8.0, deprecated from Vectorworks 2013

## Category
* [Classes](../Categories/Classes.md)
