# Name2Index

## Description
Function Name2Index returns the internal index number for the specified object.

```pascal
FUNCTION Name2Index(name : STRING): LONGINT;
```

```python
def vs.Name2Index(name):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of object.|

## Remarks
Returns the internal index for the object associated with the specified name.

(Joel Sciamma 2006.08.11): If the name does not exist, Name2Index returns zero.

## Examples
#### VectorScript ####
```pascal
NameIndex := Name2Index('objectName');
```
#### Python ####
```python

```

```pascal
BEGIN
	IF IsTextureableObject(hobj) THEN BEGIN
		IF Name2Index(ClassName) = 0 THEN BEGIN
			activeClName:= ActiveClass;
			NameClass(ClassName);
			NameClass(activeClName);
		END;

BEGIN
	GetActualClassID := Name2Index( cppdIn.strClassActualName );
END;

localarchMaterialNameID		:= GetRField (gPluginH, gPluginName, 'ArchCompMaterialID');
localstructMaterialNameID	:= GetRField (gPluginH, gPluginName, 'StructCompMaterialID');
archMaterialIDNum			:= Name2Index(localarchMaterialNameID);
structMaterialIDNum			:= Name2Index(localstructMaterialNameID);
```
```python
result = vs.Name2Index('Example')
```

## See Also
VS Functions:
[SetSkylight](SetSkylight.md) 
| [CreateSkylight](CreateSkylight.md) 
| [AddCavity](AddCavity.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Object Names](../Categories/Object%20Names.md)
