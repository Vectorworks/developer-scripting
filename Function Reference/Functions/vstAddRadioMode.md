# vstAddRadioMode

## Description
Adds a group of radio buttons to the mode bar. <ul>
<li>inNumButtons is the number of buttons <= 6</li>
<li>id# is the &#039;ICN#&#039; resource ID of the button&#039;s icon.</li>
<li>initialSetting is the number, left to right, of the button originally highlighted. </li>
</ul>

Rsrc IDs must be greater than 10000.

(Seems like this has been replaced by [AddRadioMode](AddRadioMode.md))

```pascal
PROCEDURE vstAddRadioMode(
				inInitialSetting : INTEGER;
				inNumButtons     : INTEGER;
				inRsrcID_1       : INTEGER;
				inRsrcID_2       : INTEGER;
				inRsrcID_3       : INTEGER;
				inRsrcID_4       : INTEGER;
				inRsrcID_5       : INTEGER;
				inRsrcID_6       : INTEGER);
```

```python
def vs.vstAddRadioMode(inInitialSetting, inNumButtons, inImageSpecification1, inImageSpecification2, inImageSpecification3, inImageSpecification4, inImageSpecification5, inImageSpecification6):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inInitialSetting|INTEGER|   |
|inNumButtons|INTEGER|   |
|inRsrcID_1|INTEGER|   |
|inRsrcID_2|INTEGER|   |
|inRsrcID_3|INTEGER|   |
|inRsrcID_4|INTEGER|   |
|inRsrcID_5|INTEGER|   |
|inRsrcID_6|INTEGER|   |

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
