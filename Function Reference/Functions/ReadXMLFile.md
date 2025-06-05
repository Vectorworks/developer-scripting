# ReadXMLFile

## Description
Reads an XML file.  The entire file is read in, and parsed.  Once this has been done, the calling application can then use the following accessor functions to retrieve and modify the data within that file.  whichPath is the directory specifier; if whichPath is -1, the filename is taken by itself, without prepending a directory onto it.

```pascal
FUNCTION ReadXMLFile(
				XMLHandle : LONGINT;
				whichPath : INTEGER;
				filename  : STRING):INTEGER;
```

```python
def vs.ReadXMLFile(XMLHandle, whichPath, filename):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|whichPath|INTEGER|   |
|filename|STRING|   |

## Remarks
[[User:CBM-c-|_c_]] (2016.06.16): Requires a HSF path (with colon) on Mac.

## Examples
[XMLParse](examples/XMLParse.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
