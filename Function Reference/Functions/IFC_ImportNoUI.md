# IFC_ImportNoUI

## Description
Imports IFC file without showing any dialog.

```pascal
PROCEDURE IFC_ImportNoUI(strFilePath : STRING);
```

```python
def vs.IFC_ImportNoUI(strFilePath):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strFilePath|STRING|File path.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;

BEGIN
	IFC_ImportNoUI('D:\Import\Test.ifc');
END;

RUN(Test);
```
==== Python ====
```python
vs.IFC_ImportNoUI('D:\Import\Test.ifc')
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
