# CreateFolder

## Description
Creates a folder on the hard drive.

```pascal
FUNCTION CreateFolder(path : STRING): BOOLEAN;
```

```python
def vs.CreateFolder(path):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|path|STRING|   |

## Examples
```pascal
	bResult := CreateFolder (Concat(Copy(ActXMLFilePath,1,LenXLMFilePath-1)));
	result := WriteXMLFile(hXML, -1, Concat(ActXMLFilePath,kXMLFileName));
END	{Default File IS PRESENT and contains at least 1 entry}
		ELSE
	IF (OldFldrRes = 0)&((OldBxDataTtl>0)|(OldBmpDataTtl>0)) THEN	{Old File IS PRESENT and contains at least 1 entry}

bResult := CreateFolder (Concat(Copy(ActXMLFilePath,1,LenXLMFilePath-1)));
result := WriteXMLFile(hXML, -1, Concat(ActXMLFilePath,kXMLFileName));
```
```python
import vs

# Creates a folder on the hard drive.
path = 'C:/Temp'

ok = vs.CreateFolder(path)
if ok:
    vs.Message('CreateFolder succeeded')
else:
    vs.Message('CreateFolder failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
