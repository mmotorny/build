# Toolchains reference

### Supported toolchains

Build with GCC.

```
//build/toolchains/gcc
```

Build with Clang.

```
//build/toolchains/clang
```

Build with Xcode.

```
//build/toolchains/xcode
```

Build with Visual Studio.

```
//build/toolchains/visual_studio
```

### Toolchain autodetection

Enable the autodetection of the default toolchain.

```python
import("//build/toolchains/autodetect.gni")
```

The autodetection is based on `target_os`:

- GCC is the default on Linux.
- Xcode is the default on macOS.
- Visual Studio is the default on Windows.