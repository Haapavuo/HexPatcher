# HexPatcher
A .NET command line tool to modify any binary files by their hex based address.

Targets .NET Core 1.1 Framework.

Create a configuration file that contains three rows:
- Binary file path
- Original bytes to find (can contain '\*' wildcard bytes)
- Modified bytes to replace the original bytes with

An example of a configuration file:
```
C:\Program Files\Company\Target.exe
E8 ** AB B2 FF 84 C0 75 08
E8 ** AB B2 FF 84 C0 74 08
```

The program will make a backup of the binary file before overwriting any of its content. The backup is stored at the same location as the original binary file and has a ".bak" extension added to its full filename.
