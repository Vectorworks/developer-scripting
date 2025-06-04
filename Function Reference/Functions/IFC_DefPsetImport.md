# IFC_DefPsetImport

## Description
Imports Custom Object Presets from XML, XLSX, CSV or text files from folder.
If parameter is empty, Import Folder dialog is shown to select the desired folder.

```pascal
FUNCTION IFC_DefPsetImport(strFolderPath : STRING): BOOLEAN;
```

```python
def vs.IFC_DefPsetImport(strFolderPath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strFolderPath|STRING|The path to the folder. If param is empty, Import Folder dialog is shown to select the desired folder.|

## Examples
```pascal
PROCEDURE PsetImport;
VAR
        bOK : BOOLEAN
BEGIN
        {We suggest that we are importing from an Presets.xml file that is located on D:\Vectorworks\Presets.xml}
	bOK := IFC_DefPsetImport( 'D:\Vectorworks');
END;

RUN(PsetImport);
```
#### Python ####
```python
# We suggest that we are importing from an Presets.xml file that is located on D:\Vectorworks\Presets.xml
ok = vs.IFC_DefPsetImport( 'D:\Vectorworks');
```

## See Also
[IFC_DefPsetBegin|IFC_DefPsetBegin](IFC_DefPsetBegin|IFC_DefPsetBegin.md)
[IFC_DefPsetEnd|IFC_DefPsetEnd](IFC_DefPsetEnd|IFC_DefPsetEnd.md)

[IFC_DefPsetAddMember|IFC_DefPsetAddMember](IFC_DefPsetAddMember|IFC_DefPsetAddMember.md)

## Version
Availability: from Vectorworks 2016

## Category
* [IFC](../Categories/IFC.md)
