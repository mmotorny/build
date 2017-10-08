# Customizing `BUILDCONFIG.gn`

### Default toolchain

`BUILDCONFIG.gn` [autodetects](/toolchains/README.md#toolchain-autodetection) the default toolchain based on `target_os`.

```python
import("//build/toolchains/autodetect.gni")
```

In order to override the autodetection, specify the default toolchain explicitly.

```python
if (target_os == "linux") {
  # Prefer Clang on Linux.
  set_default_toolchain("//build/toolchains/clang")
} else {
  # Fall back to the toolchain autodetection.
  import("//build/toolchains/autodetect.gni")    
}
```

See [Supported toolchains](/toolchains/README.md#supported-toolchains) for the list of toolchains.

### Default compiler configs

Specify configs that apply to all compilers by setting `default_compiler_configs` variable.

```python
default_compiler_configs = [
  # Compile as C++14.
  "//build/configs/cxx_standard:cxx_14",
  
  # Enable source-tree absolute paths in #include statements.
  "//build/configs/include_dirs:source_tree_absolute",
]
```

See [Configs reference](/configs/README.md) for the list of supported configs.