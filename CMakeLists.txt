# Minimum required version of CMake
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
IF(COMMAND CMAKE_POLICY)
  CMAKE_POLICY(SET CMP0003 NEW)
ENDIF(COMMAND CMAKE_POLICY)

# Set CMake project name
PROJECT(SPOOLES)

# Identify CMake directory
set(SPOOLES_CMAKE_DIR "${SPOOLES_SOURCE_DIR}/CMake")
if(SPOOLES_IS_SUBBUILD)
  set(CMAKE_MODULE_PATH "${CMAKE_MODULE_PATH};${SPOOLES_CMAKE_DIR}")
else(SPOOLES_IS_SUBBUILD)
  set(CMAKE_MODULE_PATH "${SPOOLES_CMAKE_DIR};${CMAKE_MODULE_PATH}")
endif(SPOOLES_IS_SUBBUILD)

if("${SPOOLES_ENABLE_TESTING}" STREQUAL "")
  set(SPOOLES_ENABLE_TESTING ON CACHE BOOL "Enable SPOOLES testing")
else("${SPOOLES_ENABLE_TESTING}" STREQUAL "")
  set(SPOOLES_ENABLE_TESTING ${SPOOLES_ENABLE_TESTING} CACHE BOOL "SPOOLES testing")
endif("${SPOOLES_ENABLE_TESTING}" STREQUAL "")

if(NOT M_LIBRARY)
  include(CheckLibraryExists)
  include(ResolveCompilerPaths)
  CHECK_LIBRARY_EXISTS(m cos "" HAVE_M_LIBRARY)
  if(HAVE_M_LIBRARY)
    RESOLVE_LIBRARIES(M_LIBRARY "-lm")
  endif(HAVE_M_LIBRARY)
endif(NOT M_LIBRARY)

# search for 32/64 bit pthread library on windows
# assumed that pthread binary placed on the same
# level with spooles directory
if(MSVC)
  if( CMAKE_SIZEOF_VOID_P EQUAL 8 )
    FILE(GLOB pthread_DIR
         "../pthreads-w64-*[0-9]-*[0-9]-*[0-9]"
    )
  else( CMAKE_SIZEOF_VOID_P EQUAL 8 )
    FILE(GLOB pthread_DIR
         "../pthreads-w32-*[0-9]-*[0-9]-*[0-9]"
    )
  endif( CMAKE_SIZEOF_VOID_P EQUAL 8 )
  FIND_PATH(pthread_INCLUDE_DIR pthread.h
      HINTS ${pthread_DIR}/Pre-built.2/include
  )
  INCLUDE_DIRECTORIES( ${pthread_INCLUDE_DIR} )
endif(MSVC)


add_subdirectory(src)

if(SPOOLES_ENABLE_TESTING)
  ENABLE_TESTING()
  add_subdirectory(src/A2/tests)
endif(SPOOLES_ENABLE_TESTING)

# Local Variables:
# tab-width: 8
# mode: cmake
# indent-tabs-mode: t
# End:
# ex: shiftwidth=2 tabstop=8
