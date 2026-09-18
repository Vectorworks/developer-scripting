# OLDForceStrToReal

## Description
Converts force string to real number and returns the result.

```pascal
FUNCTION OLDForceStrToReal(
				forceString   : STRING;
				VAR realValue : REAL): BOOLEAN;
```

```python
def vs.OLDForceStrToReal(forceString):
    return (BOOLEAN, realValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|forceString|STRING|   |
|realValue|REAL|   |

## Examples
```pascal
BEGIN
	ParamValueStr := GetRField( HoistHdl, PIOName, 'ReactionForceStr' );
	IF OLDForceStrToReal( ParamValueStr, ParamValueReal ) THEN
	BEGIN
		SetRField( HoistHdl, PIOName, 'ReactionForce', Num2Str( 9, ParamValueReal ) );
	END;

BEGIN
	FieldHolder := 'LoadWtReal';
	FieldVal := Num2Str( 9, realVal );
END;
IF (FieldHolder = 'ReactionForceStr') & OLDForceStrToReal( FieldVal, realVal ) THEN
BEGIN
	FieldHolder := 'ReactionForce';
	FieldVal := Num2Str( 9, realVal );
END;
```
```python
import vs

# Converts force string to real number and returns the result.
forceString = 'Example'

ok, realValue = vs.OLDForceStrToReal(forceString)
vs.Message('OLDForceStrToReal returned: ' + str((ok, realValue)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
