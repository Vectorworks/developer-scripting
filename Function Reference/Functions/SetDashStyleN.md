# SetDashStyleN

## Description
Procedure SetDashStyleN creates a new linestyle in a Vectorworks document. Parameter name defines the name of the linestyle, parameter swt defines whether the linestyle will be scaled with thickness, and parameter numPairs specifies the number of length pairs defining the linestyle.

The linestyle is defined by up to five black/white length pairs, which are specified in parameters pair1 through pair5. The minimum length of any given black or white parameter is 1 point, or 1/72 of an inch, and the line specification must be in pairs.

```pascal
PROCEDURE SetDashStyleN(
				name     : STRING;
				swt      : BOOLEAN;
				numPairs : INTEGER;
				pair1    : REAL;
				pair2    : REAL;
				pair3    : REAL;
				pair4    : REAL;
				pair5    : REAL);
```

```python
def vs.SetDashStyleN(name, swt, numPairs, pair1, pair2, pair3, pair4, pair5):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|   |
|swt|BOOLEAN|   |
|numPairs|INTEGER|   |
|pair1|REAL|   |
|pair2|REAL|   |
|pair3|REAL|   |
|pair4|REAL|   |
|pair5|REAL|   |

## Remarks
[[User:CBM-c-|_c_]], (2014.04.08):  It creates a named dash style definition. This sets the name in both the name list and the (now) hidden dash style list. The parameter numPairs seems to be automatically filled depending on the count of pair values passed (you can omit pairs, if they are not needed). In the example below it works with "0" whereby you'd think that "2" would be needed, since two dash-gap pairs are passed. The routine supports up to 10 real dash-gap values (5 pairs). The values must be entered in page inches. More comments on Vectorlab's [http://www.vectorlab.info/index.php?title=Index_pitfalls Index_pitfalls].

The routine can be expressed as follows, whereby you'll only enter as many dashX-gapX values as needed:
<code lang="pas">SetDashStyleN(name: STRING; scalesWithThickness: BOOLEAN; numPairs: INTEGER; dash1, gap1, dash2, gap2, dash3, gap3, dash4, gap4, dash5, gap5: REAL);</code>

## Examples
```pascal
SetDashStyle('My Dash Style', True, 0, 1", 1/4", 1/4", 1/4");
```

## Version
Availability: from Vectorworks 2010

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
