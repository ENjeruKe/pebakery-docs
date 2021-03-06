# Decompress

Extract files from an archive.

## Syntax

```pebakery
Decompress,<FileName>,<DestDir>[,Password=<Str>]
```

### Arguments

| Argument | Description |
| --- | --- |
| FileName | Full path of the archive to extract. |
| DestDir | Full path to the directory where the archive will be extracted. If the directory does not exist it will be created. |
| Password= | **(Optional)** If the archive is encrypted supply the plain-text password that will used to extract the files. |

## Supported Archive Formats

7z, APM, AR, ARJ, BZIP2, CAB, CHM, CPIO, CramFS, DEB, DMG, EXT, FAT, GPT, GZIP, HFS, IHEX, ISO, LZH, LZMA, MBR, MSI, NSIS, NTFS, QCOW2, RAR, RPM, SquashFS, TAR, UDF, UEFI, VDI, VHD, VMDK, WIM, XAR, XZ, Z, ZIP

**Note:** Only `7z`, `CAB`, `RAR`, and `ZIP` are officially tested.

Split archives are supported.

Extracting from encrypted/password protected archives is supported using the `Password=` argument.

## Remarks

Decompression is performed using [7-Zip](https://www.7-Zip.org).

## Related

[Compress](./Compress.md)

## Example

```pebakery
// Setting.7z will be extracted to %DestDir%.
Decompress,%SrcDir%\Setting.7z,%DestDir%
```
