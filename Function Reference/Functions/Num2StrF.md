# Num2StrF

## Description
Function Num2StrF converts a specified REAL value into a string. The numeric value will be converted and displayed in the current unit settings of the drawing.

```pascal
FUNCTION Num2StrF(vDistance : REAL): STRING;
```

```python
def vs.Num2StrF(vDistance):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|vDistance|REAL|Numeric value.|

## Remarks
IMPORTANT NOTE: whether or not you get unit marks appended to the returned string value depends on a user-accessible Show Marks setting in the Units dialog box (CMP). Also you get fractions instead of decimals if that's how the user has set up her units... now this may be all very well but what if you are trying to use this to convert a ratio expressed as a REAL to a string in order to poke it into a parameter value?

This appears not to work as advertised. The string value returned appears to be in inches no matter the unit settings of the document.

## Examples
#### VectorScript ####
```pascal
oldnumValue:=23.45;
newStrValue:=Num2StrF(oldnumValue);
{would return 1'-11 1/2"}
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
