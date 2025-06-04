# SetCheckoutsComment

## Description
Set the comment that will be used for checkouts and commits.<BR>
<BR>
The Enter Comment dialogs will still be shown when a checkout or commit is done; the dialog will be prepopulated with the comment set with this command.

```pascal
FUNCTION SetCheckoutsComment(comment : STRING): BOOLEAN;
```

```python
def vs.SetCheckoutsComment(comment):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|comment|STRING|The comment to replace any currently in use.|

## See Also
VS Functions:
[GetCheckoutsComment](GetCheckoutsComment.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
