# vsoParamName2Index

## Description
Return the zero-based index of a prameter specified by its universal name. Return -1 if not found.

```pascal
FUNCTION vsoParamName2Index(
				formatName    : STRING;
				paramUnivName : STRING): INTEGER;
```

```python
def vs.vsoParamName2Index(formatName, paramUnivName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|formatName|STRING|   |
|paramUnivName|STRING|   |

## Examples
```pascal
BEGIN
	PrmIdx := 1 + vsoParamName2Index( PIOName, prmName );

PrmIdx := 1 + vsoParamName2Index( PIOName, Concat(prmName, 'X') );
```
```python
import vs

# Return the zero-based index of a prameter specified by its universal name.
formatName = 'MyRecord'
paramUnivName = 'Example'

index = vs.vsoParamName2Index(formatName, paramUnivName)
vs.Message('vsoParamName2Index returned: ' + str(index))
```

## Version
Availability: from Vectorworks 2015

## Category
* [Object Events](../Categories/Object%20Events.md)
