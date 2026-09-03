# GetTextSpace

## Description
Procedure GetTextSpace returns the line spacing of the referenced text object.

**Table - Text Spacing**

| Leading        | Constant |
|----------------|----------|
| Single space   | 2        |
| 1 1/2 space    | 3        |
| Double space   | 4        |

```pascal
FUNCTION GetTextSpace(theText : HANDLE): INTEGER;
```

```python
def vs.GetTextSpace(theText):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|

## Examples
```pascal
txtLeading_pt := GetTextLeading (H);
txtSpace := GetTextSpace (H);
txtSize := GetTextSize (H, 1);
{
writeln (' ### Issue Text ### txtLeading_pt = ',txtLeading_pt ,'    txtSpace = ',txtSpace,'    txtSize = ',txtSize );
}

		txtLeading_pt := GetTextLeading (gRevTextH);
		txtSpace := GetTextSpace (gRevTextH);
		txtSize := GetTextSize (gRevTextH, 1);
{
writeln (' *** Revision text *** txtLeading_pt = ',txtLeading_pt ,'    txtSpace = ',txtSpace,'    txtSize = ',txtSize );
}
```
```python
import vs

# Procedure GetTextSpace returns the line spacing of the referenced text object.
theText = 'Example text'

resultN = vs.GetTextSpace(theText)
vs.Message('GetTextSpace returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
