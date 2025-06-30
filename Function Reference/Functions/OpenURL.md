# OpenURL

## Description
Opens a web page or file using the default browser or appropriate application (e.g. Adobe Acrobat).  Returns a boolean indicating the success of the operation.

The URL (Uniform Resource Locator) is a pointer to a resource on the World Wide Web.  It specifies both the protocol and location of the document to open.

*For files on the local computer, the URL should begin with <code>file://</code> protocol specifier.
* For web pages, the URL should begin with <code>http://</code>.  The URL should use forward slashes / to separate parts of the path.  

There are some platform differences to be aware of.  Windows will accept either  or / as the path separators.  MacOS X requires that <code>file://</code> URLs begin with <code>/Volumes/</code> before the drive name.  Also, currently the MacOS X implementation of OpenURL does not accept spaces in the URL.  Spaces should be replaced with the escape code <code>%20</code> before calling this function.

Note: The function [GetFolderPath](GetFolderPath.md) returns a string with separators specific for the platform it is running on (/ on Mac and  on Windows).  If your script calls this function to assemble a local <code>file://</code> URL then you will have to replace the : separators with / characters.

```pascal
FUNCTION OpenURL(URLname : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.OpenURL(URLname):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|URLname|DYNARRAY[] of CHAR|The Uniform Resource Locator for the web page or file to open.|

## Remarks
```pascal
PROCEDURE Main;
VAR
  dialogID :INTEGER;
  boo      :BOOLEAN;

  PROCEDURE Dialog_Setup;
  BEGIN
    dialogID := CreateLayout('Sample Dialog', FALSE, '', '');
    CreateControl     (dialogID, 4, 3, '', 25);
    CreatePushButton  (dialogID, 1, 'OK');
    CreatePushButton  (dialogID, 2, 'Cancel');
    CreatePushButton  (dialogID, 3, 'Help');

    SetFirstLayoutItem(dialogID,4);
    SetBelowItem      (dialogID,4,1,0,0);
    SetRightItem      (dialogID,1,2,0,0);
    SetRightItem      (dialogID,2,3,0,0);
  END;

  PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
  BEGIN
    CASE item OF 
      3: boo := OpenURL(Concat(GetFolderPath(1), 'VWHelpHelpLinks.pdf'));
    END;
  END;

BEGIN
  Dialog_Setup;
  IF RunLayoutDialog(dialogID, Dialog_Handler) = 1 then BEGIN
    AlrtDialog('OK');
  END;
END;
RUN(Main);
```


1.) Use forward slash / to separate directories. (Windows accepts  or / as separators. )

2.) Use <code>file:///</code> to begin the URL if it is a file on your local machine.
:<code>theURL := 'file:///C:/Documents and Settings/Jeff/My Documents/Test.htm';</code>

3.) Use <code>http://</code> to begin the URL if the page is hosted by a web server.
:<code>theURL := 'http://www.vectordepot.com';</code>

4.) Tests show that this can also be used with <code>mailto:</code>. Could be a nice way to get feedback from your users...

If you are on MacOS X:

5.) For a file on the boot drive, the path should not contain the name of the drive.
:<code>theURL := 'file:///Documents/Test.html';</code>

6.) For file on other non-boot drive or partition, the path should begin with /Volumes/ followed by the name of the partition.
:<code>theURL := 'file:///Volumes/Xtra2/SomeTest.html';</code>

7.) Spaces are not allowed in the url. Replace them with %20 characters. This is a bug that we should be able to fix in future version. (MacOS 9 and Windows seem to accept spaces.)
:<code>theURL := 'file:///Documents/This%20Is%20A%20Test.html';</code>


```pascal
{--------------------------------------------------------------------}
{ A sample script from Jeff }
{ }
{ This sample VectorScript opens the VectorScript Function Reference }
{ in a web browser.  It gets the full path to the application, }
{ appends it to the partial path for the help file.  The paths are }
{ tweaked so that they will be accepted by the OpenURL call. }
{ Tested on MacOS X 10.3.3, MacOS 9.2.2 and Windows XP with VW 11.}

PROCEDURE OpenURLExample;
VAR
boo :BOOLEAN;
theURL, finalURL : STRING;


{-------------------------}
function RunningOnMacPlatform: BOOLEAN;
var
  appMajor, appMinor, appIncr, platform : INTEGER;

begin
  GetVersion(appMajor, appMinor, appIncr, platform);
  if (platform = 1) then
    RunningOnMacPlatform := true
  else
    RunningOnMacPlatform := false;
end;


{-------------------------}
function RunningOnMacOSX: BOOLEAN;
VAR
  major, minor, incr : LONGINT;
begin
  GetOSVersion(major, minor, incr);
  if (RunningOnMacPlatform = true) and ((major = 0) or (major = 10)) then
    RunningOnMacOSX := true
  else
    RunningOnMacOSX := false;
end;


{-------------------------}
procedure EscapeSpacesURL(theURL :String; VAR destURL : STRING);
var
  spaceIndex : INTEGER;
  locURL : DYNArray[] of CHAR;

begin
  { Replace space characters with %20 }
  locURL := theURL;
  spaceIndex := Pos(' ', locURL);
  while (spaceIndex <> 0) do begin
    locURL[spaceIndex] := '%';
    Insert('20', locURL, spaceIndex + 1);
    spaceIndex := Pos(' ', locURL);
  end;

  destURL := locURL;
end;


{-------------------------}
function GetFolderURL(whichFolder : INTEGER) : STRING;
{ Calls GetFolderPath and then converts path to valid URL string for
each platform. }
var
  appDir : DYNARRAY[] of CHAR;
  sepIndex : INTEGER;
begin
  { Get Path }
  appDir := GetFolderPath(whichFolder);

  { If Mac, replace : with / }
  if (RunningOnMacPlatform = true) then begin
    sepIndex := Pos(':', appDir);
    while (sepIndex <> 0) do begin
      appDir[sepIndex] := '/';
      sepIndex := Pos(':', appDir);
    end;
  end;

  { If MacOS X, prepend /Volumes/ }
  if (RunningOnMacOSX = true) then
    appDir := ConCat('/Volumes/', appDir)   { MacOS X }
  else
    appDir := ConCat('/', appDir);                  { MacOS 9 and Windows }

  { Prepend the file:// specifier }
  appDir := ConCat('file://', appDir);

  GetFolderURL := appDir
end;

{-------------------------}
BEGIN
  theURL := Concat(GetFolderURL(1), 'VWHelp/VectorScript
  Reference/VSFunctionReference.html');

  { Escape the space characters }
  EscapeSpacesURL(theURL, finalURL);

  boo := OpenURL(finalURL);       { OpenURL is actually limited to 256 characters. }
  message(finalURL, ' RESULT IS ', boo);

END;
RUN(OpenURLExample);
```

## Examples
#### VectorScript ####
```pascal
{ Open a webpage. }
status := OpenURL('http://www.vectorworks.net');

{ Open an HTML file on MacOS X. }
status := OpenURL('file:///Volumes/MyMacXHD/Documents/My%20Files/Test.html');

{ Open a PDF file in Acrobat on MacOS X. }
status := OpenURL('file:///Volumes/MyMacXHD/Documents/My%20Files/VSLG11.pdf');

{ Open a PDF file in Acrobat on MacOS 9. }
status := OpenURL('file:///MyMac9HD/My Files/VSLG11.pdf');

{ Open a PDF file in Acrobat on Windows. }
status := OpenURL('file:///C:/My Files/VSLG11.pdf';
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Utility](../Categories/Utility.md)
