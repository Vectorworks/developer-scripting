# IFC_ImportLibrary

## Description
Imports IFC Library of objects.

```pascal
FUNCTION IFC_ImportLibrary(
				strFilePath    : STRING;
				bKeepHierarchy : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_ImportLibrary(strFilePath, bKeepHierarchy):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strFilePath|STRING|Path to the Folder with IFC files|
|bKeepHierarchy|BOOLEAN|Boolean that determines whether the hierarchy of the library is preserved in the Symbol Folder hierarchy.|

## Remarks
This function is used when importing more than one IFC files simultaneously.

Please note that a Symbol Folder in the Resource Manager is created and every file is imported as a separate symbol. If the main folder contains a hierarchy of folders with more IFC files, the hierarchy can be conveyed in the Symbol Folder by setting bKeepHierarchy boolean to TRUE.

## Examples
==== VectorScript ====
```pascal
PROCEDURE ImportLibrary;
VAR
        bKeepHierarchy : BOOLEAN
        bOK            : BOOLEAN
        strFilePath    : STRING
BEGIN
        {We suggest that the path to the library that contains the IFC files is "D:\Files\IFCLibrary"}
        bKeepHierarchy := TRUE;
        strFilePath    := "D:\Files\IFCLibrary";
	bOK            := IFC_ImportLibrary( strFilePath, bKeepHierarchy );
END;

RUN(ImportLibrary);
```
==== Python ====
```python
# We suggest that the path to the library that contains the IFC files is "D:\Files\IFCLibrary"
ok = vs.IFC_ImportLibrary( "D:\Files\IFCLibrary", True );
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
