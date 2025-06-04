# CopySymbol

## Description
Procedure CopySymbol will copy a symbol into the active document from a user specified source document. 

If the filename includes a fully qualified path, the path has to use the appropriate notation for the local operating system:
* Macintosh HD:Applications:VectorWorks:Plug-Ins:Data:Notes.txt
* C:Program Files/VectorWorksPlug-Ins/DataNotes.txt

If the filename includes a path relative to the location of the VectorWorks executable, the subfolder delimiters have to be backslashes:
* Plug-Ins\DataNotes.txt

If the filename does not include a path, the file is assumed to exist in the same folder as the VectorWorks executable.

```pascal
FUNCTION CopySymbol(
				filePath : STRING;
				symbol   : STRING): BOOLEAN;
```

```python
def vs.CopySymbol(filePath, symbol):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|File path to document, relative to the application folder.|
|symbol|STRING|Name of symbol to import.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE CopySym;
VAR
	theSymbolName :STRING;
BEGIN
	theSymbolName := 'Fax';
	IF CopySymbol('Object Libraries\Office Equipment.vwx', theSymbolName)  THEN
		Symbol(theSymbolName, 0, 0, 0);
END;
RUN(CopySym);
```
#### Python ####
```python
def CopySym():
	theSymbolName = 'Fax'
	if vs.CopySymbol('Object Libraries\Office Equipment.vwx', theSymbolName): 
		vs.Symbol(theSymbolName, 0, 0, 0)
CopySym()
```

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
