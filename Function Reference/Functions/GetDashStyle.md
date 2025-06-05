# GetDashStyle

## Description
Function GetDashStyle searches for the pattern specified by the parameters. If it exists, then the linestyle index associated with the existing dash pattern is returned. If it does not exist, then it is added to the document and the linestyle index associated with the new dash pattern is returned. The current document default linestyle will be set to the index of the dash pattern.

```pascal
FUNCTION GetDashStyle(
				swt      : BOOLEAN;
				numPairs : INTEGER;
				pair1    : REAL;
				pair2    : REAL;
				pair3    : REAL;
				pair4    : REAL;
				pair5    : REAL): INTEGER;
```

```python
def vs.GetDashStyle(swt, numPairs, pair1, pair2, pair3, pair4, pair5):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|swt|BOOLEAN|scales with thickness|
|numPairs|INTEGER|count of used pairs|
|pair1|REAL|   |
|pair2|REAL|   |
|pair3|REAL|   |
|pair4|REAL|   |
|pair5|REAL|   |

## Remarks
*_c_*, (2016.03.01):  The dash style index returned is relative to the dash style list, so it's not an index that can be used with [Index2Name](Index2Name.md). The values must be page inches. This routine seems to be the same as [GetDashStyleIndex](GetDashStyleIndex.md), but it also sets the found/created style to active. More comments on Vectorlab's [http://www.vectorlab.info/index.php?title=Index_pitfalls Index_pitfalls].
<code lang="vs">
GetDashStyle(scalesWithThickness: BOOLEAN; numPairs: INTEGER; dash1, gap1, dash2, gap2, dash3, gap3, dash4, gap4, dash5, gap5: REAL): INTEGER; 

indx := GetDashStyle(TRUE, 1, 0.12, 0.03); 
{ returns the dash style index of 'ISO-02 Dashed' or creates a style in the document with these values }
</code>

Parameter swt defines whether the linestyle will be scaled with thickness, and parameter numPairs specifies the number of length pairs (2-10) defining the linestyle. 
The linestyle is defined by up to five black/white length pairs, which are specified in parameters pair1 through pair5. The minimum length of any given black or white parameter is 1 point, or 1/72 of an inch, and the line specification must be in pairs.  
The Function will also set the document default line style.

## Examples
#### VectorScript ####
```pascal
currLS:=GetDashStyle;
```
#### Python ####
```python
vs.GetDashStyle(True, 1, 1)
```

## Version
Availability: from MiniCAD 5.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
