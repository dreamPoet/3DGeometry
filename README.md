# Acquisition and Processing of 3D Geometry



##How to configure Libigl with VS2017

you only need to download libigl and cmake. For libigl, make sure use 

` git clone --recursive https://github.com/libigl/libigl.git`

to get the correct relation and the whole files.

Remember to add cmake/bin to `PATH`.

```
cd tutorial
mkdir build
cd build
cmake -G "Visual Studio 15 2017 Win64" ../
```

Modify the string for different VS version.

Take 102 as an example. Open`build/102_DrawMesh` and click `102_DrawMesh.sln`. Set `102_DrawMesh_bin` as StartUp Project. Use `Debug` or `Release` with `x64`. Finally you can get an `.exe` and result window.

There may be no nanogui in the result window. I only find the way solving this problem is to use `cmake gui`  instead of `cmd`. Check the `LIBIGL_WITH_NANOGUI`. Click Configure button and then Generate Button. Pay attention that red in the configure box does not mean error happened. Finally click the `.sln` file and follow the steps mentioned before.

There may be some problems such as 

```
pthread.h does not found
Performing Test COMPILER_HAS_DEPRECATED_ATTR - Failed
Could NOT find MOSEK (missing: MOSEK_LIBRARIES MOSEK_INCLUDE_DIR)
```

But these errors do not influence the final success. ( I do not find the reason for these...)