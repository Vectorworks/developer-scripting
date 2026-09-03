# Prot_IsModuleEnabled

## Description
Returns true if the specified module is enabled.

```pascal
FUNCTION Prot_IsModuleEnabled(module : LONGINT): BOOLEAN;
```

```python
def vs.Prot_IsModuleEnabled(module):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|module|LONGINT|   |

## Examples
```pascal
BEGIN
	UprString(which);
	Product := FALSE;
	IF (which = 'VECTORWORKS') & (Prot_IsModuleEnabled(1)) THEN Product := TRUE;
	IF (which = 'RENDERWORKS') 						   	   THEN Product := TRUE;
	IF (which = 'ARCHITECT')   & (Prot_IsModuleEnabled(2)) THEN Product := TRUE;
	IF (which = 'LANDMARK')    & (Prot_IsModuleEnabled(3)) THEN Product := TRUE;
	IF (which = 'SPOTLIGHT')   & (Prot_IsModuleEnabled(5)) THEN Product := TRUE;
```
```python
import vs

# Returns true if the specified module is enabled.
module = 1

ok = vs.Prot_IsModuleEnabled(module)
if ok:
    vs.Message('Prot_IsModuleEnabled succeeded')
else:
    vs.Message('Prot_IsModuleEnabled failed')
```

## Version
Availability: from Vectorworks 2023

## Category
* [Protection](../Categories/Protection.md)
