# Date

## Description
Function Date returns a formatted date and time string.


{| class="wikitable_c"

|-
| 
{| class="wikitable"
|+ Table - Values for dateFormat parameter
! Date Format
! Constant
|-
| Full Date
| style="text-align:center"| 0
|-
| Abbreviated Date
| style="text-align:center"| 1
|-
| Short Date
| style="text-align:center"| 2
|}

|
{| class="wikitable"
|+ Table - Values for infoFormat parameter:
! Date/Time
! Constant
|-
| Date only
| style="text-align:center"| 0
|-
| Date and Time
| style="text-align:center"| 1
|-
| Time only
| style="text-align:center"| 2
|}
|}

```pascal
FUNCTION Date(
				dateFormat : INTEGER;
				infoFormat : INTEGER): STRING;
```

```python
def vs.Date(dateFormat, infoFormat):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dateFormat|INTEGER|Specify how verbose or compact the resulting string is.|
|infoFormat|INTEGER|Specify if result should contain date, time or both.|

## Remarks
From Vectorlab, 2006:
* Short date always returns MM/DD/YY regardless of your system settings.
* Day and month can return one or two digits, so use the "/" character to parse the values. The year is always 2 digits.
* The hour can also return one or two digits but minutes and seconds always return two digits, so use the ":" character to parse the values.
* the time is a 12-hour clock, not 24-hour. Use the [[VS:Pos| Pos()]] function to detect the AM or PM suffix.

At least on Windows, some of the return values are dependent on the user's operating system date format settings.

From Gideon Scott on the tech board: WinXP &gt; Control Panel &gt; Regional and Language Options &gt; Advanced &gt; Language for non-Unicode programs...

The default setting of "English (United States)" affects the VW date format rather than the date settings under the normal "Regional Options" tab.

## Examples
#### VectorScript ####
```pascal
{ All examples are for the date Friday,  }
{ Nov. 18, 1988 and the time 10:42:24 AM }

Message.(Date(0,1));
{returns Friday, November 18, 1988 10:42:24 AM}

Message.(Date(0,0));
{returns Friday, November 18, 1988}

Message.(Date(2,2));
{returns 10:42:24 AM}

Message.(Date(2,1));
{returns 11/18/88 10:42:24 AM}
```
#### Python ####
```python
#{ All examples are for the date Friday,  }
#{ Nov. 18, 1988 and the time 10:42:24 AM }

vs.Message(vs.Date(0,1))
#{returns Friday, November 18, 1988 10:42:24 AM}

vs.Message(vs.Date(0,0))
#{returns Friday, November 18, 1988}

vs.Message(vs.Date(2,2))
#{returns 10:42:24 AM}

vs.Message(vs.Date(2,1))
#{returns 11/18/88 10:42:24 AM}
```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
