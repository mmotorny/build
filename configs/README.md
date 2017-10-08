# Configs reference

## Common compiler configs

### Include directories

Enable source-tree absolute paths in `#include` statements.

```
//build/configs/include_dirs:source_tree_absolute
```

### Warnings

Enable pedantic warnings.

```
//build/configs/warnings:pedantic
```

Treat warnings as errors.

```
//build/configs/warnings:treat_as_errors
```



## C++ configs

### C++ standard

Compile as C++98.

```
//build/configs/cxx_standard:cxx_98
```

Compile as C++03.

```
//build/configs/cxx_standard:cxx_03
```

Compile as C++11.

```
//build/configs/cxx_standard:cxx_11
```

Compile as C++14.

```
//build/configs/cxx_standard:cxx_14
```

Compile as C++17.

```
//build/configs/cxx_standard:cxx_17
```

