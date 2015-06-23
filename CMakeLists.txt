cmake_minimum_required(VERSION 2.8.8)

project(Example)

include(LoadSources.cmake)

include_directories("example/include")

# Load all CPP files recursively from "example/include",
# creating the proper source groups so that files are
# grouped into nested folders in Visual Studio.
load_sources(example_src "example/include")

# Do the same for "example/src"
load_sources(example_src "example/src")

# Now that we've loaded sources into "example_src"
# variable, we can create an executable from it
add_executable(example ${example_src})
