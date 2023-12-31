# seapeapea

C++ to python transpiler

```
usage: seapeapea [-h] [-I INCLUDE] [-o OUTPUT] [-p PREPROCESSED] [-m MAP]
                 [--no-imports] [--qt {pyside6,pyqt6,pyside2,pyqt5}] [--time]
                 src [src ...]

transpiles c++ into python

positional arguments:
  src                   cpp files

options:
  -h, --help            show this help message and exit
  -I INCLUDE, --include INCLUDE
                        includepath
  -o OUTPUT, --output OUTPUT
                        output
  -p PREPROCESSED, --preprocessed PREPROCESSED
                        path to save preprocessed
  -m MAP, --map MAP     save map for side by side
  --no-imports          do not add imports
  --qt {pyside6,pyqt6,pyside2,pyqt5}
                        python qt library
  --time                print time stat
```

# Install
```
pip install seapeapea
```

# About

There are two ways to write c++ transpiler:

1) Hard way: write c++ compiler and preprocessor that can expand all macros and process all templates, it will produce semireadable code that is almost guaranteed to be correct.

2) Easy way: write processor that parses code and makes reasonable assumptions about missing information and produces readable code that is probably correct.

Seapeapea goes the easy way, it produces first iteration of what will become working code after you repair it.