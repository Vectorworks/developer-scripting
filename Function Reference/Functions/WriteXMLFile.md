# WriteXMLFile

## Description
Writes an XML file. whichPath is the directory specifier; it accepts the same values as GetFolderPath. If whichPath is -1, the filename is taken by itself, without prepending a directory onto it.

```pascal
FUNCTION WriteXMLFile(
				XMLHandle : LONGINT;
				whichPath : INTEGER;
				filename  : STRING):INTEGER;
```

```python
def vs.WriteXMLFile(XMLHandle, whichPath, filename):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|whichPath|INTEGER|   |
|filename|STRING|   |

## Remarks
Looks like the whichPath argument no longer supports 1 or 12. The other indexes should still work.

For example, this does not work:

```pascal
xmlFileName := 'XML Test File.xml';
result := WriteXMLFile(hXML, 12, xmlFileName);
```

But this does:

```pascal
xmlFileName := Concat(GetFolderPath(12), 'XML Test File.xml');
result := WriteXMLFile(hXML, -1, xmlFileName);
```

Result Values:
```pascal
No Error = 0;
Unknown Error = -1;
Invalid Path Error = -2;
Element Not Found Error	= -3;
Attribute Not FoundError = -4;
CDATA Section Not Found Error = -5;
Memory Error = -20;
Invalid XML Handle Error = -21;
Invalid Parameters Error = -22;
Parser Error = -23;
No Child Or Sibling Nodes = -24;
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE WriteXML;
{Writes data to an XML file.}

CONST
   kAppFolder = 1;

VAR
   hXML            :LONGINT;
   xmlFile         :STRING;
   result          :INTEGER;
   elementResult   :STRING;
   attributeResult :STRING;
   pathResult      :STRING;
   cdata           :DYNARRAY [] of CHAR;

BEGIN
   ALLOCATE  cdata [1..1024];
   cdata := Copy('00 01 02 03 04 05 06 07', 1, 23);
   cdata := Concat(cdata, Chr(13), '08 09 10 1a 1b 1c 1d 1e');
   cdata := Concat(cdata, Chr(13), '1f 20 21 22 23 24 25 26');

   hXML := InitXML;

   IF hXML <> 0 THEN BEGIN
      xmlFile := 'XML Test File.xml';
      result := CreateNewXMLDocument(hXML, 'XMLTest');

      result := SetElementValue  (hXML, '/XMLTest/Tools/Computers/Platform/Macintosh/CPU', 'G4');
      result := SetElementValue  (hXML, '/XMLTest/Tools/Computers/Platform/Macintosh/Disk', 'SCSI');
      result := SetElementValue  (hXML, '/XMLTest/Tools/Computers/Platform/Windows/CPU', 'P4');
      result := SetElementValue  (hXML, '/XMLTest/Tools/Computers/Platform/Windows/Disk', 'EIDE');

      result := SetAttributeValue(hXML, '/XMLTest/Tools/Computers/Platform/Windows/CPU', 'Speed', '3.0 GHz');
      result := SetAttributeValue(hXML, '/XMLTest/Tools/Computers/Platform/Macintosh/CPU', 'Speed', '1.2 GHz');

      result := SetAttributeValue(hXML, '/XMLTest/Tools/Computers/Platform/Windows/Disk', 'Size', '300 GB');
      result := SetAttributeValue(hXML, '/XMLTest/Tools/Computers/Platform/Macintosh/Disk', 'Size', '450 GB');

      result := SetAttributeValue(hXML, '/XMLTest/Tools/Hardware/Screwdriver/Regular', 'Head', 'Flat');
      result := SetAttributeValue(hXML, '/XMLTest/Tools/Hardware/Screwdriver/Philips', 'Head', '4-point');
      result := SetElementValue  (hXML, '/XMLTest/Tools/Hardware/Wrench/Fixed/Units/Metric', 'mm');
      result := SetElementValue  (hXML, '/XMLTest/Tools/Hardware/Wrench/Fixed/Units/English', 'inches');
      result := SetAttributeValue(hXML, '/XMLTest/Tools/Hardware/Wrench/Non-fixed/Adjustable', 'slide', 'Horizontal');
      result := SetAttributeValue(hXML, '/XMLTest/Tools/Hardware/Wrench/Non-fixed/Monkey', 'slide', 'Vertical');

      {Write some CDATA strings}
      result := SetCDATA(hXML, '/XMLTest/Tools/BinaryData/MiscData', cdata);
      
      result := WriteXMLFile(hXML, kAppFolder, xmlFile);
      Message('result: ', result);
      result := ReleaseXML(hXML);
   END ELSE BEGIN
      SysBeep;
      Message('Could not initialize XML reader.');
   END;
END;
Run(WriteXML);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
