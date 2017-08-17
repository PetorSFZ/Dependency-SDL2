# phDependency_SDL2
This is a distribution and CMake wrapper of the SDL2 library (available from https://www.libsdl.org/). It bundles the official pre-built SDL2 binaries (https://libsdl.org/download-2.0.php) for Windows in order to make it easier to build. Uses `FindSDL2.cmake` module (originally found in Twinklebear-Dev SDL tutorial: `https://github.com/Twinklebear/TwinklebearDev-Lessons/blob/master/cmake/FindSDL2.cmake`) on other platforms.

# Usage

Place this entire directory in the subdirectory of your CMake project, then add it with `add_subdirectory()`. Three CMake variables are returned:

`${SDL2_FOUND}`: Variable that signals whether SDL2 is available or not.

`${SDL2_HEADERS}`: The headers you need to include with `include_directories()` or similar.

`${SDL2_LIBRARIES}`: The libraries you need to link your to with `target_link_libraries()`.

`${SDL2_RUNTIME_FILES}`: The path to runtime files. On Windows this is the `SDL2.dll`.


# License

Made by `Peter Hillerström` ([GitHub](https://github.com/PetorSFZ)). I license this whole build wrapper as `public domain` (`SDL2` is obviously still `zlib`). The sole exception being the `FindSDL2.cmake` module, which is under unknown license (but likely BSD "the license" to Kitware). Feel free to do whatever you want with this wrapper, but it would be nice if you kept this readme and the header in the `CMakeLists.txt` file.