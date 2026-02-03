# Rpstr_GetValueStr

## Description
Get a string value from the VectorScript value repository.

```pascal
FUNCTION Rpstr_GetValueStr(
				name         : STRING;
				defaultValue : DYNARRAY[] of CHAR): DYNARRAY[] of CHAR;
```

```python
def vs.Rpstr_GetValueStr(name, defaultValue):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name of the value.|
|defaultValue|DYNARRAY[] of CHAR|Default value if the name does not exist in the VectorScript value repository.|

## Remarks
Here is a sample for when this is  used from the SDK plugin to communicate with a dialog:
```c++
bool CDlgXXX::CreateDialogLayout()
{
	VectorWorks::Scripting::IVectorScriptEnginePtr	vsEngine( VectorWorks::Scripting::IID_VectorScriptEngine );
	if ( vsEngine )
	{
		VWVariant	varParamsList( true );
		vsEngine->Repository_SetValue( "XXX_VarName", varParamsList );
	}

	return this->CreateDialogLayoutFromRsrcAndVWR( kDialogID, DefaultPluginVWRIdentifier() );
}
```

## See Also
VS Functions:
[Rpstr_RemoveValues](Rpstr_RemoveValues.md) 
| [Rpstr_RemoveValue](Rpstr_RemoveValue.md) 
| [Rpstr_GetValueBool](Rpstr_GetValueBool.md) 
| [Rpstr_SetValueBool](Rpstr_SetValueBool.md) 
| [Rpstr_GetValueInt](Rpstr_GetValueInt.md) 
| [Rpstr_SetValueInt](Rpstr_SetValueInt.md) 
| [Rpstr_GetValueReal](Rpstr_GetValueReal.md) 
| [Rpstr_SetValueReal](Rpstr_SetValueReal.md) 
| [Rpstr_GetValueStr](Rpstr_GetValueStr.md) 
| [Rpstr_SetValueStr](Rpstr_SetValueStr.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Utility](../Categories/Utility.md)
