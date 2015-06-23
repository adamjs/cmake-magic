# Handy CMake Scripts

This is my dumping ground for handy CMake snippets.

## LoadSources.cmake - Load Sources Recursively

This script recursively loads all CPP (.h, .cc, .cpp) source files from a certain folder
and creates the necessary `source_groups` so that directory structure is maintained 
within Visual Studio's Solution Explorer.

### Usage:

`load_sources(src_list, "src_path")`
 * `src_list`: [out] Variable to store the resulting list of source paths. All results will be appended to the end of the list if it already exists.
 * `"src_path"`: String containing the directory path to recursively search for source files in.
 
### Example:
 
Look at `CMakeLists.txt` for a full example of use.
