
# Unicode Support

## ConEmu

- [ConEmu Unicode Support](https://conemu.github.io/en/UnicodeSupport.html)

Check active codepage:

```powershell
$ chcp
# Active code page: 850
```

Set `UTF-8` encoding:

```powershell
$ chcp 65001 & cmd
# Active code page: 65001
```

CheckUnicode test:

```powershell
$ ConEmuC -CheckUnicode
# Unicode check succeeded
```

`UTF-8` test:

```powershell
$ cmd /c "%ConEmuBaseDir%\Addons\utf-8-test.cmd"
# If you can read the output of this batch
#  your console runs correctly.
```

---
