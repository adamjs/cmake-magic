# Handy CMake Scripts

This is my dumping ground for handy CMake snippets.

## LoadSources.cmake - Load Sources for Visual Studio

This script recursively loads all CPP (.h, .cc, .cpp) source files from a certain folder
and creates the necessary `source_groups` so that directory structure is maintained 
within Visual Studio's Solution Explorer.

### Why is this useful?

Without this script you'd need to hand-code a `CMakeLists.txt` with a list of every source file __AND__ declare `source_groups` for each folder so that the files are grouped into the proper folders in Visual Studio's Solution Explorer. This gets too tedious for large CMake projects so I decided to automate it.

### Usage:

`load_sources(src_list, "src_path")`
 * `src_list`: [out] Variable to store the resulting list of source paths. All results will be appended to the end of the list if it already exists.
 * `"src_path"`: String containing the directory path to recursively search for source files in.
 
### Example:
 
Look at `CMakeLists.txt` for a full example of use.
