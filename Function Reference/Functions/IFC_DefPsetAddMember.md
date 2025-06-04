# IFC_DefPsetAddMember

## Description
Adds a new member to the currently defined Custom Object Preset.

```pascal
FUNCTION IFC_DefPsetAddMember(
				psetName : STRING;
				propName : STRING;
				propType : STRING): BOOLEAN;
```

```python
def vs.IFC_DefPsetAddMember(psetName, propName, propType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|psetName|STRING|The Custom Property Set Name.|
|propName|STRING|Member Name.|
|propType|STRING|Member type.|

## Remarks
The possible values for the member type are 'IfcReal', 'IfcInteger', 'IfcText', 'IfcBoolean'.

## Examples
==== VectorScript ====
```pascal
PROCEDURE PsetAddMember;
VAR
        bOK : BOOLEAN
BEGIN
        {We suggest that 'Chair Details' is a Custom Pset and we want to add 'Height' member with type 'IfcReal'}
	bOK := IFC_DefPsetAddMember( 'Chair Details', 'Height', 'IfcReal');
END;

RUN(PsetAddMember);
```
==== Python ====
```python
# We suggest that 'Chair Details' is a Custom Pset and we want to add 'Height' member with type 'IfcReal'
ok = vs.IFC_DefPsetAddMember( 'Chair Details', 'Height', 'IfcReal');
```

## See Also
[IFC_DefPsetBegin|IFC_DefPsetBegin](IFC_DefPsetBegin|IFC_DefPsetBegin.md)
[IFC_DefPsetEnd|IFC_DefPsetEnd](IFC_DefPsetEnd|IFC_DefPsetEnd.md)

[IFC_DefPsetImport|IFC_DefPsetImport](IFC_DefPsetImport|IFC_DefPsetImport.md)

## Version
Availability: from Vectorworks 2016.

## Category
* [IFC](../Categories/IFC.md)
