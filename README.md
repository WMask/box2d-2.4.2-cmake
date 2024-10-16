# box2d-2.4.2-cmake
Box2D 2.4.2 CMake wrapper

## Integration

FetchContent_Declare(
	box2d
	GIT_REPOSITORY https://github.com/WMask/box2d-2.4.2-cmake.git
	GIT_TAG        3ac4500f1122f18f04d2c3fd2af2cbff39501af1 # release - 2.4.2
)

FetchContent_MakeAvailable(box2d)
FetchContent_GetProperties(box2d)

...

target_link_libraries(TargetModuleName box2d)
