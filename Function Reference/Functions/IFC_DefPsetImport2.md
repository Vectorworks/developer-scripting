# IFC_DefPsetImport2

## Description
Imports Custom Object Presets from XML, XLSX, CSV or text files.
If parameter is empty, Import File dialog is shown to select the desired file.

```pascal
FUNCTION IFC_DefPsetImport2(strFilePath : STRING): BOOLEAN;
```

```python
def vs.IFC_DefPsetImport2(strFilePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strFilePath|STRING|The path to the file. If param is empty, Import File dialog is shown to select the desired file.|

## Examples
```pascal
PROCEDURE PsetImport;
VAR
        bOK : BOOLEAN
BEGIN
        {We suggest that we are importing from an Presets.xml file that is located on D:\Vectorworks\Presets.xml}
	bOK := IFC_DefPsetImport2( 'D:\Vectorworks\Presets.xml');
END;

RUN(PsetImport);
```
#### Python ####
```python
# We suggest that we are importing from an Presets.xml file that is located on D:\Vectorworks\Presets.xml
ok = vs.IFC_DefPsetImport2( 'D:\Vectorworks\Presets.xml');
```

## Version
Availability: from Vectorworks 2023 SP6

## Category
* [IFC](../Categories/IFC.md)
