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
*_c_*, 2016.02.29:  It supports also posix paths on mac ("/"). It can't be used to retrive the resources in the active document. The useDefaultContent variable doesn't make sense to me: it doesn't seem to make any difference. 

Here some usage examples:
<code lang="vs">
resID := 127; { wall styles }
pathID := 113; { Wall ~ Slabs folder }
path := Concat(GetFolderPath(pathID), 'Walls~Slabs Styles Metric.vwx'); { pick a file within the shipped default content }

list := BuildResourceListN2(resID, path, cnt, TRUE); { chosen document }
list := BuildResourceListN2(resID, path, cnt, FALSE); { chosen document again }

list := BuildResourceListN2(resID, GetFPathName, cnt, FALSE); { WARNING: it always returns zero }
</code>

## See Also
VS Functions:
[BuildResourceListN](BuildResourceListN.md) 
| [BuildResourceList](BuildResourceList.md) 
| [BuildResourceList2](BuildResourceList2.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
