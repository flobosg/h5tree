## h5tree
`h5tree` is a command-line utilitly that prints the tree structure of an HDF5 file, similar to `tree`.
It also displays meta-data, such as the data shape, data type, and the values of attributes.

## Install
Install with `pip install h5tree`, or simply copy the file `bin/h5tree` to a folder in your system `PATH`

## Example output
```bash
>>> h5tree -va data.h5
data.h5  (3 objects, 2 attributes)
│   ├── name  Sam
│   ├── value  105
├── group_1  (3 objects)
│   ├── group_1_sub  (1 object, 1 attribute)
│   │   ├── name  Dan
│   │   └── x  (5, 3), float64
│   ├── x  (5, 3), float64
│   └── y  (5, 3), float64
├── group_2  (2 objects)
│   ├── x  (5, 3), float64
│   └── y  (5, 3), float64
└── x  (5, 5, 3), float64

3 groups, 6 datasets
```

## Usage
```bash
usage: h5tree [-h] [-c] [-v] [-a] [-g] [-L [LEVEL]] [-p [PATTERN]] path [group]

positional arguments:
  path                  filepath
  group                 group path (default: /)

options:
  -h, --help            show this help message and exit
  -c, --color           colored output
  -v, --verbose         verbose output
  -a, --attributes      show attributes
  -g, --groups          only show groups
  -L [LEVEL], --level [LEVEL]
                        maximum number of directories to recurse into
  -p [PATTERN], --pattern [PATTERN]
                        pattern
```
