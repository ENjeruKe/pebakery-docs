# List,PosX

Returns the position of the given value inside the specified list. **Case Sensitive.**

## Syntax

```pebakery
List,PosX,<%ListVar%>,<Value>,<%DestVar%>[,Delim=<Str>]
```

### Arguments

| Argument | Description |
| --- | --- |
| ListVar | The variable containing the list. |
| Value | The value to find within the list. |
| DestVar | The variable where the result will be saved. |
| Delim= | **(Optional)** Delimiter used to separate the items in the list. Case Insensitive. **Default:** `\|` |

## Remarks

If the `Value` is not found the `%DestVar%` will return zero.

If multiple occurrences of `Value` exist within the list only the first occurrence will be returned.

## Related

[List,LastPos](./LastPos.md), [List,LastPosX](./LastPosX.md), [List,Pos](./Pos.md)

## Examples

### Example 1

Get the index for the first occurrence of _Starter_.

```pebakery
[Main]
Title=List-PosX Example
Description=Demonstrate usage of List,PosX.
Level=5
Version=1
Author=Homes32

[variables]
%myList%=Home|UlTiMaTe|StarteR|Professional|Starter|Enterprise|PrOfEsSiOnAl|Starter|Ultimate

[process]
List,PosX,%myList%,Starter,%result%
Message,"Value [Starter] is at position: %result%"
```