from os import path

env = DefaultEnvironment()
env.Append(
    CXXFLAGS=["-O2", "-g", "-Wall", "-std=c++1y", "-fdiagnostics-color=auto", '-Wno-deprecated-declarations', '-DEIGEN_DONT_ALIGN_STATICALLY'],
    LINKFLAGS=["-Wl,--unresolved-symbols=ignore-in-shared-libs", "-Wl,--as-needed"],
    CPPPATH=['/usr/local/include', 'include', '/usr/local/opencv3/include', '.'],
    LIBPATH=['/usr/local/lib', '/usr/local/lib64', '/usr/local/opencv3/lib', '.'],
)

SharedLibrary("dbow3", Glob('*.cpp'), LIBS=['opencv_core'])
Program("test/demo", Glob('*.cpp') + ["test/demo.cpp"], LIBS=['opencv_core', 'opencv_features2d', 'opencv_xfeatures2d', 'opencv_imgcodecs'])
