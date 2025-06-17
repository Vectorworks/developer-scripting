# GetWallHalfBreakInfo

## Description
Gets the start point, center point and end point of a half break in a wall along the wall line.

```pascal
FUNCTION GetWallHalfBreakInfo(
				wallH                   : HANDLE;
				breakIndex              : INTEGER;
				VAR startPtX,startPtY   : REAL;
				VAR centerPtX,centerPtY : REAL;
				VAR endPtX,endPtY       : REAL): BOOLEAN;
```

```python
def vs.GetWallHalfBreakInfo(wallH, breakIndex):
    return (BOOLEAN, startPt, centerPt, endPt)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallH|HANDLE|   |
|breakIndex|INTEGER|   |
|startPt|REAL|   |
|centerPt|REAL|   |
|endPt|REAL|   |

## Remarks
This currently fails on Round Walls. (VW 13.01+).

The routine parses wall join breaks, not sym breaks. It will return FALSE on:
*start and end of wall: they are always the last two of the break count. Eventual caps do not influence the result.
*inserted symbols/plug-ins: which means you cannot use this routine to (easily) reconstruct the kind of break the inserted symbol or plug-in have.

When the routine returns FALSE the VAR startPt, cenPt and endPt are set to "0,0,0". Mind this.
This routine just serves wall-join analyzing.

An example, which you'll like to run on many walls to see how the routine behaves in different conditions.
It places loci on all break points (a break point has 3 loci: break's start, center and end). The loci take an incremental color index starting 2 (magenta), in order to better distinguish the breaks between each other.

```pascal
PROCEDURE xxxxx;
VAR
wallH : HANDLE;

PROCEDURE LocusAtBreakPoints(wallH: HANDLE);
VAR
startPt, cenPt, endPt : POINT;
i, numWallBreaks: INTEGER;

BEGIN
IF GetNumOfWallBreaks(wallH, numWallBreaks)  THEN BEGIN
message(numWallBreaks);
PushAttrs;

i := 0;
WHILE i &lt; numWallBreaks DO BEGIN
i := i + 1;
PenFore(i+2);

IF GetWallHalfBreakInfo(wallH, i, startPt.x, startPt.y, cenPt.x, cenPt.y, endPt.x, endPt.y) THEN BEGIN
Locus(startPt.x, startPt.y); 
Locus(cenPt.x, cenPt.y); 
Locus(endPt.x, endPt.y); 
END ELSE
AlrtDialog(concat('Skipped break nr: ', i));
END;

PopAttrs;
END;
END;
BEGIN
wallH := FSActLayer;
IF (WallH &lt;&gt; NIL) &amp; ((GetType(wallH) = 68) | (GetType(wallH) = 86)) THEN
LocusAtBreakPoints(wallH)
ELSE
AlrtDialog('Select a wall with some breaks or inserted objects');
END;
Run(xxxxx);
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
