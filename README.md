# box2d-2.4.2-cmake
Box2D 2.4.2 CMake wrapper.

## Integration

```
FetchContent_Declare(
	box2d
	GIT_REPOSITORY https://github.com/WMask/box2d-2.4.2-cmake.git
	GIT_TAG        f12cea4291d5296c6a89f21cc8cbc3739e425f98 # release - 2.4.2
)

FetchContent_MakeAvailable(box2d)
FetchContent_GetProperties(box2d)

...

target_include_directories(TargetModuleName
	PUBLIC
		${box2d_SOURCE_DIR}/box2d-src-v.2.4.2/include
)
target_link_libraries(TargetModuleName box2d)
```
