# GISDimStringToMM

## Description
Converts string value that represents dimension real to real number in millimeters.

```pascal
FUNCTION GISDimStringToMM(
				inputStr          : STRING;
				footMarkException : STRING) : REAL;
```

```python

def vs.GISDimStringToMM(inputStr, footMarkException):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inputStr|STRING||
|footMarkException|STRING||

## Examples
```pascal
BEGIN
	GetItemText( dlogID, kProjectElevEdit, projectElevEditText );
	projectElev := GISDimStringToMM( projectElevEditText, GetPluginString (5011) );
END;
```
```python
import vs

# Converts string value that represents dimension real to real number in
# millimeters.
inputStr = 'Example'
footMarkException = 'Example'

value = vs.GISDimStringToMM(inputStr, footMarkException)
vs.Message('GISDimStringToMM returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2024

## Category
* [GIS](../Categories/GIS.md)
