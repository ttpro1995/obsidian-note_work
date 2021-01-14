https://packaging.python.org/guides/using-manifest-in/
[[pip]]



# This is MANIFEST.in
example
```
include AUTHORS.rst
include CONTRIBUTING.rst
include HISTORY.rst
include LICENSE
include README.rst

recursive-include tests *
recursive-exclude * __pycache__
recursive-exclude * *.py[co]

recursive-include docs *.rst conf.py Makefile make.bat *.jpg *.png *.gif
```

# Read data include in package
[pkgutil](https://docs.python.org/3/library/pkgutil.html)

```
.
├── package
│   ├── __init__.py
│   ├── templates
│   │   └── temp_file
│   ├── mymodule1.py
│   └── mymodule2.py
├── README.rst
├── MANIFEST.in
└── setup.py

```


```
# within package/mymodule1.py, for example
import pkgutil

data = pkgutil.get_data(__name__, "templates/temp_file")
```

Data is binary format, equivalent to: 

```
d = os.path.dirname(sys.modules[package].__file__)
data = open(os.path.join(d, resource), 'rb').read()
```