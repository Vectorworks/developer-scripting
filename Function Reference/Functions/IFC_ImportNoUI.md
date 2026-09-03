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
#### VectorScript ####
```pascal
PROCEDURE Test;

BEGIN
	IFC_ImportNoUI('D:\Import\Test.ifc');
END;

RUN(Test);
```
#### Python ####
```python
vs.IFC_ImportNoUI('D:\Import\Test.ifc')
```

```pascal
IFC_ImportNoUI('file.txt');
```
```python
import vs

# Imports IFC file without showing any dialog.
strFilePath = 'C:/Temp'

vs.IFC_ImportNoUI(strFilePath)
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
