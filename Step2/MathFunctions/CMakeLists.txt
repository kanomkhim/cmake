# TODO 14: Remove mysqrt.cxx from the list of sources

# TODO 1: Add a library called MathFunctions with sources MathFunctions.cxx
# and mysqrt.cxx
# Hint: You will need the add_library command
# add_library(MathFunctions MathFunctions.cxx mysqrt.cxx)
add_library(MathFunctions MathFunctions.cxx)

# TODO 7: Create a variable USE_MYMATH using option and set default to ON
option(USE_MYMATH "Use tutorial provided math implementation" ON)

# TODO 8: If USE_MYMATH is ON, use target_compile_definitions to pass
# USE_MYMATH as a precompiled definition to our source files
if (USE_MYMATH)
  target_compile_definitions(MathFunctions PRIVATE "USE_MYMATH")
# endif()

# TODO 12: When USE_MYMATH is ON, add a library for SqrtLibrary with
# source mysqrt.cxx
    add_library(SqrtLibrary STATIC mysqrt.cxx)

# TODO 13: When USE_MYMATH is ON, link SqrtLibrary to the MathFunctions Library
    target_link_libraries(MathFunctions PRIVATE SqrtLibrary)

endif()
