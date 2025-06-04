# GetCurrentLocalization

## Description
Get the Vectorworks language in the ISO 639-3 draft standard Language ID and sublanguage is unused and will be the empty string reserved for future use for a regional dialect.<BR>
<BR>
Currently this will always return the same language for a given installation of Vectorworks.

```pascal
PROCEDURE GetCurrentLocalization(
				VAR language    : STRING;
				VAR subLanguage : STRING);
```

```python
def vs.GetCurrentLocalization():
    return (language, subLanguage)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|language|STRING|Output parameter. Returns language in ISO 639-3 draft standard Language ID.|
|subLanguage|STRING|Output parameter. Unused. Returns empty string.|

## Version
Availability: from Vectorworks 2010

## Category
* [Utility](../Categories/Utility.md)
