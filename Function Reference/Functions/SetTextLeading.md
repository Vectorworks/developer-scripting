# SetTextLeading

## Description
Procedure SetTextLeading sets the line spacing of the referenced text object to a custom leading value (in points).

```pascal
PROCEDURE SetTextLeading(
				theText : HANDLE;
				leading : REAL);
```

```python
def vs.SetTextLeading(theText, leading):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|leading|REAL|Custom leading value for text.|

## Examples
```pascal
{if the text spacing is not single, 1 1/2, or double spaced	}
{the text leading must be set						}
IF txtSpace = 0 THEN
	SetTextLeading (gIssueNoteTextH, txtLeading_pt);

}
				{if the text spacing is not single, 1 1/2, or double spaced	}
				{the text leading must be set						}
				IF txtSpace = 0 THEN
					SetTextLeading (gRevNoteTextH, txtLeading_pt);
```
```python
import vs

# Procedure SetTextLeading sets the line spacing of the referenced text
# object to a custom leading value (in points).
theText = 'Example text'
leading = 1.0

vs.SetTextLeading(theText, leading)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
