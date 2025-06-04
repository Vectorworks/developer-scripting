# IFC_DefPsetBegin

## Description
Marks the beginning of creation of a new Custom Object Property set (PSet).

```pascal
FUNCTION IFC_DefPsetBegin(psetName : STRING): BOOLEAN;
```

```python
def vs.IFC_DefPsetBegin(psetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|psetName|STRING|The name of the Custom PSet.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	ok	: BOOLEAN;
	psetName: STRING;
	
BEGIN
	psetName:= 'My Custom Pset';

	ok	:= IFC_DefPsetBegin( psetName );
	ok	:= IFC_DefPsetAddMember( psetName, 'Field', 'IfcInteger' );
	ok	:= IFC_DefPsetEnd( psetName );
END;

RUN(Test);
```
==== Python ====
```python
psetName	= "My Custom Pset"

ok	= vs.IFC_DefPsetBegin( psetName )
ok	= vs.IFC_DefPsetAddMember( psetName, "Field", "IfcInteger" )
ok	= vs.IFC_DefPsetEnd( psetName )
```

## See Also
[IFC_DefPsetEnd|IFC_DefPsetEnd](IFC_DefPsetEnd|IFC_DefPsetEnd.md)
[IFC_DefPsetImport|IFC_DefPsetImport](IFC_DefPsetImport|IFC_DefPsetImport.md)

[IFC_DefPsetAddMember|IFC_DefPsetAddMember](IFC_DefPsetAddMember|IFC_DefPsetAddMember.md)

## Version
Availability: from Vectorworks 2016

## Category
* [IFC](../Categories/IFC.md)
