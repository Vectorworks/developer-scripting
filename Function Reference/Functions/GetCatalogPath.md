# GetCatalogPath

## Description
Get the path to catalog files for a plug-in object.

```pascal
FUNCTION GetCatalogPath(
				inhObject           : HANDLE;
				VAR outFolderSpec   : INTEGER;
				VAR outRelativePath : STRING): BOOLEAN;
```

```python
def vs.GetCatalogPath(inhObject):
    return (BOOLEAN, outFolderSpec, outRelativePath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inhObject|HANDLE|Handle of parametric object.|
|outFolderSpec|INTEGER|Returns the Folder Specificer of the catalogs.|
|outRelativePath|STRING|Returns the relative path to the folder specficier. May be empty.|

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
