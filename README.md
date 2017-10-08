# How to create a GN-based project

*by Maksym Motornyy (mmotorny@gmail.com)*



[Instructions for Linux](#instructions-for-linux)

[Instructions for macOS](#instructions-for-macos)

[Instructions for Windows](#instructions-for-windows)



## Instructions for Linux

### Prerequisites

Install GN.

```sh
cd $(mktemp -d)
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
git clone https://chromium.googlesource.com/chromium/buildtools
PATH=$PATH:depot_tools python depot_tools/download_from_google_storage.py \
    --no_resume --platform=linux* --no_auth --bucket chromium-gn \
    -s buildtools/linux64/gn.sha1
sudo cp buildtools/linux64/gn /usr/local/bin
sudo chmod a+x /usr/local/bin/gn
```

Install Ninja.

```sh
sudo apt install ninja-build
```

### Create a project

Create a project directory.

```sh
mkdir your_project
cd your_project
```

*Option 1.* Clone the GN configuration.

```sh
git clone https://github.com/mmotorny/build.git
```

*Option 2.* If your project is tracked by Git, add the GN configuration as a submodule.

```sh
git submodule add https://github.com/mmotorny/build build
```

Initialize the source root with templates of `.gn` and `BUILDCONFIG.gn` files.

```sh
cp build/templates/*.gn .
```

*Optional.* [Customize `BUILDCONFIG.gn`](/templates/README.md).

Now you are ready to [write a `BUILD.gn` file](https://chromium.googlesource.com/chromium/src/tools/gn/+/HEAD/docs/quick_start.md#adding-a-build-file).



## Instructions for macOS

### Prerequisites

Install GN.

```sh
cd $(mktemp -d)
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
git clone https://chromium.googlesource.com/chromium/buildtools
PATH=$PATH:depot_tools python depot_tools/download_from_google_storage.py \
    --no_resume --platform=darwin --no_auth --bucket chromium-gn \
    -s buildtools/mac/gn.sha1
cp buildtools/mac/gn /usr/local/bin
```

Install Ninja.

```sh
brew install ninja
```

### Create a project

Create a project directory.

```sh
mkdir your_project
cd your_project
```

*Option 1.* Clone the GN configuration.

```sh
git clone https://github.com/mmotorny/build.git
```

*Option 2.* If your project is tracked by Git, add the GN configuration as a submodule.

```sh
git submodule add https://github.com/mmotorny/build build
```

Initialize the source root with templates of `.gn` and `BUILDCONFIG.gn` files.

```sh
cp build/templates/*.gn .
```

*Optional.* [Customize `BUILDCONFIG.gn`](/templates/README.md).

Now you are ready to [write a `BUILD.gn` file](https://chromium.googlesource.com/chromium/src/tools/gn/+/HEAD/docs/quick_start.md#adding-a-build-file).



## Instructions for Windows

TODO
