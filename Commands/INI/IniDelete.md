# IniDelete

Deletes a key from a standard .ini file.

## Syntax

```pebakery
IniDelete,<FileName>,<Section>,<Key>
```

### Arguments

| Argument | Description |
| --- | --- |
| FileName | The full path of the file. |
| Section | The Section containing the value to be removed. |
| Key | The value to be removed.|

## Remarks

PEBakery will optimize multiple `IniDelete` commands in a row into single delete command.

## Example

Lets assume we have the following .ini file:

```pebakery
// C:\myFile.ini
[mySection]
myKey=myValue
anotherKey=anotherValue
```

In the following example the key `myKey` and it's value will be removed.

```pebakery
IniDelete,C:\myFile.ini,mySection,myKey
```