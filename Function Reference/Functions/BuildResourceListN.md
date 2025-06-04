# BuildResourceListN

## Description
Build a resource list from the specified file.

```pascal
FUNCTION BuildResourceListN(
				type         : INTEGER;
				fullPath     : DYNARRAY[] of CHAR;
				VAR numItems : LONGINT): LONGINT;
```

```python
def vs.BuildResourceListN(type, fullPath):
    return (LONGINT, numItems)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|type|INTEGER|the type of resource to put in the list|
|fullPath|DYNARRAY[] of CHAR|The path to the file that provides the resources.|
|numItems|LONGINT|the number of items in the list built|

## Remarks
[[User:CBM-c-|_c_]], (2016.02.29):  It supports also posix paths on mac ("/"). It can't be used to retrive the resources in the active document.

Here some usage examples:
<code lang="vs">
resID := 127; { wall styles }
pathID := 113; { Wall ~ Slabs folder }
path := Concat(GetFolderPath(pathID), 'Walls~Slabs Styles Metric.vwx'); { pick a file within the shipped default content }

list := BuildResourceListN(resID, path, cnt); { chosen document }
list := BuildResourceListN2(resID, GetFPathName, cnt); { WARNING: it always returns zero }
</code>

## See Also
VS Functions:
[BuildResourceList](BuildResourceList.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
