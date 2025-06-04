# SetClUseGraphic

## Description
Toggles the document setting for using the graphic attributes of the specified class at object creation.

```pascal
PROCEDURE SetClUseGraphic(
				className : STRING;
				use       : BOOLEAN);
```

```python
def vs.SetClUseGraphic(className, use):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|use|BOOLEAN|Use graphic attributes on-off setting.|

## Remarks
Sets whether the class graphic attributes are used at object creation.

## Examples
==== VectorScript ====
```pascal
SetClUseGraphic('Forested Cover',TRUE);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
