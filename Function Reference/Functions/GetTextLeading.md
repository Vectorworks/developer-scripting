# GetTextLeading

## Description
Procedure GetTextLeading returns the custom leading value(in points) of the referenced text object.

```pascal
FUNCTION GetTextLeading(theText : HANDLE): REAL;
```

```python
def vs.GetTextLeading(theText):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|

## Remarks
If a custom value was not set, this returns -1.0.

## Examples
```pascal
txtLeading_pt := GetTextLeading (H);
txtSpace := GetTextSpace (H);
txtSize := GetTextSize (H, 1);
{
writeln (' ### Issue Text ### txtLeading_pt = ',txtLeading_pt ,'    txtSpace = ',txtSpace,'    txtSize = ',txtSize );

		txtLeading_pt := GetTextLeading (gRevTextH);
		txtSpace := GetTextSpace (gRevTextH);
		txtSize := GetTextSize (gRevTextH, 1);
{
writeln (' *** Revision text *** txtLeading_pt = ',txtLeading_pt ,'    txtSpace = ',txtSpace,'    txtSize = ',txtSize );
```
```python
import vs

# Procedure GetTextLeading returns the custom leading value(in points) of the
# referenced text object.
theText = 'Example text'

value = vs.GetTextLeading(theText)
vs.Message('GetTextLeading returned: ' + str(value))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
