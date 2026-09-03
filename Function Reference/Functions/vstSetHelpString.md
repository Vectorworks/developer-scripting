# vstSetHelpString

## Description
Places helpMessage in the mode bar to the right of any other mode objects.

```pascal
PROCEDURE vstSetHelpString(inHelpStr : STRING);
```

```python
def vs.vstSetHelpString(inHelpStr):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inHelpStr|STRING|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
   vstSetHelpString('Test Message');
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
BEGIN
	TempToolCallback := 0;
	CASE action OF
	3: vstSetHelpString(GetPluginString(3010));
	103:
		BEGIN
		If Is3dView then
			Begin

BEGIN
	TwoPointsToolCallback := 0;
	CASE action OF
	3: begin {initial tool setup}
			vstSetHelpString(pick2points);
			vstSetPtBehavior (2);
	   end;
```
```python
vs.vstSetHelpString('Example')
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
