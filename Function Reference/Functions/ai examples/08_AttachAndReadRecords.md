# 08. Attach and Read Records on Objects

## Description
Data records are Vectorworks' answer to "tag every object with structured
metadata". This example creates a small `Furniture Info` record, drops three
rectangles that stand in for pieces of furniture, attaches the record to each,
fills in its fields, and finally reads the data back — the same round-trip the
`Comm Device` and `Circuiting Tool` plug-ins perform.

## What This Demonstrates
- Defining a record and its fields with
  [`NewField`](../NewField.md) (auto-creates the record)
- Attaching the record to an object with
  [`SetRecord`](../SetRecord.md)
- Writing field values with [`SetRField`](../SetRField.md)
- Reading them back with [`GetRField`](../GetRField.md)
- Iterating objects that carry the record with
  [`ForEachObject`](../ForEachObject.md)

## Python Script
```python
import vs

kRecordName = 'Furniture Info'

# NewField `fType` codes (see Appendix E):
#   1 = integer, 2 = boolean, 3 = number, 4 = text, 5 = number w/ dim units
kFieldType_Integer = 1
kFieldType_Boolean = 2
kFieldType_Text    = 4


def EnsureRecordFormat():
    """Create the record on the fly if it doesn't already exist.

    NewField creates the record itself the first time it's called, so we can
    safely call it every run — it will re-use the existing format.
    """
    vs.NewField(kRecordName, 'AssetTag',    '',      kFieldType_Text,    0)
    vs.NewField(kRecordName, 'RoomNumber',  '101',   kFieldType_Text,    0)
    vs.NewField(kRecordName, 'Quantity',    '1',     kFieldType_Integer, 0)
    vs.NewField(kRecordName, 'NeedsPower',  'False', kFieldType_Boolean, 0)


def PlaceTaggedItem(tag, roomNumber, quantity, needsPower, x, y):
    """Draw a rectangle and attach a filled-in Furniture Info record."""
    vs.Rect(x, y, x + 1.0, y + 0.6)
    h = vs.LNewObj()

    vs.SetRecord(h, kRecordName)
    vs.SetRField(h, kRecordName, 'AssetTag',   tag)
    vs.SetRField(h, kRecordName, 'RoomNumber', roomNumber)
    vs.SetRField(h, kRecordName, 'Quantity',   str(quantity))
    vs.SetRField(h, kRecordName, 'NeedsPower', 'True' if needsPower else 'False')

    # Print the tag next to the shape so you can eyeball what got stored.
    vs.TextOrigin(x, y + 0.7)
    vs.CreateText(tag)


def PrintRecord(h):
    """Callback used by ForEachObject to dump this object's Furniture Info."""
    tag   = vs.GetRField(h, kRecordName, 'AssetTag')
    room  = vs.GetRField(h, kRecordName, 'RoomNumber')
    qty   = vs.GetRField(h, kRecordName, 'Quantity')
    power = vs.GetRField(h, kRecordName, 'NeedsPower')
    vs.Message(tag, ' | room=', room, ' qty=', qty, ' power=', power)


def main():
    EnsureRecordFormat()

    PlaceTaggedItem('DESK-01', '101', quantity=1, needsPower=True,  x=0.0, y=0.0)
    PlaceTaggedItem('CHAIR-01','101', quantity=4, needsPower=False, x=2.0, y=0.0)
    PlaceTaggedItem('LAMP-01', '102', quantity=2, needsPower=True,  x=4.0, y=0.0)

    # Criteria: "any object that has the Furniture Info record attached".
    criteria = "R IN ['" + kRecordName + "']"
    vs.ForEachObject(PrintRecord, criteria)

main()
```

## Key VectorScript Functions Used
- [`NewField`](../NewField.md), [`SetRecord`](../SetRecord.md)
- [`SetRField`](../SetRField.md), [`GetRField`](../GetRField.md)
- [`ForEachObject`](../ForEachObject.md)
- [`Rect`](../Rect.md), [`LNewObj`](../LNewObj.md)
- [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`Message`](../Message.md)
