# vsoGetCatalogPath

## Description
Get the folder specifier and options path for an object catalog

```pascal
PROCEDURE vsoGetCatalogPath(
				folderSpec   : INTEGER;
				relativePath : STRING);
```

```python
def vs.vsoGetCatalogPath(folderSpec, relativePath):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|folderSpec|INTEGER|   |
|relativePath|STRING|   |

## Examples
```pascal
vsoGetCatalogPath(1, 'file.txt');
```
```python
import vs

# Get the folder specifier and options path for an object catalog.
folderSpec = 1
relativePath = 'C:/Temp'

vs.vsoGetCatalogPath(folderSpec, relativePath)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Object Events](../Categories/Object%20Events.md)
