# SetClFPat

## Description
Sets the fill pattern of the specified class.

To apply a bitmap fill pattern, use a positive value corresponding to the desired fill pattern index. To apply a vector fill, use the negative of the index of the vector fill (index * -1).

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
PROCEDURE SetClFPat(
				className   : STRING;
				fillpattern : LONGINT);
```

```python
def vs.SetClFPat(className, fillpattern):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|fillpattern|LONGINT|Fill pattern index value.|

## Remarks
Assigns a fill pattern to the class named className.

## Examples
#### VectorScript ####
```pascal
SetClFPat('Grassy Cover',42);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
