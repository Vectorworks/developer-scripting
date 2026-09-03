# BuildResourceListN2

## Description
Build a resource list from the specified file.

```pascal
FUNCTION BuildResourceListN2(
				type              : INTEGER;
				fullPath          : DYNARRAY[] of CHAR;
				VAR numItems      : LONGINT;
				useDefaultContent : BOOLEAN): LONGINT;
```

```python
def vs.BuildResourceListN2(type, fullPath, useDefaultContent):
    return (LONGINT, numItems)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|type|INTEGER|the type of resource to put in the list|
|fullPath|DYNARRAY[] of CHAR|The path to the file that provides the resources.|
|numItems|LONGINT|the number of items in the list built|
|useDefaultContent|BOOLEAN|determine if the list should contain default content|

## Remarks
*\_c\_*, 2016.02.29:  It supports also posix paths on mac ("/"). It can't be used to retrive the resources in the active document. The useDefaultContent variable doesn't make sense to me: it doesn't seem to make any difference. 

Here some usage examples:
```pascal
resID := 127; { wall styles }
pathID := 113; { Wall ~ Slabs folder }
path := Concat(GetFolderPath(pathID), 'Walls~Slabs Styles Metric.vwx'); { pick a file within the shipped default content }

list := BuildResourceListN2(resID, path, cnt, TRUE); { chosen document }
list := BuildResourceListN2(resID, path, cnt, FALSE); { chosen document again }

list := BuildResourceListN2(resID, GetFPathName, cnt, FALSE); { WARNING: it always returns zero }
```

## Examples
```pascal
BEGIN
	PathFile := Concat(LocImpFile);
	FileResourceListID := BuildResourceListN2(16,PathFile , NumSymbols,TRUE);
		IF NumSymbols <> 0 THEN
			BEGIN
				For Counter := 0 to NumSymbols DO
					BEGIN

FileResourceListID := BuildResourceListN2(16,PathFile , NumSymbols,TRUE);

FileResourceListID := BuildResourceListN2(16,PathFile , NumSymbols,TRUE);
If NumSymbols <> 0 then
	Begin
		For Counter := 0 to NumSymbols-1 DO
			BEGIN
```
```python
import vs

# Build a resource list from the specified file.
type = 0
fullPath = 'C:/Temp'
useDefaultContent = True

resultN, numItems = vs.BuildResourceListN2(type, fullPath, useDefaultContent)
vs.Message('BuildResourceListN2 returned: ' + str((resultN, numItems)))
```

## See Also
VS Functions:
[BuildResourceListN](BuildResourceListN.md) 
| [BuildResourceList](BuildResourceList.md) 
| [BuildResourceList2](BuildResourceList2.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
