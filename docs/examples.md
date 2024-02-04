# Usage Examples

## Helper Function

### Comparing Files for Identical Content

```python
from JCompare import print_identical_files
from JCompare import Folder

folder1 = Folder("/path/to/folder")
folder2 = Folder("/path/to/archive.zip")

folder2.extract()

print_identical_files(folder1, folder2)
```

### Finding Similar Files

```python
from JCompare import Folder, CompressionSimilarity, print_similar_files

folder1 = Folder("/path/to/folder1")
folder2 = Folder("/path/to/folder2")

print_similar_files(folder1, folder2, threshold=0.9, comparer=CompressionSimilarity("zstd"))
```

### Comparing Files by Directory Structures

```python
from JCompare import print_identical_files
from JCompare import Folder

folder1 = Folder("/path/to/folder")
folder2 = Folder("/path/to/archive.zip")

print_different_files_by_mcs(folder1, folder2, ignore_directory_names=True)
```
