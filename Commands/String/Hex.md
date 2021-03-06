# StrFormat,Hex

Convert an integer to it's hexadecimal representation.

**This command is included for compatibility with Winbuilder 082. It is recommended that you update your code to use the more flexible `Math,Hex` command.**

## Syntax

```pebakery
StrFormat,Hex,<Integer>,<%DestVar%>
```

### Arguments

| Argument | Description |
| --- | --- |
| Integer | Number to convert. |
| DestVar | Variable where the resulting Hex representation will be stored. |

## Remarks

Negative integer conversion is supported.

For backwards compatibility with Winbuilder only 32bit integers are supported.

## Related

[Math,Hex](../Math/Hex.md)

## Examples

### Example 1

```pebakery
[Main]
Title=StrFormat-Hex
Description=Show the usage of StrFormat,Hex.
Level=5
Version=1
Author=Homes32

[Variables]
%Int1%=88888888
%Int2%=-2

[process]
StrFormat,Hex,%Int1%,%result1%
StrFormat,Hex,%Int2%,%result2%
Message,"Input: [%Int1%] Hex: [0x%result1%]#$xInput: [%Int2%] Hex: [0x%result2%]"
```