# SetSymbolOptionsN

## Description
Sets the default class, insert  options, and break options for the specified symbol. 

* Table - Symbol Insertion Options

| Category | Description | Constant Value |
|----------|-------------|----------------|
| Insertion Mode | Insert on Center Line | 0 |
| Insertion Mode | Insert on Edge | 1 |
| Break Mode | Full Break with Caps | 1 |
| Break Mode | Full Break No Caps | 2 |
| Break Mode | Half Break | 3 |
| Break Mode | No Break | 4 |

```pascal
PROCEDURE SetSymbolOptionsN(
				name       : STRING;
				insertMode : INTEGER;
				breakMode  : INTEGER;
				className  : STRING);
```

```python
def vs.SetSymbolOptionsN(name, insertMode, breakMode, className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of symbol.|
|insertMode|INTEGER|Insertion mode of symbol.|
|breakMode|INTEGER|Break mode for symbol.|
|className|STRING|Default class for symbol.|

## Remarks
Sets the insert and break options for the master symbol named &lt;name&gt;. 

The insertMode options are:
0 = insert on the center line of the wall
1 = insert on the edge of the wall

The breakMode options are:
1 = Full break with caps, both edges of the wall are broken and cap lines close off the two broken portions of the wall.
2 = Full break with no caps, both edges of the wall  are broken and there are no cap lines.
3 = Half break, for edge insertions only, wall edge is broken on the same edge that the symbol is inserted on.
4 = No break, there is no break in the wall, the symbol is drawn on top of the wall.

See also Get SymbolOptions

[sd 8/18/98]

The className should specify the name of a class that exists in the parent document. After a class is set, all instances of this symbol will be marked as members of the class.

## Version
Availability: from VectorWorks 8.5

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
