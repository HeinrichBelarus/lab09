elarus@Roblox:~$ ls -l
total 44
drwxr-xr-x 2 belarus belarus 4096 May 11 22:33 Desktop
drwxr-xr-x 2 belarus belarus 4096 May 11 22:33 Documents
drwxr-xr-x 2 belarus belarus 4096 May 11 22:33 Downloads
drwxrwxr-x 3 belarus belarus 4096 May 11 23:09 HeinrichBelarus
drwxr-xr-x 2 belarus belarus 4096 May 11 22:33 Music
drwxr-xr-x 3 belarus belarus 4096 May 11 22:38 Pictures
drwxr-xr-x 2 belarus belarus 4096 May 11 22:33 Public
drwx------ 5 belarus belarus 4096 May 12 00:00 snap
drwxr-xr-x 2 belarus belarus 4096 May 11 22:33 Templates
drwxr-xr-x 2 belarus belarus 4096 May 11 22:33 Videos
drwxrwxr-x 6 belarus belarus 4096 May 26 01:59 workspace
belarus@Roblox:~$ cd /lab06
bash: cd: /lab06: No such file or directory
belarus@Roblox:~$ export GITHUB_USERNAME=
belarus@Roblox:~$ export GITHUB_USERNAME=HeinrichBelarus
belarus@Roblox:~$ alias gsed=sed # for *-nix system
belarus@Roblox:~$ cd ${GITHUB_USERNAME}/workspace
belarus@Roblox:~/HeinrichBelarus/workspace$ pushd .
~/HeinrichBelarus/workspace ~/HeinrichBelarus/workspace
belarus@Roblox:~/HeinrichBelarus/workspace$ source scripts/activate
belarus@Roblox:~/HeinrichBelarus/workspace$ cd projects/lab06
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ ls -l
total 36
drwxrwxr-x 4 belarus belarus 4096 May 27 00:02 _build
-rw-rw-r-- 1 belarus belarus 1133 May 26 23:56 CMakeLists.txt
drwxrwxr-x 2 belarus belarus 4096 May 27 00:03 include
-rw-rw-r-- 1 belarus belarus 1072 May 26 23:43 LICENSE
-rw-rw-r-- 1 belarus belarus  172 May 26 23:59 print.cpp
-rw-rw-r-- 1 belarus belarus   19 May 26 23:43 README.md
drwxrwxr-x 2 belarus belarus 4096 May 26 23:58 sources
drwxrwxr-x 2 belarus belarus 4096 May 26 23:56 tests
drwxrwxr-x 3 belarus belarus 4096 May 26 23:44 third-party
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ ls -l sources
total 4
-rw-rw-r-- 1 belarus belarus 172 May 27 00:02 print.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ ls -l include
total 0
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano sources/print.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano include/print.hpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git remote remove origin
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab06
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ mkdir third-party
mkdir: cannot create directory ‘third-party’: File exists
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git submodule add https://github.com/google/googletest third-party/gtest
fatal: 'third-party/gtest' already exists in the index
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cd third-party/gtest && git checkout release-1.8.1 && cd ../..
HEAD is now at 2fe3bd99 Merge pull request #1433 from dsacre/fix-clang-warnings
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git add third-party/gtest
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git commit -m"added gtest framework"
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	CMakeLists.txt
	_build/
	include/
	print.cpp
	sources/
	tests/

nothing added to commit but untracked files present (use "git add" to track)
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git add *
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git commit -m"added gtest framework"
[main 46b7d2c] added gtest framework
 23 files changed, 3260 insertions(+)
 create mode 100644 CMakeLists.txt
 create mode 100644 _build/CMakeCache.txt
 create mode 100644 _build/CMakeFiles/3.28.3/CMakeCCompiler.cmake
 create mode 100644 _build/CMakeFiles/3.28.3/CMakeCXXCompiler.cmake
 create mode 100755 _build/CMakeFiles/3.28.3/CMakeDetermineCompilerABI_C.bin
 create mode 100755 _build/CMakeFiles/3.28.3/CMakeDetermineCompilerABI_CXX.bin
 create mode 100644 _build/CMakeFiles/3.28.3/CMakeSystem.cmake
 create mode 100644 _build/CMakeFiles/3.28.3/CompilerIdC/CMakeCCompilerId.c
 create mode 100755 _build/CMakeFiles/3.28.3/CompilerIdC/a.out
 create mode 100644 _build/CMakeFiles/3.28.3/CompilerIdCXX/CMakeCXXCompilerId.cpp
 create mode 100755 _build/CMakeFiles/3.28.3/CompilerIdCXX/a.out
 create mode 100644 _build/CMakeFiles/CMakeConfigureLog.yaml
 create mode 100644 _build/CMakeFiles/cmake.check_cache
 create mode 100644 _build/third-party/gtest/googlemock/gtest/generated/GTestConfig.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/generated/GTestConfigVersion.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/generated/gmock.pc
 create mode 100644 _build/third-party/gtest/googlemock/gtest/generated/gmock_main.pc
 create mode 100644 _build/third-party/gtest/googlemock/gtest/generated/gtest.pc
 create mode 100644 _build/third-party/gtest/googlemock/gtest/generated/gtest_main.pc
 create mode 100644 include/print.hpp
 create mode 100644 print.cpp
 create mode 100644 sources/print.cpp
 create mode 100644 tests/test1.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ gsed -i '/option(BUILD_EXAMPLES "Build examples" OFF)/a\
option(BUILD_TESTS "Build tests" OFF)
' CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat >> CMakeLists.txt <<EOF

if(BUILD_TESTS)
  enable_testing()
  add_subdirectory(third-party/gtest)
  file(GLOB \${PROJECT_NAME}_TEST_SOURCES tests/*.cpp)
  add_executable(check \${\${PROJECT_NAME}_TEST_SOURCES})
  target_link_libraries(check \${PROJECT_NAME} gtest_main)
  add_test(NAME check COMMAND check)
endif()
EOF
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ mkdir tests
mkdir: cannot create directory ‘tests’: File exists
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat > tests/test1.cpp <<EOF
#include <print.hpp>

#include <gtest/gtest.h>

TEST(Print, InFileStream)
{
  std::string filepath = "file.txt";
  std::string text = "hello";
  std::ofstream out{filepath};

  print(text, out);
  out.close();

  std::string result;
  std::ifstream in{filepath};
  in >> result;

  EXPECT_EQ(result, text);
}
EOF
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake -H. -B_build -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googlemock/CMakeLists.txt:42 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googletest/CMakeLists.txt:49 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Warning (dev) at third-party/gtest/googletest/cmake/internal_utils.cmake:239 (find_package):
  Policy CMP0148 is not set: The FindPythonInterp and FindPythonLibs modules
  are removed.  Run "cmake --help-policy CMP0148" for policy details.  Use
  the cmake_policy command to set the policy and suppress this warning.

Call Stack (most recent call first):
  third-party/gtest/googletest/CMakeLists.txt:84 (include)
This warning is for project developers.  Use -Wno-dev to suppress it.

CMake Error at CMakeLists.txt:51 (add_subdirectory):
  The binary directory

    /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/third-party/gtest

  is already used to build a source directory.  It cannot be used to build
  source directory

    /home/belarus/HeinrichBelarus/workspace/projects/lab06/third-party/gtest

  Specify a unique binary directory name.


CMake Error at CMakeLists.txt:53 (add_executable):
  add_executable cannot create target "check" because another target with the
  same name already exists.  The existing target is an executable created in
  source directory "/home/belarus/HeinrichBelarus/workspace/projects/lab06".
  See documentation for policy CMP0002 for more details.


CMake Error at CMakeLists.txt:55 (add_test):
  add_test given test NAME "check" which already exists in this directory.


-- Configuring incomplete, errors occurred!
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build
gmake: Makefile: No such file or directory
gmake: *** No rule to make target 'Makefile'.  Stop.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ rm -rf _build
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ gsed -i '/if(BUILD_TESTS)/,/endif()/d' CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake -H. -B_build -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- The C compiler identification is GNU 13.3.0
-- The CXX compiler identification is GNU 13.3.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.2s)
CMake Error at CMakeLists.txt:12 (add_library):
  Cannot find source file:

    /sources/print.cpp

  Tried extensions .c .C .c++ .cc .cpp .cxx .cu .mpp .m .M .mm .ixx .cppm
  .ccm .cxxm .c++m .h .hh .h++ .hm .hpp .hxx .in .txx .f .F .for .f77 .f90
  .f95 .f03 .hip .ispc


CMake Error at CMakeLists.txt:12 (add_library):
  No SOURCES given to target: print


CMake Generate step failed.  Build files cannot be regenerated correctly.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano /sources/print.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano sources/print.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano sources/print.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano /sources/print.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ ls -l
total 36
drwxrwxr-x 3 belarus belarus 4096 May 27 00:16 _build
-rw-rw-r-- 1 belarus belarus  886 May 27 00:15 CMakeLists.txt
drwxrwxr-x 2 belarus belarus 4096 May 27 00:10 include
-rw-rw-r-- 1 belarus belarus 1072 May 26 23:43 LICENSE
-rw-rw-r-- 1 belarus belarus  172 May 26 23:59 print.cpp
-rw-rw-r-- 1 belarus belarus   19 May 26 23:43 README.md
drwxrwxr-x 2 belarus belarus 4096 May 27 00:16 sources
drwxrwxr-x 2 belarus belarus 4096 May 26 23:56 tests
drwxrwxr-x 3 belarus belarus 4096 May 26 23:44 third-party
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ ls -l sources
total 4
-rw-rw-r-- 1 belarus belarus 172 May 27 00:02 print.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake -H. -B_build -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- Configuring done (0.0s)
-- Generating done (0.0s)
-- Build files have been written to: /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ mkdir examples
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ touch examples/example1.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ touch examples/example2.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ ls -l examples
total 0
-rw-rw-r-- 1 belarus belarus 0 May 27 00:21 example1.cpp
-rw-rw-r-- 1 belarus belarus 0 May 27 00:21 example2.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat > examples/example1.cpp <<EOF
#include <print.hpp>

#include <iostream>

int main(int argc, char** argv) {
   print("hello", std::cout);
   return 0;
}
EOF
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat > examples/example2.cpp <<EOF
#include <print.hpp>
#include <fstream>

int main(int argc, char** argv) {
   std::ofstream file("log.txt");
   print(std::string("hello"), file);
   return 0;
}
EOF
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano example1.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano examples/example1.cpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build
[ 50%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
/home/belarus/HeinrichBelarus/workspace/projects/lab06/sources/print.cpp:1:9: fatal error: print.hpp: No such file or directory
    1 | #include<print.hpp>
      |         ^~~~~~~~~~~
compilation terminated.
gmake[2]: *** [CMakeFiles/print.dir/build.make:76: CMakeFiles/print.dir/sources/print.cpp.o] Error 1
gmake[1]: *** [CMakeFiles/Makefile2:83: CMakeFiles/print.dir/all] Error 2
gmake: *** [Makefile:136: all] Error 2
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ ls -l include
total 4
-rw-rw-r-- 1 belarus belarus 216 May 27 00:10 print.hpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano include/print.hpp
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- Configuring done (0.0s)
CMake Error in CMakeLists.txt:
  Found relative path while evaluating include directories of "print":

    "include"



-- Generating done (0.0s)
CMake Generate step failed.  Build files cannot be regenerated correctly.
gmake: *** [Makefile:228: cmake_check_build_system] Error 1
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat CMakeLists.txt
cmake_minimum_required(VERSION 3.4)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

option(BUILD_EXAMPLES "Build examples" OFF)
option(BUILD_TESTS "Build tests" OFF)
option(BUILD_TESTS "Build tests" OFF)

project(print)

add_library(print STATIC sources/print.cpp)

target_include_directories(print PUBLIC
  $<BUILD_INTERFACE:include>
  $<INSTALL_INTERFACE:include>
)

if(BUILD_EXAMPLES)
  file(GLOB EXAMPLE_SOURCES "examples/*.cpp")
  foreach(EXAMPLE_SOURCE )
    get_filename_component(EXAMPLE_NAME  NAME_WE)
    add_executable( )
    target_link_libraries( print)
    install(TARGETS 
      RUNTIME DESTINATION bin
    )
  endforeach(EXAMPLE_SOURCE )
endif()

install(TARGETS print
    EXPORT print-config
    ARCHIVE DESTINATION lib
    LIBRARY DESTINATION lib
)

install(DIRECTORY include/ DESTINATION include)
install(EXPORT print-config DESTINATION cmake)


belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build
CMake Error at CMakeLists.txt:1 (make_minimum_required):
  Unknown CMake command "make_minimum_required".


CMake Warning (dev) in CMakeLists.txt:
  No cmake_minimum_required command is present.  A line of code such as

    cmake_minimum_required(VERSION 3.28)

  should be added at the top of the file.  The version specified may be lower
  if you wish to support older CMake versions for this project.  For more
  information run "cmake --help-policy CMP0000".
This warning is for project developers.  Use -Wno-dev to suppress it.

-- Configuring incomplete, errors occurred!
gmake: *** [Makefile:228: cmake_check_build_system] Error 1
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- Configuring done (0.0s)
-- Generating done (0.0s)
-- Build files have been written to: /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build
[ 50%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[100%] Linking CXX static library libprint.a
[100%] Built target print
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test
gmake: *** No rule to make target 'test'.  Stop.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test
gmake: *** No rule to make target 'test'.  Stop.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test
gmake: *** No rule to make target 'test'.  Stop.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test
gmake: *** No rule to make target 'test'.  Stop.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test
gmake: *** No rule to make target 'test'.  Stop.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake -H. -B_build -DBUILD_ESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googlemock/CMakeLists.txt:42 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googletest/CMakeLists.txt:49 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Warning (dev) at third-party/gtest/googletest/cmake/internal_utils.cmake:239 (find_package):
  Policy CMP0148 is not set: The FindPythonInterp and FindPythonLibs modules
  are removed.  Run "cmake --help-policy CMP0148" for policy details.  Use
  the cmake_policy command to set the policy and suppress this warning.

Call Stack (most recent call first):
  third-party/gtest/googletest/CMakeLists.txt:84 (include)
This warning is for project developers.  Use -Wno-dev to suppress it.

-- Found PythonInterp: /usr/bin/python3 (found version "3.12.3") 
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE  
CMake Error at CMakeLists.txt:21 (add_executable):
  Legacy variable expansion in source file "${${PROJECT_NAME}_TEST_SOURCES}"
  expanded to "" in target "check".  This behavior will be removed in a
  future version of CMake.


-- Configuring incomplete, errors occurred!
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ $ cat >> CMakeLists.txt <<EOF

if(BUILD_TESTS)
  enable_testing()
  add_subdirectory(third-party/gtest)
  file(GLOB \${PROJECT_NAME}_TEST_SOURCES tests/*.cpp)
  add_executable(check \${\${PROJECT_NAME}_TEST_SOURCES})
  target_link_libraries(check \${PROJECT_NAME} gtest_main)
  add_test(NAME check COMMAND check)
endif()
EOF
$: command not found
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat >> CMakeLists.txt <<EOF

if(BUILD_TESTS)
  enable_testing()
  add_subdirectory(third-party/gtest)
  file(GLOB \${PROJECT_NAME}_TEST_SOURCES tests/*.cpp)
  add_executable(check \${\${PROJECT_NAME}_TEST_SOURCES})
  target_link_libraries(check \${PROJECT_NAME} gtest_main)
  add_test(NAME check COMMAND check)
endif()
EOF
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test
gmake: *** No rule to make target 'test'.  Stop.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat >> CMakeLists.txt <<EOF

if(BUILD_TESTS)
  enable_testing()
  add_subdirectory(third-party/gtest)
  file(GLOB \${PROJECT_NAME}_TEST_SOURCES tests/*.cpp)
  add_executable(check \${\${PROJECT_NAME}_TEST_SOURCES})
  target_link_libraries(check \${PROJECT_NAME} gtest_main)
  add_test(NAME check COMMAND check)
endif()
EOF
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test
gmake: *** No rule to make target 'test'.  Stop.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake -H. -B_build -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googlemock/CMakeLists.txt:42 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googletest/CMakeLists.txt:49 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Warning (dev) at third-party/gtest/googletest/cmake/internal_utils.cmake:239 (find_package):
  Policy CMP0148 is not set: The FindPythonInterp and FindPythonLibs modules
  are removed.  Run "cmake --help-policy CMP0148" for policy details.  Use
  the cmake_policy command to set the policy and suppress this warning.

Call Stack (most recent call first):
  third-party/gtest/googletest/CMakeLists.txt:84 (include)
This warning is for project developers.  Use -Wno-dev to suppress it.

-- Configuring done (0.0s)
CMake Error at CMakeLists.txt:10 (add_library):
  Cannot find source file:

    /home/belarus/HeinrichBelarus/workspace/projects/lab06sources/print.cpp

  Tried extensions .c .C .c++ .cc .cpp .cxx .cu .mpp .m .M .mm .ixx .cppm
  .ccm .cxxm .c++m .h .hh .h++ .hm .hpp .hxx .in .txx .f .F .for .f77 .f90
  .f95 .f03 .hip .ispc


CMake Error at CMakeLists.txt:10 (add_library):
  No SOURCES given to target: print


CMake Generate step failed.  Build files cannot be regenerated correctly.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake -H. -B_build -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googlemock/CMakeLists.txt:42 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googletest/CMakeLists.txt:49 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Warning (dev) at third-party/gtest/googletest/cmake/internal_utils.cmake:239 (find_package):
  Policy CMP0148 is not set: The FindPythonInterp and FindPythonLibs modules
  are removed.  Run "cmake --help-policy CMP0148" for policy details.  Use
  the cmake_policy command to set the policy and suppress this warning.

Call Stack (most recent call first):
  third-party/gtest/googletest/CMakeLists.txt:84 (include)
This warning is for project developers.  Use -Wno-dev to suppress it.

-- Configuring done (0.0s)
CMake Error at CMakeLists.txt:10 (add_library):
  Cannot find source file:

    /home/belarus/HeinrichBelarus/workspace/projects/lab06sources/print.cpp

  Tried extensions .c .C .c++ .cc .cpp .cxx .cu .mpp .m .M .mm .ixx .cppm
  .ccm .cxxm .c++m .h .hh .h++ .hm .hpp .hxx .in .txx .f .F .for .f77 .f90
  .f95 .f03 .hip .ispc


CMake Error at CMakeLists.txt:10 (add_library):
  No SOURCES given to target: print


CMake Generate step failed.  Build files cannot be regenerated correctly.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ nano CMakeLists.txt
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake -H. -B_build -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googlemock/CMakeLists.txt:42 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googletest/CMakeLists.txt:49 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Warning (dev) at third-party/gtest/googletest/cmake/internal_utils.cmake:239 (find_package):
  Policy CMP0148 is not set: The FindPythonInterp and FindPythonLibs modules
  are removed.  Run "cmake --help-policy CMP0148" for policy details.  Use
  the cmake_policy command to set the policy and suppress this warning.

Call Stack (most recent call first):
  third-party/gtest/googletest/CMakeLists.txt:84 (include)
This warning is for project developers.  Use -Wno-dev to suppress it.

-- Configuring done (0.0s)
-- Generating done (0.0s)
-- Build files have been written to: /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build
[ 16%] Built target print
[ 25%] Building CXX object third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
In file included from /home/belarus/HeinrichBelarus/workspace/projects/lab06/third-party/gtest/googletest/src/gtest-all.cc:42:
/home/belarus/HeinrichBelarus/workspace/projects/lab06/third-party/gtest/googletest/src/gtest-death-test.cc: In function ‘bool testing::internal::StackGrowsDown()’:
/home/belarus/HeinrichBelarus/workspace/projects/lab06/third-party/gtest/googletest/src/gtest-death-test.cc:1224:24: error: ‘dummy’ may be used uninitialized [-Werror=maybe-uninitialized]
 1224 |   StackLowerThanAddress(&dummy, &result);
      |   ~~~~~~~~~~~~~~~~~~~~~^~~~~~~~~~~~~~~~~
/home/belarus/HeinrichBelarus/workspace/projects/lab06/third-party/gtest/googletest/src/gtest-death-test.cc:1214:13: note: by argument 1 of type ‘const void*’ to ‘void testing::internal::StackLowerThanAddress(const void*, bool*)’ declared here
 1214 | static void StackLowerThanAddress(const void* ptr, bool* result) {
      |             ^~~~~~~~~~~~~~~~~~~~~
/home/belarus/HeinrichBelarus/workspace/projects/lab06/third-party/gtest/googletest/src/gtest-death-test.cc:1222:7: note: ‘dummy’ declared here
 1222 |   int dummy;
      |       ^~~~~
cc1plus: all warnings being treated as errors
gmake[2]: *** [third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/build.make:76: third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/src/gtest-all.cc.o] Error 1
gmake[1]: *** [CMakeFiles/Makefile2:245: third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/all] Error 2
gmake: *** [Makefile:146: all] Error 2
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test
Running tests...
Test project /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build
    Start 1: check
Could not find executable /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
Looked in the following places:
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Release/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Release/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Debug/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Debug/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/MinSizeRel/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/MinSizeRel/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/RelWithDebInfo/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/RelWithDebInfo/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Deployment/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Deployment/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Development/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Development/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Release/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Release/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Debug/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Debug/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/MinSizeRel/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/MinSizeRel/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/RelWithDebInfo/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/RelWithDebInfo/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Deployment/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Deployment/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Development/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Development/check
Unable to find executable: /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
1/1 Test #1: check ............................***Not Run   0.00 sec

0% tests passed, 1 tests failed out of 1

Total Test time (real) =   0.00 sec

The following tests FAILED:
	  1 - check (Not Run)
Errors while running CTest
Output from these tests are in: /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Testing/Temporary/LastTest.log
Use "--rerun-failed --output-on-failure" to re-run the failed cases verbosely.
gmake: *** [Makefile:71: test] Error 8
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ _build/check
bash: _build/check: No such file or directory
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cmake --build _build --target test -- ARGS=--verbose
Running tests...
UpdateCTestConfiguration  from :/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/DartConfiguration.tcl
UpdateCTestConfiguration  from :/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/DartConfiguration.tcl
Test project /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build
Constructing a list of tests
Done constructing a list of tests
Updating test list for fixtures
Added 0 tests to meet fixture requirements
Checking test dependency graph...
Checking test dependency graph end
test 1
    Start 1: check
Could not find executable /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
Looked in the following places:
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Release/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Release/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Debug/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Debug/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/MinSizeRel/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/MinSizeRel/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/RelWithDebInfo/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/RelWithDebInfo/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Deployment/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Deployment/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Development/check
/home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Development/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Release/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Release/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Debug/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Debug/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/MinSizeRel/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/MinSizeRel/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/RelWithDebInfo/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/RelWithDebInfo/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Deployment/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Deployment/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Development/check
home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Development/check

1: Test command: 
1: Working Directory: /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build
Unable to find executable: /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/check
1/1 Test #1: check ............................***Not Run   0.00 sec

0% tests passed, 1 tests failed out of 1

Total Test time (real) =   0.00 sec

The following tests FAILED:
	  1 - check (Not Run)
Errors while running CTest
Output from these tests are in: /home/belarus/HeinrichBelarus/workspace/projects/lab06/_build/Testing/Temporary/LastTest.log
Use "--rerun-failed --output-on-failure" to re-run the failed cases verbosely.
gmake: *** [Makefile:71: test] Error 8
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ gsed -i 's/lab04/lab06/g' README.md
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ gsed -i 's/\(DCMAKE_INSTALL_PREFIX=_install\)/\1 -DBUILD_TESTS=ON/' .travis.yml
sed: can't read .travis.yml: No such file or directory
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat > .travis.yml <<EOF
language: cpp

script:
- cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
- cmake --build _build
- cmake --build _build --target install
EOF
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ cat .travis.yml
language: cpp

script:
- cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
- cmake --build _build
- cmake --build _build --target install
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ gsed -i 's/\(DCMAKE_INSTALL_PREFIX=_install\)/\1 -DBUILD_TESTS=ON/' .travis.yml
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ gsed -i '/cmake --build _build --target install/a\
- cmake --build _build --target test -- ARGS=--verbose
' .travis.yml
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ travis lint

  ________                                 __
 /        |                               /  |
 ########/ ______    ______    __     __  ##/    _______
    ## |  /      \  /      \  /  \   /  | /  |  /       |
    ## | /######  | ######  | ##  \ /##/  ## | /#######/
    ## | ## |  ##/  /    ## |  ##  /##/   ## | ##      \
    ## | ## |      /####### |   ## ##/    ## |  ######  |
    ## | ## |      ##    ## |    ###/     ## | /     ##/
    ##/  ##/        #######/      #/      ##/  #######/

    TRajectory Analyzer and VISualizer  -  Open-source free software under GNU GPL v3

    Copyright (c) Martin Brehm      (2009-2022), University of Halle (Saale)
                  Martin Thomas     (2012-2022)
                  Sascha Gehrke     (2016-2022), University of Bonn
                  Barbara Kirchner  (2009-2022), University of Bonn

    http://www.travis-analyzer.de

    Please cite: J. Chem. Phys. 2020, 152 (16), 164105.         (DOI 10.1063/5.0005078 )
                 J. Chem. Inf. Model. 2011, 51 (8), 2007-2023.  (DOI 10.1021/ci200217w )

    There is absolutely no warranty on any results obtained from TRAVIS.

 #  Running on Roblox at Tue May 27 00:51:13 2025 (PID 8295)
 #  Running in /home/belarus/HeinrichBelarus/workspace/projects/lab06
 #  Version: Jul 29 2022, built at Jan 14 2023, 12:32:45, compiler "12.2.0", GCC 12.2.0
 #  Target platform: Linux, __cplusplus=201703L, Compile flags: NEW_CHARGEVAR DEBUG_ARRAYS 
 #  Compiled with OpenMP, but USE_OMP not switched on in "config.h"!
 #  Machine: x86_64, char=1b, int=4b, long=8b, addr=8b, 0xA0B0C0D0=D0,C0,B0,A0.
 #  Home: /home/belarus,  Executable: /usr/bin/travis
 #  Input from terminal,  Output to terminal

    >>> Please use a color scheme with dark background or specify "-nocolor"! <<<

    Loading configuration from /home/belarus/.travis.conf ...

Unknown parameter: "lint".

    List of supported command line options:

      -p <file>       Load position data from specified trajectory file.
                      Format may be *.xyz, *.pdb, *.lmp (LAMMPS), HISTORY (DLPOLY), POSCAR/XDATCAR (VASP),
                                    *.gro, *.dcd, or *.prmtop/*.mdcrd (Amber).
                      The bqb format (*.bqb, *.btr, *.emp, *.blist) as well as *.voronoi are also supported.
      -vel <file>     Read atom velocities from a file in addition to the position trajectory.
                      Currently, only .xyz format is supported for velocity data.
      -i <file>       Read input from specified text file.
      -c <file>       Read and execute control file (experimental).
      cubetool        Execute the CubeTool for modifying Gaussian Cube files.
      -sankey <file>  Create Sankey diagrams (file name is optional).
      -ramanfrompola  Compute Raman spectra from existing polarizability time series.
      (de-)compress   Start built-in bqbtool (compress trajectories to BQB format).
      check           Check BQB file integrity.

      -config <file>  Load the specified configuration file.
      -stream         Treat input trajectory as a stream (e.g. named pipe): No fseek, etc.
      -showconf       Show a tree structure of the configuration file.
      -writeconf      Write the default configuration file, including all defines values.

      -verbose        Show detailed information about what's going on.
      -nocolor        Execute TRAVIS in monochrome mode (suitable for white background).
      -dimcolor       Use dim instead of bright colors.

      -credits        Display a list of persons who contributed to TRAVIS.
      -help, -?       Shows this help.

    If only one argument is specified, it is assumed to be the name of a trajectory file.
    If no argument is specified at all, TRAVIS asks for the trajectory file to open.

    Note: To show a list of all persons who contributed to TRAVIS,
          please add "-credits" to your command line arguments, or set the
          variable "SHOWCREDITS" to "TRUE" in your travis.conf file.

    Source code from other projects used in TRAVIS:
      - lmfit     from Joachim Wuttke
      - kiss_fft  from Mark Borgerding
      - voro++    from Chris Rycroft

    http://www.travis-analyzer.de

    Please cite all of the following articles for the analyses you have used:

  * For TRAVIS in general:

    "TRAVIS - A Free Analyzer for Trajectories from Molecular Simulation",
    M. Brehm, M. Thomas, S. Gehrke, B. Kirchner; J. Chem. Phys. 2020, 152 (16), 164105.   (DOI 10.1063/5.0005078 )

    "TRAVIS - A Free Analyzer and Visualizer for Monte Carlo and Molecular Dynamics Trajectories",
    M. Brehm, B. Kirchner; J. Chem. Inf. Model. 2011, 51 (8), pp 2007-2023.   (DOI 10.1021/ci200217w )

*** The End ***

belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git add *
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git add tests
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git add -p
No changes.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git commit -m"added tests"
[main 53755d2] added tests
 106 files changed, 4708 insertions(+), 113 deletions(-)
 create mode 100644 _build/CMakeFiles/CMakeDirectoryInformation.cmake
 create mode 100644 _build/CMakeFiles/Export/272ceadb8458515b2ae4b5630a6029cc/print-config-noconfig.cmake
 create mode 100644 _build/CMakeFiles/Export/272ceadb8458515b2ae4b5630a6029cc/print-config.cmake
 create mode 100644 _build/CMakeFiles/Makefile.cmake
 create mode 100644 _build/CMakeFiles/Makefile2
 create mode 100644 _build/CMakeFiles/Progress/11
 create mode 100644 _build/CMakeFiles/Progress/12
 create mode 100644 _build/CMakeFiles/Progress/7
 create mode 100644 _build/CMakeFiles/Progress/count.txt
 create mode 100644 _build/CMakeFiles/TargetDirectories.txt
 create mode 100644 _build/CMakeFiles/check.dir/DependInfo.cmake
 create mode 100644 _build/CMakeFiles/check.dir/build.make
 create mode 100644 _build/CMakeFiles/check.dir/cmake_clean.cmake
 create mode 100644 _build/CMakeFiles/check.dir/compiler_depend.make
 create mode 100644 _build/CMakeFiles/check.dir/compiler_depend.ts
 create mode 100644 _build/CMakeFiles/check.dir/depend.make
 create mode 100644 _build/CMakeFiles/check.dir/flags.make
 create mode 100644 _build/CMakeFiles/check.dir/link.txt
 create mode 100644 _build/CMakeFiles/check.dir/progress.make
 create mode 100644 _build/CMakeFiles/print.dir/DependInfo.cmake
 create mode 100644 _build/CMakeFiles/print.dir/build.make
 create mode 100644 _build/CMakeFiles/print.dir/cmake_clean.cmake
 create mode 100644 _build/CMakeFiles/print.dir/cmake_clean_target.cmake
 create mode 100644 _build/CMakeFiles/print.dir/compiler_depend.internal
 create mode 100644 _build/CMakeFiles/print.dir/compiler_depend.make
 create mode 100644 _build/CMakeFiles/print.dir/compiler_depend.ts
 create mode 100644 _build/CMakeFiles/print.dir/depend.make
 create mode 100644 _build/CMakeFiles/print.dir/flags.make
 create mode 100644 _build/CMakeFiles/print.dir/link.txt
 create mode 100644 _build/CMakeFiles/print.dir/progress.make
 create mode 100644 _build/CMakeFiles/print.dir/sources/print.cpp.o
 create mode 100644 _build/CMakeFiles/print.dir/sources/print.cpp.o.d
 create mode 100644 _build/CMakeFiles/progress.marks
 create mode 100644 _build/CTestTestfile.cmake
 create mode 100644 _build/Makefile
 create mode 100644 _build/Testing/Temporary/CTestCostData.txt
 create mode 100644 _build/Testing/Temporary/LastTest.log
 create mode 100644 _build/Testing/Temporary/LastTestsFailed.log
 create mode 100644 _build/cmake_install.cmake
 create mode 100644 _build/libprint.a
 create mode 100644 _build/third-party/gtest/CMakeFiles/CMakeDirectoryInformation.cmake
 create mode 100644 _build/third-party/gtest/CMakeFiles/progress.marks
 create mode 100644 _build/third-party/gtest/CTestTestfile.cmake
 create mode 100644 _build/third-party/gtest/Makefile
 create mode 100644 _build/third-party/gtest/cmake_install.cmake
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/CMakeDirectoryInformation.cmake
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/DependInfo.cmake
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/build.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/cmake_clean.cmake
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/cmake_clean_target.cmake
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/compiler_depend.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/compiler_depend.ts
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/depend.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/flags.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/link.txt
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock.dir/progress.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/DependInfo.cmake
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/build.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/cmake_clean.cmake
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/cmake_clean_target.cmake
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/compiler_depend.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/compiler_depend.ts
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/depend.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/flags.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/link.txt
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/progress.make
 create mode 100644 _build/third-party/gtest/googlemock/CMakeFiles/progress.marks
 create mode 100644 _build/third-party/gtest/googlemock/CTestTestfile.cmake
 create mode 100644 _build/third-party/gtest/googlemock/Makefile
 create mode 100644 _build/third-party/gtest/googlemock/cmake_install.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/CMakeDirectoryInformation.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/Export/0c08b8e77dd885bfe55a19a9659d9fc1/GTestTargets-noconfig.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/Export/0c08b8e77dd885bfe55a19a9659d9fc1/GTestTargets.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/DependInfo.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/build.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/cmake_clean.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/cmake_clean_target.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/compiler_depend.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/compiler_depend.ts
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/depend.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/flags.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/link.txt
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/progress.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/src/gtest-all.cc.o.d
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/DependInfo.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/build.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/cmake_clean.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/cmake_clean_target.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/compiler_depend.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/compiler_depend.ts
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/depend.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/flags.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/link.txt
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/gtest_main.dir/progress.make
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CMakeFiles/progress.marks
 create mode 100644 _build/third-party/gtest/googlemock/gtest/CTestTestfile.cmake
 create mode 100644 _build/third-party/gtest/googlemock/gtest/Makefile
 create mode 100644 _build/third-party/gtest/googlemock/gtest/cmake_install.cmake
 create mode 100644 examples/example1.cpp
 create mode 100644 examples/example2.cpp
 create mode 100644 input.txt
 create mode 100644 travis.log
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git push origin master
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/HeinrichBelarus/lab06'
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git push origin main
Username for 'https://github.com': HeinrichBelarus
Password for 'https://HeinrichBelarus@github.com': 
To https://github.com/HeinrichBelarus/lab06
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/HeinrichBelarus/lab06'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git pull origin main
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (4/4), 1.50 KiB | 1.50 MiB/s, done.
From https://github.com/HeinrichBelarus/lab06
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git branch
* main
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git remote show origin
* remote origin
  Fetch URL: https://github.com/HeinrichBelarus/lab06
  Push  URL: https://github.com/HeinrichBelarus/lab06
  HEAD branch: main
  Remote branch:
    main tracked
  Local ref configured for 'git push':
    main pushes to main (local out of date)
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git branch
* main
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ git push -f origin main
Username for 'https://github.com': HeinrichBelarus
Password for 'https://HeinrichBelarus@github.com': 
Enumerating objects: 171, done.
Counting objects: 100% (171/171), done.
Delta compression using up to 4 threads
Compressing objects: 100% (141/141), done.
Writing objects: 100% (171/171), 68.64 KiB | 7.63 MiB/s, done.
Total 171 (delta 50), reused 4 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (50/50), done.
To https://github.com/HeinrichBelarus/lab06
 + 52f64e4...53755d2 main -> main (forced update)
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ travis login --auto
[Renaming existing File travis.log to #1#travis.log ...OK.]

  ________                                 __
 /        |                               /  |
 ########/ ______    ______    __     __  ##/    _______
    ## |  /      \  /      \  /  \   /  | /  |  /       |
    ## | /######  | ######  | ##  \ /##/  ## | /#######/
    ## | ## |  ##/  /    ## |  ##  /##/   ## | ##      \
    ## | ## |      /####### |   ## ##/    ## |  ######  |
    ## | ## |      ##    ## |    ###/     ## | /     ##/
    ##/  ##/        #######/      #/      ##/  #######/

    TRajectory Analyzer and VISualizer  -  Open-source free software under GNU GPL v3

    Copyright (c) Martin Brehm      (2009-2022), University of Halle (Saale)
                  Martin Thomas     (2012-2022)
                  Sascha Gehrke     (2016-2022), University of Bonn
                  Barbara Kirchner  (2009-2022), University of Bonn

    http://www.travis-analyzer.de

    Please cite: J. Chem. Phys. 2020, 152 (16), 164105.         (DOI 10.1063/5.0005078 )
                 J. Chem. Inf. Model. 2011, 51 (8), 2007-2023.  (DOI 10.1021/ci200217w )

    There is absolutely no warranty on any results obtained from TRAVIS.

 #  Running on Roblox at Tue May 27 01:09:38 2025 (PID 8963)
 #  Running in /home/belarus/HeinrichBelarus/workspace/projects/lab06
 #  Version: Jul 29 2022, built at Jan 14 2023, 12:32:45, compiler "12.2.0", GCC 12.2.0
 #  Target platform: Linux, __cplusplus=201703L, Compile flags: NEW_CHARGEVAR DEBUG_ARRAYS 
 #  Compiled with OpenMP, but USE_OMP not switched on in "config.h"!
 #  Machine: x86_64, char=1b, int=4b, long=8b, addr=8b, 0xA0B0C0D0=D0,C0,B0,A0.
 #  Home: /home/belarus,  Executable: /usr/bin/travis
 #  Input from terminal,  Output to terminal

    >>> Please use a color scheme with dark background or specify "-nocolor"! <<<

    Loading configuration from /home/belarus/.travis.conf ...

[Renaming existing File input.txt to #1#input.txt ...OK.]
Unknown parameter: "login".

    List of supported command line options:

      -p <file>       Load position data from specified trajectory file.
                      Format may be *.xyz, *.pdb, *.lmp (LAMMPS), HISTORY (DLPOLY), POSCAR/XDATCAR (VASP),
                                    *.gro, *.dcd, or *.prmtop/*.mdcrd (Amber).
                      The bqb format (*.bqb, *.btr, *.emp, *.blist) as well as *.voronoi are also supported.
      -vel <file>     Read atom velocities from a file in addition to the position trajectory.
                      Currently, only .xyz format is supported for velocity data.
      -i <file>       Read input from specified text file.
      -c <file>       Read and execute control file (experimental).
      cubetool        Execute the CubeTool for modifying Gaussian Cube files.
      -sankey <file>  Create Sankey diagrams (file name is optional).
      -ramanfrompola  Compute Raman spectra from existing polarizability time series.
      (de-)compress   Start built-in bqbtool (compress trajectories to BQB format).
      check           Check BQB file integrity.

      -config <file>  Load the specified configuration file.
      -stream         Treat input trajectory as a stream (e.g. named pipe): No fseek, etc.
      -showconf       Show a tree structure of the configuration file.
      -writeconf      Write the default configuration file, including all defines values.

      -verbose        Show detailed information about what's going on.
      -nocolor        Execute TRAVIS in monochrome mode (suitable for white background).
      -dimcolor       Use dim instead of bright colors.

      -credits        Display a list of persons who contributed to TRAVIS.
      -help, -?       Shows this help.

    If only one argument is specified, it is assumed to be the name of a trajectory file.
    If no argument is specified at all, TRAVIS asks for the trajectory file to open.

    Note: To show a list of all persons who contributed to TRAVIS,
          please add "-credits" to your command line arguments, or set the
          variable "SHOWCREDITS" to "TRUE" in your travis.conf file.

    Source code from other projects used in TRAVIS:
      - lmfit     from Joachim Wuttke
      - kiss_fft  from Mark Borgerding
      - voro++    from Chris Rycroft

    http://www.travis-analyzer.de

    Please cite all of the following articles for the analyses you have used:

  * For TRAVIS in general:

    "TRAVIS - A Free Analyzer for Trajectories from Molecular Simulation",
    M. Brehm, M. Thomas, S. Gehrke, B. Kirchner; J. Chem. Phys. 2020, 152 (16), 164105.   (DOI 10.1063/5.0005078 )

    "TRAVIS - A Free Analyzer and Visualizer for Monte Carlo and Molecular Dynamics Trajectories",
    M. Brehm, B. Kirchner; J. Chem. Inf. Model. 2011, 51 (8), pp 2007-2023.   (DOI 10.1021/ci200217w )

*** The End ***

belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ travis enable
[Renaming existing File travis.log to #2#travis.log ...OK.]

  ________                                 __
 /        |                               /  |
 ########/ ______    ______    __     __  ##/    _______
    ## |  /      \  /      \  /  \   /  | /  |  /       |
    ## | /######  | ######  | ##  \ /##/  ## | /#######/
    ## | ## |  ##/  /    ## |  ##  /##/   ## | ##      \
    ## | ## |      /####### |   ## ##/    ## |  ######  |
    ## | ## |      ##    ## |    ###/     ## | /     ##/
    ##/  ##/        #######/      #/      ##/  #######/

    TRajectory Analyzer and VISualizer  -  Open-source free software under GNU GPL v3

    Copyright (c) Martin Brehm      (2009-2022), University of Halle (Saale)
                  Martin Thomas     (2012-2022)
                  Sascha Gehrke     (2016-2022), University of Bonn
                  Barbara Kirchner  (2009-2022), University of Bonn

    http://www.travis-analyzer.de

    Please cite: J. Chem. Phys. 2020, 152 (16), 164105.         (DOI 10.1063/5.0005078 )
                 J. Chem. Inf. Model. 2011, 51 (8), 2007-2023.  (DOI 10.1021/ci200217w )

    There is absolutely no warranty on any results obtained from TRAVIS.

 #  Running on Roblox at Tue May 27 01:09:46 2025 (PID 8978)
 #  Running in /home/belarus/HeinrichBelarus/workspace/projects/lab06
 #  Version: Jul 29 2022, built at Jan 14 2023, 12:32:45, compiler "12.2.0", GCC 12.2.0
 #  Target platform: Linux, __cplusplus=201703L, Compile flags: NEW_CHARGEVAR DEBUG_ARRAYS 
 #  Compiled with OpenMP, but USE_OMP not switched on in "config.h"!
 #  Machine: x86_64, char=1b, int=4b, long=8b, addr=8b, 0xA0B0C0D0=D0,C0,B0,A0.
 #  Home: /home/belarus,  Executable: /usr/bin/travis
 #  Input from terminal,  Output to terminal

    >>> Please use a color scheme with dark background or specify "-nocolor"! <<<

    Loading configuration from /home/belarus/.travis.conf ...

[Renaming existing File input.txt to #2#input.txt ...OK.]
Unknown parameter: "enable".

    List of supported command line options:

      -p <file>       Load position data from specified trajectory file.
                      Format may be *.xyz, *.pdb, *.lmp (LAMMPS), HISTORY (DLPOLY), POSCAR/XDATCAR (VASP),
                                    *.gro, *.dcd, or *.prmtop/*.mdcrd (Amber).
                      The bqb format (*.bqb, *.btr, *.emp, *.blist) as well as *.voronoi are also supported.
      -vel <file>     Read atom velocities from a file in addition to the position trajectory.
                      Currently, only .xyz format is supported for velocity data.
      -i <file>       Read input from specified text file.
      -c <file>       Read and execute control file (experimental).
      cubetool        Execute the CubeTool for modifying Gaussian Cube files.
      -sankey <file>  Create Sankey diagrams (file name is optional).
      -ramanfrompola  Compute Raman spectra from existing polarizability time series.
      (de-)compress   Start built-in bqbtool (compress trajectories to BQB format).
      check           Check BQB file integrity.

      -config <file>  Load the specified configuration file.
      -stream         Treat input trajectory as a stream (e.g. named pipe): No fseek, etc.
      -showconf       Show a tree structure of the configuration file.
      -writeconf      Write the default configuration file, including all defines values.

      -verbose        Show detailed information about what's going on.
      -nocolor        Execute TRAVIS in monochrome mode (suitable for white background).
      -dimcolor       Use dim instead of bright colors.

      -credits        Display a list of persons who contributed to TRAVIS.
      -help, -?       Shows this help.

    If only one argument is specified, it is assumed to be the name of a trajectory file.
    If no argument is specified at all, TRAVIS asks for the trajectory file to open.

    Note: To show a list of all persons who contributed to TRAVIS,
          please add "-credits" to your command line arguments, or set the
          variable "SHOWCREDITS" to "TRUE" in your travis.conf file.

    Source code from other projects used in TRAVIS:
      - lmfit     from Joachim Wuttke
      - kiss_fft  from Mark Borgerding
      - voro++    from Chris Rycroft

    http://www.travis-analyzer.de

    Please cite all of the following articles for the analyses you have used:

  * For TRAVIS in general:

    "TRAVIS - A Free Analyzer for Trajectories from Molecular Simulation",
    M. Brehm, M. Thomas, S. Gehrke, B. Kirchner; J. Chem. Phys. 2020, 152 (16), 164105.   (DOI 10.1063/5.0005078 )

    "TRAVIS - A Free Analyzer and Visualizer for Monte Carlo and Molecular Dynamics Trajectories",
    M. Brehm, B. Kirchner; J. Chem. Inf. Model. 2011, 51 (8), pp 2007-2023.   (DOI 10.1021/ci200217w )

*** The End ***

belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ mkdir artifacts
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ sleep 20s && gnome-screenshot --file artifacts/screenshot.png
Command 'gnome-screenshot' not found, but can be installed with:
sudo apt install gnome-screenshot
belarus@Roblox:~/HeinrichBelarus/workspace/projects/lab06$ popd
~/HeinrichBelarus/workspace
belarus@Roblox:~/HeinrichBelarus/workspace$ export LAB_NUMBER=05
belarus@Roblox:~/HeinrichBelarus/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Cloning into 'tasks/lab06'...
remote: Enumerating objects: 137, done.
remote: Counting objects: 100% (25/25), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 137 (delta 18), reused 16 (delta 16), pack-reused 112 (from 1)
Receiving objects: 100% (137/137), 918.92 KiB | 3.56 MiB/s, done.
Resolving deltas: 100% (60/60), done.
belarus@Roblox:~/HeinrichBelarus/workspace$ mkdir reports/lab${LAB_NUMBER}
belarus@Roblox:~/HeinrichBelarus/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
belarus@Roblox:~/HeinrichBelarus/workspace$ cd reports/lab${LAB_NUMBER}
belarus@Roblox:~/HeinrichBelarus/workspace/reports/lab06$ gist README.md
Error: No such file or directory @ rb_sysopen - /home/belarus/HeinrichBelarus/workspace/reports/lab06/README.md
belarus@Roblox:~/HeinrichBelarus/workspace/reports/lab06$ nano README.md
