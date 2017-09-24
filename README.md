# How to create a GN-based project

*by Maksym Motornyy (mmotorny@gmail.com)*

[Instructions for Linux](#instructions-for-linux)
[Instructions for macOS](#instructions-for-macos)
[Instructions for Windows](#instructions-for-windows)



## Instructions for Linux

TODO



## Instructions for macOS

### Prerequisites

Install GN.

```shell
cd $TMPDIR
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
git clone https://chromium.googlesource.com/chromium/buildtools
python depot_tools/download_from_google_storage.py --no_resume \
    --platform=darwin --no_auth --bucket chromium-gn -s buildtools/mac/gn.sha1
cp buildtools/mac/gn /usr/local/bin
```

Install Ninja.

```shell
brew install ninja
```

### Create a project

Create a project directory.

```sh
mkdir your_project
cd your_project
```

Checkout the GN configuration.

```shell
git clone https://github.com/mmotorny/build.git
```

Create a `.gn` file to indicate the source root.

```shell
echo 'buildconfig = "//build/BUILDCONFIG.gn"' > .gn
```

Now you are ready to [write a `BUILD.gn` file](https://chromium.googlesource.com/chromium/src/tools/gn/+/HEAD/docs/quick_start.md#adding-a-build-file).



## Instructions for Windows

TODO