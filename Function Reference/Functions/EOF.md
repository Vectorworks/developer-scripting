# EOF

## Description
Function EOF returns TRUE if the file pointer of an open text file has reached the end of the file (EOF marker). Function EOF is used with Procedures Read and ReadLn to ensure proper file reading and closure. Parameter fileName specifies a text file which is open for reading or writing.


If the filename includes a fully qualified path, the path has to use the appropriate notation for the local operating system:
: <code>Macintosh HD:Applications:VectorWorks:Plug-Ins:Data:Notes.txt</code>
: <code>C:\Program Files\VectorWorks\Plug-Ins\Data\Notes.txt</code>


If the filename includes a path relative to the location of the VectorWorks executable, the subfolder delimiters have to be backslashes:
: <code>Plug-Ins\Data\Notes.txt</code>


If the filename does not include a path, the file is assumed to exist in the same folder as the VectorWorks executable.

```pascal
FUNCTION EOF(fileName : STRING): BOOLEAN;
```

```python
def vs.EOF(fileName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Name of file.|

## Examples
#### VectorScript ####
```pascal
BEGIN
Open('MyData');
WHILE NOT EOF('MyData') DO
ReadLn(a,b,c,d);
Close('MyData');
END;
```
#### Python ####
```python
def Example():
	vs.Open('D:\test.txt')
	while not vs.EOF('D:\test.txt'):
		a,b,c,d = vs.ReadLn()
	vs.Close('D:\test.txt')
	vs.Message(a)

Example()
```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
