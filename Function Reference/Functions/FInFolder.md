# FInFolder

## Description
Function FInFolder returns a handle to the first object in the referenced symbol folder. The object can be either a symbol definition or a nested symbol folder.
If the folder is empty, the function returns NIL.

```pascal
FUNCTION FInFolder(sfHd : HANDLE): HANDLE;
```

```python
def vs.FInFolder(sfHd):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sfHd|HANDLE|Handle to symbol definition or symbol folder.|

## Remarks
*_c_* (2017.12.25): This since VW 2017 supports all resource folders, not only symbol folders.

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
