# Field

## Description
<b>Obsolete. Use [ SetRField](SetRField.md) for new scripts.</b>

```pascal
PROCEDURE Field(
				h  : HANDLE;
				s1 : STRING;
				s2 : STRING;
				s3 : STRING);
```

```python
def vs.Field(h, s1, s2, s3):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|s1|STRING|   |
|s2|STRING|   |
|s3|STRING|   |

## Remarks
Obsolete function maintained for compatibility with old scripts. Use [ SetRField](SetRField.md) for new scripts.

[sd 9/14/98] Update the RecordNode attached to object "h" by setting the field "s2" of format "s1" to the value "s3".  The object is not redrawn immediately, so don't call this for a symbol which uses the "link text to record" feature.

## See Also
VS Functions:
[SetRField](SetRField.md)

## Version
Availability: from All Versions. Obsolete from VW 9.

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
