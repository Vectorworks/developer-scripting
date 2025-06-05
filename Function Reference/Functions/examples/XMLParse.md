## VectorScript

```pascal
PROCEDURE Example;
CONST
   userFolder = 15;
   xmlFile = 'VectorWorks Preferences.xml';
   xmlRoot = '/VectorWorksPreferences/General';
VAR
   xmlID :LONGINT;
   value :STRING;
   elementPath :STRING;

PROCEDURE ShowPathAndValue(path :STRING);
BEGIN
   IF GetElementValue(xmlID, path, value) = 0 THEN BEGIN
      AlrtDialog(Concat(path, Chr(13), value));
   END ELSE BEGIN
      AlrtDialog(Concat('Problem in GetElementValue.', Chr(13), 'Path = ', path));
   END;
END;

BEGIN
   xmlID := InitXML;
   IF ReadXMLFile(xmlID, userFolder, xmlFile) = 0 THEN BEGIN
      IF GetFirstChild(xmlID, xmlRoot, elementPath) = 0 THEN BEGIN
         ShowPathAndValue(Concat(xmlRoot, '/', elementPath));
         WHILE GetPreviousElement(xmlID, Concat(xmlRoot, '/', elementPath), elementPath) = 0 DO BEGIN
            ShowPathAndValue(Concat(xmlRoot, '/', elementPath));
         END;
      END ELSE BEGIN
         AlrtDialog('Problem in GetFirstChild');
      END;
   END ELSE BEGIN
      AlrtDialog('Problem in ReadXMLFile');
   END;
   xmlID := ReleaseXML(xmlID);
END;
RUN(Example);
```

## Python

```python
def ShowPathAndValue(path):
	hasErr, value = vs.GetElementValue(xmlID, path)
	if hasErr == 0:
		vs.AlrtDialog(vs.Concat(path, vs.Chr(13), value))
	else:
		vs.AlrtDialog(vs.Concat('Problem in GetElementValue.', vs.Chr(13), 'Path = ', path))

def Example():
	userFolder = 15
	xmlFile = 'VectorWorks Preferences.xml'
	xmlRoot = '/VectorWorksPreferences/General'
	global xmlID
	xmlID = vs.InitXML()
	if vs.ReadXMLFile(xmlID, userFolder, xmlFile) == 0:
		hasErr, elementPath = vs.GetFirstChild(xmlID, xmlRoot)
		if hasErr == 0:
			ShowPathAndValue(vs.Concat(xmlRoot, '/', elementPath))
			hasErr, elementPath = vs.GetPreviousElement(xmlID, vs.Concat(xmlRoot, '/', elementPath))
			while hasErr == 0:
				ShowPathAndValue(vs.Concat(xmlRoot, '/', elementPath))
				hasErr, elementPath = vs.GetPreviousElement(xmlID, vs.Concat(xmlRoot, '/', elementPath))
		else:
			vs.AlrtDialog('Problem in GetFirstChild')
	else:
		vs.AlrtDialog('Problem in ReadXMLFile')

	xmlID = vs.ReleaseXML(xmlID)

xmlID = 0
Example()
```
