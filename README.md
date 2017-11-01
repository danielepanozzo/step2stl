# step2stl
Example program of how to convert ISO 10303 STEP files (AP203 and AP 214) to STL using OpenCascade.
This is a fork of https://github.com/chfritz/step2stl that uses a cmake build system and works with OpenCascade 7.1

## Dependencies

You need OpenCascade.

### MACOSX:
```
brew install opencascade
```

## Compiling

This has been tested only on MacOSX but should also work on linux.

```
mkdir build
cd build
cmake ../
make
```

## Running

Once you have compiled it,
just use it as:

```
./step2stl STEPFILENAME STLFILENAME
```
