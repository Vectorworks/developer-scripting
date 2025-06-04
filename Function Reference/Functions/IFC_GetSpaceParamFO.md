# IFC_GetSpaceParamFO

## Description
Gets the space type, name or number of the Space object.

```pascal
FUNCTION IFC_GetSpaceParamFO(
				hSpace           : HANDLE;
				inStrParam       : STRING;
				VAR outStrResult : STRING): BOOLEAN;
```

```python
def vs.IFC_GetSpaceParamFO(hSpace, inStrParam):
    return (BOOLEAN, outStrResult)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSpace|HANDLE|Handle to the Space object.|
|inStrParam|STRING|The Space param value. "1" for Space Type. "2" for Space Name. "3" for Space Number.|
|outStrResult|STRING|The result.|

## Examples
To use the sample you need to have a selected Space object on the drawing.

==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	hSpace	: HANDLE;
	ok	: BOOLEAN;
	res	: STRING;
	
BEGIN
	hSpace	:= FSObject( FLayer );
	if ( hSpace <> nil ) then
	begin
		{We suggest the handle is a handle to Space object.}
		{Additional verification could be done.}
		
		{Get the Space Type}
		ok	:= IFC_GetSpaceParamFO( hSpace, '1', res );

		{Get the Space Name}
		ok	:= IFC_GetSpaceParamFO( hSpace, '2', res );
		
		{Get the Space number}
		ok	:= IFC_GetSpaceParamFO( hSpace, '3', res );
	end;
END;

RUN(Test);
```
==== Python ====
```python
hSpace	= vs.FSObject( vs.FLayer() )
if hSpace != vs.Handle(0):
	# We suggest the handle is a handle to Space object.
	# Additional verification could be done.
		
	res	= ''
	
	# Get the Space Type
	ok	= vs.IFC_GetSpaceParamFO( hSpace, '1', res )

	# Get the Space Name
	ok	= vs.IFC_GetSpaceParamFO( hSpace, '2', res )
		
	# Get the Space number
	ok	= vs.IFC_GetSpaceParamFO( hSpace, '3', res )
```

## Version
Availability: from Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
