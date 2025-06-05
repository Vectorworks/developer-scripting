# InitXML

## Description
Initializes internal structures. The handle returned is used as the first parameter in all other XML functions. If the value returned is 0, there was an error in initialization.

; Using the XML Library:
The XML Library allows a VectorScript script or SDK plug-in to read and write XML files.  To use the library, a script will first call InitXML to initialize the library.  This function returns a LONGINT which is needed when calling every other XML function.  This value is passed in as the first parameter in all the other XML functions.

To create a new XML file, use [[VS:CreateNewXMLDocument| CreateNewXMLDocument]], or to read an XML file, use [[VS:ReadXMLFile| ReadXMLFile]], which reads the entire file into memory.  Once a document has been either created or read, the various XML functions can be used to set and get elements and attributes; the entire XML document remains in memory during this process.  When all changes have been made, and it is desired to write the XML file out to disk, use [[VS:WriteXMLFile| WriteXMLFile]].  When finished with the library, the function [[VS:ReleaseXML| ReleaseXML]] should be called, to free up internal memory used by the library.

; Notes:
* Elements (or tags), may not contain spaces.
* Element paths must not end with a slash character.


**Table - XML Error Codes**

| Error             | Meaning                        |
|-------------------|-------------------------------|
| 0                 | No error                      |
| -1                | Unknown error                 |
| -2                | Invalid path to XML node (not file path) |
| -3                | Element not found             |
| -4                | Attribute not found           |
| -5                | CDATA section not found       |
| -20               | Memory error                  |
| -21               | Invalid XML handle            |
| -22               | Invalid parameters            |
| -23               | Parser error                  |
| -30               | Index size error              |
| -31               | DOM String size error         |
| -32               | Hierarchy request error       |
| -33               | Wrong document error          |
| -34               | Invalid character error       |
| -35               | No data allowed error         |
| -36               | No modification allowed error |
| -37               | Not found error               |
| -38               | Not supported error           |
| -39               | In use attribute error        |
| -40               | Invalid state error           |
| -41               | Syntax error                  |
| -42               | Invalid modification error    |
| -43               | Namespace error               |
| -44               | Invalid access error          |
| -45               | Validation error              |
| -1000 ~ -2000     | Internal parser error         |

```pascal
FUNCTION InitXML() :LONGINT;
```

```python
def vs.InitXML():
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
||   |   |

## Examples
[XMLParse](examples/XMLParse.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
