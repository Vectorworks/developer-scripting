## Search Criteria Format

### Syntax

Filterkriterien in Skripten bestehen aus zwei Teilen: dem Suchattribut-Typ und dem Suchwert. Der Suchattribut-Typ gibt an, welches Attribut zum Filtern von Objekten im Dokument verwendet wird; der Suchwert gibt den Wert an, der durch den Filtervorgang gefunden und abgeglichen werden soll. So gibt z. B. der Filterkriterien-Ausdruck

```pascal
(C=’Wand’)
```

an, dass nach allen Objekten gesucht werden soll, deren Klasse Wand ist. Im Filterkriterien-Ausdruck gibt der Attributtyp C an, dass die Suche nach dem Klassenattribut von Objekten im Dokument durchgeführt werden soll. Der Suchwert Wand gibt an, welche Klasse beim Filtern als übereinstimmend gewertet wird.

Die allgemeine Syntax für Filterkriterien-Ausdrücke lautet:

```pascal
(<Suchattribut Type> = <Suchwert>)
```

Klammern werden üblicherweise verwendet, um einzelne Filter-Ausdrücke einzuschließen und zu kennzeichnen; sie sind nicht erforderlich.

### Mehrfache Filterkriterien

Es können mehrere Kriterien angegeben werden, um den Suchvorgang auf eine spezifischere Untergruppe von Objekten einzuschränken. Mehrere Filterkriterien werden mit dem Operator & erstellt, um einzelne Filterkriterien zu verketten. Im Ausdruck


```pascal
((L='Neue Bebauung') & (C='Phase 1'))
```

werden zwei Suchbegriffe kombiniert, um nach einer bestimmten Gruppe von Objekten zu filtern, in diesem Fall nach allen Objekten auf der Ebene Neue Bebauung, deren Klasse Phase 1 ist. Um die Suche noch weiter einzugrenzen, fügen Sie einfach weitere Suchbegriffe hinzu:

```pascal
((L='Neue Bebauung') & (C='Phase 1') & (SEL=TRUE))
```

Im Beispiel wurde der Attributtyp "Aktivierungsstatus" hinzugefügt, so dass jetzt nur aktivierte Objekte der Klasse "Phase 1" auf der Ebene "Neue Bebauung" der Suche entsprechen.

### Mehrfache Suchwerte

Es ist auch möglich, anhand von Filterkriterien nach mehreren übereinstimmenden Werten zu filtern. Mehrere übereinstimmende Werte verwenden die folgende Syntax:

```pascal
(<Attribut Type> IN [<Suchwert>,<Suchwert>,...])
```

Wenn ein Suchbegriff auf diese Weise angegeben wird, werden Objekte, die mit einem beliebigen Wert in der durch Komma getrennten Werteliste übereinstimmen, in die Liste der Objekte aufgenommen, die der Suche entsprechen. Zum Beispiel:

```pascal
(R IN ['Bauteildaten','Baugruppendaten','Montagedaten'])
```

Eine Suche mit dem oben gezeigten Filterkriterien-Ausdruck führt zu allen Objekten mit einer verknüpften Datenbank, der mit einer der Datenbanken in der Suchliste übereinstimmen.

## Attribut-Typen

Diese Standard-Attribut-Typen sind für die Verwendung in Suchbegriffen verfügbar.

| Attribut | Tastenkürzel | Beschreibung | Bemerkungen |
|-----------|----------|-------------|-------|
| All objects | (ALL) | This specifier will search for all objects in the document. | |
| Descend into plug‐in objects | (INOBJECT) | This traversal specifier instructs the search to look inside plug-in object containers. | |
| Descend into viewport annotations | (INVIEWPORT) | This traversal specifier instructs the search to look inside viewport annotations. | |
| Do not descend into referenced design layer viewports | (NOTINREFDLVP) | This traversal specifier instructs the search to ignore the content of referenced design layer viewports. | |
| Do not descend into non-referenced design layer viewports | (NOTINDLVP) | This traversal specifier instructs the search to ignore the content of non-referenced design layer viewports. | |
| Attached Record | (R) | The record attribute specifier will search for objects that have the indicated record attached. The record attribute specifier requires the use of the multiple criteria format to specify the record name. For example, to search for objects having the Part Data record attached, the search term would be: ```pascal (R IN ['Part Data']) ``` The record name must be a literal *STRING* value. | |
| Class | (C) | The class attribute type will search for objects assigned to the specified class. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Layer | (L) | The layer attribute type will search for objects on the specified layer. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Object Type | (T) | The object type attribute specifier will search for objects that match the specified object type. The search value must be one of the predefined object type selectors (see table at the end of this section for a complete listing). | |
| Story | (STO) | (Design Series required) The story attribute specifier will search for objects on the specified layer. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Object Name | (N) | The object name attribute specifier will search for the object which is assigned the specified object name. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Symbol Name | (S) | The symbol name attribute specifier will search for symbol instances based on the specified symbol name. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Fill Background | (FB) | The fill background attribute type will search for objects that have the specified fill background. The search value should be a standard Vectorworks color index value (which can be obtained with [RGBToColorIndex](VS:RGBToColorIndex)). | |
| Fill Foreground | (FF) | The fill foreground attribute type will search for objects that have the specified fill foreground. The search value should be a standard Vectorworks color index value (which can be obtained with [RGBToColorIndex](VS:RGBToColorIndex)). | |
| Fill Pattern | (FP) | The fill pattern attribute type will search for objects that have the specified fill pattern. The search value should be the standard Vectorworks fill pattern selector value (in a range of 0 – 71). | |
| Gradient Fill | (GFI) | The gradient fill attribute specifier will search for objects that have the gradient fill with the specified name. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Hatch Fill | (HFI) | The hatch fill attribute specifier will search for objects that have the hatch fill with the specified name. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Image Fill | (IFI) | The image fill attribute specifier will search for objects that have the image fill with the specified name. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Tile Fill | (TFI) | The tile fill attribute specifier will search for objects that have the tile fill with the specified name. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Texture | (TX) | The texture attribute specifier will search for objects that have the texture with the specified name. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Pen Background | (PB) | The pen background attribute specifier will search for objects that have the specified pen background. The search value should be a standard Vectorworks color index value (which can be obtained with [RGBToColorIndex](VS:RGBToColorIndex)). | |
| Pen Foreground | (PF) | The pen foreground attribute specifier will search for objects that have the specified pen foreground. The search value should be a standard Vectorworks color index value (which can be obtained with [RGBToColorIndex](VS:RGBToColorIndex)). | |
| Pen Pattern | (PP) | The pen pattern attribute specifier will search for objects that have the indicated pen pattern. The search value should be a standard pen pattern selector value. | |
| Line Style | (LS) | The line style attribute specifier will search for objects that have the indicated pen style (solid, pattern, line type, etc.). The search value should be a standard line style selector value. | |
| Line Type | (LT) | The line type attribute specifier will search for objects that have the indicated line type. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Line Weight | (LW) | The line weight attribute specifier will search for objects that have the indicated line weight. The search value should be an *INTEGER* value specifying the line weight. | |
| Opacity | (OPA) | The opacity specifier will search for objects with the specified opacity percentage (in a range of 0 to 100). | |
| Marker Style | (AR) | The marker style attribute specifier will search for objects using the indicated marker style. The search value should be one of the supported marker style flag selector values (see marker styles constants [Function Reference Appendix](VS:Function_Reference_Appendix#appx_i)). | |
| Marker Size | (ASZ) | The marker size attribute specifier will search for objects using a marker of the specified size. The search value is the size of the marker in inches (marker size value in inches). | |
| Material | (MAT) | The material attribute specifier will search for objects that have the specified material. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Sketch Style | (SST) | The sketch style attribute specifier will search for objects that use the specified sketch style. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Wall Style | (WST) | (Design Series required) The wall style attribute specifier will search for walls that have the specified wall style. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Slab Style | (SLST) | (Design Series required) The slab style attribute specifier will search for slabs that have the specified slab style. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Roof Style | (RST) | (Design Series required) The roof style attribute specifier will search for roofs/roof faces that have the specified roof style. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Component | (COMP) | The component attribute specifier will search for walls, roofs, slabs, hardscapes that have components with the specified name. The search value should be a *STRING* value (literals and variables are supported). | |
| Plug-in Style | (PST) | The plug-in style attribute specifier will search for plug-in objects that have the specified style. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Font | (FOT) | The font attribute specifier will search for objects that have text with the specified font. The search value should be a *STRING* value (literals and variables are supported). | |
| Font Size | (FSZ) | The font size attribute specifier will search for objects that have text with the specified font size. The search value is the font size value in points (font size in points). | |
| Text Style | (TSTY) | The text style attribute specifier will search for objects that have text with the specified text style. The search value should be a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |
| Selection | (SEL) | The selection specifier will search for selected or deselected objects. The search value is a *BOOLEAN* value indicating the selection state (*TRUE* for selected, *FALSE* for deselected). | |
| Visible Selection | (VSEL) | The visible selection specifier will search for selected objects that are visibly selected in the document and indicated on the object info palette. The search value is a *BOOLEAN* value indicating the selection state (*TRUE* for selected, *FALSE* for deselected). | |
| Visibility | (V) | The visibility attribute specifier will search for objects based on their visibility status. The search value is a *BOOLEAN* value indicating the visibility state (*TRUE* for visible, *FALSE* for invisible). | |
| Plane | (PLA) | The plane specifier will search for objects that belong to the specified plane. The search value should be a *STRING* value indicating the name of the plane (literals and variables are supported). | |
| Flipped Status | (ISFLIPPED) | The flipped status specifier will search for objects based on their flipped state. | |
| Location | (LOC) | The location specifier will search for objects that are within the boundary of the specified named object. The search value is a *STRING* value which is up to 64 characters in length (literals and variables are supported). | |

## Spezialisiertes Filtern

Zusätzlich zu den Standard-Attributtypen, die für die Verwendung in Filterausdrücken zur Verfügung stehen, bieten Skripte auch spezielle Filter-Attributtypen für zusätzliche Flexibilität bei der Suche in einer Datei.

### Werte in Datenbankfeldern

Datenbankfelder können mit Hilfe eines speziellen Attributtyps zur Abfrage des Feldwerts nach bestimmten übereinstimmenden Werten durchsucht werden. Die Syntax für die Abfrage von Datenbankfeldern lautet:

```pascal
(<Datenbankname>.<Feldname>[< = |<> |> |>= |< |<= ><Suchwert>])
```

Die Datenbank- und Feldnamen sind STRING-Werte und sollten in einfache Anführungszeichen gesetzt werden. Jeder der optionalen Vergleichsoperatoren kann verwendet werden, um die Suche auf eine bestimmte Teilmenge von Elementen zu fokussieren, die mit der Datenbank verknüpft sind. So wird zum Beispiel mit

```pascal
('Montagedaten'.'Grundkosten' < 250.00)
```

nach Elementen gesucht, die mit der Datenbank verknüpft sind und deren Grundkosten weniger als 250.00 betragen.

[CMP] undokumentierte, aber sehr nützliche Funktion: Die Wildcards ? und * können in Suchwerten verwendet werden. So findet zum Beispiel

```pascal
('Gerät'.'Name' = 'VJF_*')
```

alle Felder, deren Werte mit "VJF_" beginnen. Meine Tests haben gezeigt, dass mehrere Instanzen von * und ? in einem Suchbegriff verwendet werden können und dass diese sich ziemlich intelligent verhalten. So kann zum Beispiel nach Strings gesucht werden, die einen Teilstring enthalten.

### In Symbolinstanzen suchen (INSYMBOL)

Der Spezifikator *INSYMBOL* veranlasst die Suche, in allen gefundenen Symbolen nach der Symboldefinition zu suchen. Angenommen, Sie richten ein großes Büro ein und möchten die Gesamtzahl der zu beschaffenden Schreibtischteile zählen. Ihr Dokument enthält eine Mischung aus Symbolen für einzelne Schreibtische und Schubladenelemente sowie Symbole, die sich aus einer Kombination der beiden Schreibtischkomponenten zusammensetzen. Eine Suche nach dem Ausdruck

```pascal
(S IN ['3660 Schreibtisch','3660 LH Schubladenelement'])
```

wird eine ungenaue Zählung zurückgegeben, da Instanzen von Symbolen, die selbst innerhalb eines anderen Symbols liegen, nicht berücksichtigt werden. Fügen Sie den Typ-Spezifikator INSYMBOL zum Ausdruck hinzu:

```pascal
((S IN ['3660 Schreibtisch','LH Schubladenelement']) & (INSYMBOL))
```

zwingt die Suche, in allen gefundenen Symbolen zu suchen und alle eingebetteten Instanzen der Symbole im Suchausdruck zu erkennen.


### In Intelligenten Objekten suchen (INOBJECT)

Der Spezifikator *INOBJECT* veranlasst die Suche, in Plug-in-Objekte zu suchen und auch deren einzelne Bestandteile auszuwerten. Normalerweise werden Unterobjekte von Plug-in-Objekten und Symbolen von den Filterkriterien ignoriert. Die Spezifikatoren INSYMBOL und INOBJECT beeinflussen das Durchlaufen der Zeichnung und bewirken, dass mehr Objekte anhand der Filterkriterien ausgewertet werden.

Um zum Beispiel die Anzahl der Rechtecke in der Zeichnung zu zählen, einschließlich der Rechtecke, die sich innerhalb von Symbolen und Plug-in-Objekten befinden, verwenden Sie den folgenden Ausdruck:

```pascal
ZÄHLEN(INSYMBOL & INOBJECT & (T=RECHTECK))
```

### In Ansichtsbereichen suchen (INVIEWPORT)

Der Spezifikator *INVIEWPORT* veranlasst die Suche, in den Ergänzungen aller gefundenen Ansichtsbereiche zu suchen Sie können z. B. nach Zeichnungsbeschriftungen oder Bemaßungen innerhalb der Ergänzung suchen. Eine Suche mit dem Ausdruck

```pascal
(S IN [T=BEMASSUNG])
```

wird eine ungenaue Anzahl zurückgeben, da er keine Ansichtsbereiche enthält. Fügen Sie den Typ-Spezifikator INVIEWPORT zum Ausdruck hinzu:

```pascal
(S IN (INVIEWPORT)&(T= BEMASSUNG))
```

zwingt die Suche, alle Bemaßungen in den Ergänzungen der Ansichtsbereiche zu finden.

Auf ähnliche Weise können Sie nicht referenzierte Ansichtsbereiche auf Konstruktionsebenen mit dem Spezifikator *NOTINDLVP* und referenzierte Ansichtsbereiche auf Konstruktionsebenen mit *NOTINREFDLVP* ausschließen..

```pascal
(S IN (NOTINDLVP)&(PON='Door CW'))
```
findet alle Türen, die sich nicht in nicht referenzierten Ansichtsbereichen auf Konstruktionsebenen befinden.

```pascal
(S IN (NOTINREFDLVP)&(PON='Door CW'))
```
findet alle Türen, die sich nicht in referenzierten Ansichtsbereichen auf Konstruktionsebenen befinden.

### Ort (LOC)

Der *LOC*-Spezifikator findet Objekte, die sich innerhalb der Grenzen eines benannten Objekts befinden, z. B. innerhalb eines Zauns.

### Spiegelungsstatus eines Symbols (GESPIEGELT)

Der Spezifikator *GESPIEGELT* prüft den Spiegelungsstatus von Symbolen oder anderen Objekten. Um zum Beispiel die Anzahl aller gespiegelten Instanzen eines bestimmten Symbols festzustellen, findet der Ausdruck:

```pascal
((S=’Zargentür’) & (GESPIEGELT))
```

nur die Instanzen des Symbols, die gespiegelt wurden. Der GESPIEGELT-Spezifikator ist nützlich, um die Ausrichtung von Objekten für die Bearbeitung oder verwandte Aufgaben herauszufinden.


### Project Sharing criteria

Working Files may be searched for object ownership or modification status.

#### Ownership (OWN)

The owner criteria will test the userid that has checked out an object. The special string '#' will match objects checked out to the current user in the current file. 
```pascal
(OWN=’rberge’)
(OWN='#')
```

The special string '*' will match objects checked out by anyone and exclude objects available to check out. An empty string can be used to match objects available to check out. 
```pascal
(OWN=’*’)
(OWN=’’)
```

#### Modification status (MODIFIED)

The modification status will match objects that have been modified in the current working file and will be submitted in the next commit. 
```pascal
(MODIFIED=TRUE) | (MODIFIED=FALSE)
```

#### Container modification status (MOCMODIFIED)

The container modification status will match objects that have been modified directly. It will also match containers like layers or groups that have contents that have been modified. 
```pascal
(MOCMODIFIED=TRUE)
```


### Alle Objekte (ALL)

Mit dem Attributtyp *ALL* werden alle Objekte im Dokument aktiviert. 

## Filterkriterien-Tabelle

Die Attributtypen für Filterkriterien sind in der folgenden Tabelle aufgelistet.

| Attributtyp | Typauswahl | Beispiel |
|----------------|---------------|---------|
| All objects | ALL | n/a |
| Descend into plug‐in objects | INOBJECT | (T=RECT) & INOBJECT |
| Descend into symbols | INSYMBOL | & (INSYMBOL) |
| Descend into viewport annotations | INVIEWPORT | & (INVIEWPORT) |
| Do not descend into non‐referenced design layer viewports | NOTINDLVP | & (NOTINDLVP) |
| Do not descend into referenced design layer viewports | NOTINREFDLVP | & (NOTINREFDLVP) |
| Attached Record | R | R IN \[Part Data\] |
| Class | C | C='Millwork' |
| Layer | L | L='First Floor' |
| Object Type | T | Type selector (see table) |
| Story | STO | STO = 'Second Floor' |
| Object Name | N | N = 'Name-1' |
| Symbol Name | S | S = 'My Symbol' |
| Fill Background | FB | Color index value |
| Fill Foreground | FF | Color index value |
| Fill Pattern | FP | FP=4 |
| Gradient Fill | GFI | GFI='Fall' |
| Hatch Fill | HFI | HFI='Stipple Dark' |
| Image Fill | IFI | IFI='Stones' |
| Tile Fill | TFI | TFI='Tile‐1' |
| Texture | TX | TX='Glass' |
| Pen Background | PB | Color index value |
| Pen Foreground | PF | Color index value |
| Pen Pattern | PP | PP=3 |
| Line Style | LS | INTEGER value |
| Line Type | LT | LT='Line Type‐1' |
| Line Weight | LW | INTEGER value |
| Marker | AR | INTEGER selector value |
| Marker Size | ASZ | ASZ=0.125 |
| Opacity | OPA | OPA=70 |
| Material | MAT | MAT='Wood' |
| Sketch Style | SST | SST='Rough' |
| Wall Style | WST | WST='Wallstyle‐1' |
| Slab Style | SLST | SLST='SlabStyle‐1' |
| Roof Style | RST | RST='RoofStyle‐1' |
| Component | COMP | COMP='Brick Veneer' |
| Plug-in Style | PST | PST='WindowStyle‐1' |
| Font | FOT | FOT='Arial' |
| Font Size | FSZ | FSZ=10 |
| Text Style | TSTY | TSTY='Text Style‐1' |
| Location is contained within boundary of a named object | LOC | (LOC='MyRoom') |
| Plane | PLA | PLA='Layer Plane' |
| Selected status | SEL | BOOLEAN value |
| Visible Selected status | VSEL | BOOLEAN value |
| Visibility status | V | BOOLEAN value |
| Flipped status | ISFLIPPED | n/a |
| Owner in Project Sharing | OWN | String for userid, #, *, or empty string. |
| Modification status in Project Sharing | MODIFIED | BOOLEAN value |
| Object or contents modification status in Project Sharing | MOCMODIFIED | BOOLEAN value |

| Object Type | Type Selector | Example |
|-------------|---------------|---------|
| 2D Locus | LOCUS | T=LOCUS |
| 3D Locus | LOCUS3D | T=LOCUS3D |
| 3D Polygon | POLY3D | T=POLY3D |
| Arc | ARC | T=ARC |
| Bitmap Image | BITMAP | T=BITMAP |
| Component Index<br>(objects that have components;<br>available only in IFC mapping formulas) | INDEX | T=INDEX |
| Cone, Sphere, Pyramid | SOLID | T=SOLID |
| CSG Solid | CSGSOLID | T=CSGSOLID |
| Dimension | DIMENSION | T=DIMENSION |
| Extrude | XTRD | T=XTRD |
| Freehand | FHAND | T=FHAND |
| Group | GROUP | T=GROUP |
| Layer Link | LAYERLINK | T=LAYERLINK |
| Line | LINE | T=LINE |
| Mesh | MESH | T=MESH |
| Multiple Extrude | MXTRD | T=MXTRD |
| Oval | OVAL | T=OVAL |
| PICT Image | PICT | T=PICT |
| Plug-in Object | PLUGINOBJECT | T=PLUGINOBJECT |
| Polygon | POLY | T=POLY |
| Polyline | POLYLINE | T=POLYLINE |
| Quarter Arc | QARC | T=QARC |
| Rectangle | RECT | T=RECT |
| Roof | ROOF | T=ROOF |
| Roof Element | ROOFELEMENT | T=ROOFELEMENT |
| Roof Face, Floor, Column | SLAB | T=SLAB |
| Round Wall | ROUNDWALL | T=ROUNDWALL |
| Rounded Rectangle | RRECT | T=RRECT |
| Sub Type<br>(all objects except plug-in objects; <br>available sub types are listed in<br>[Search Criteria Sub Types](VS:Search_Criteria#Search Criteria Sub Types) ) | ST | ST=CONE |
| Sub Type (plug-in object names only) | PON | PON=“DOOR” |
| Sweep | SWEEP | T=SWEEP |
| Symbol | SYMBOL | T=SYMBOL |
| Text | TEXT | T=TEXT |
| Wall | WALL | T=WALL |
| Worksheet | SPRDSHEET | T=SPRDSHEET |

### Filterkriterien-Untertypen

Verwenden Sie die ST-Objekttyp-Auswahl für Objekte, die keine Plug-in-Objekte sind, stehen die folgenden Untertypen zur Verfügung:

| Objekt-Untertyp	| Objekttyp | Untertyp-Auswahl | Beispiel |
|----------------|-------------|-------------------|---------|
| Directional Light | Light | DIRLIGHT | ST=DIRLIGHT |
| Spot Light | Light | SPOTLIGHT | ST=SPOTLIGHT |
| Point Light | Light | POINTLIGHT | ST=POINTLIGHT |
| Custom Light | Light | CUSTLIGHT | ST=CUSTLIGHT |
| Area Light | Light | AREALIGHT | ST=AREALIGHT |
| Line Light | Light | LINELIGHT | ST=LINELIGHT |
| Regular Viewport | Viewport | REGVIEWPORT | ST=REGVIEWPORT |
| Section Viewport | Viewport | SECTVIEWPORT | ST=SECTVIEWPORT |
| Floor | Floor | FLOOR | ST=FLOOR |
| Roof Face | Roof face | ROOFFACE | ST=ROOFFACE |
| Pillar | Pillar | PILLAR | ST=PILLAR |
| Cone | Solid | CONE | ST=CONE |
| Sphere | Solid | SPHERE | ST=SPHERE |
| Hemisphere | Solid | HEMISPHERE | ST=HEMISPHERE |
| Circle | Arc | CIRCLE | ST=CIRCLE |
| Opened Arc | Arc | OPENEDARC | ST=OPENEDARC |
| Solid Subtraction | CSG Solid | CSGSUBTR | ST=CSGSUBTR |
| Solid Addition | CSG Solid | CSGADD | ST=CSGADD |
| Solid Intersection | CSG Solid | CSGINTER | ST=CSGINTER |
| Solid Section | CSG Solid | CSGSECT | ST=CSGSECT |
| Shell | CSG Solid | CSGSHELL | ST=CSGSHELL |
| Chamfer | CSG Solid | CSGCHAMFER | ST=CSGCHAMFER |
| Fillet | CSG Solid | CSGFILLET | ST=CSGFILLET |
| Control Point Based NURBS Surface | NURBS Surface | NURBSSURFCTRLP | ST=NURBSSURFCTRLP |
| Interpolated NURBS Surface | NURBS Surface | NURBSSURFINTERP | ST=NURBSSURFINTERP |
