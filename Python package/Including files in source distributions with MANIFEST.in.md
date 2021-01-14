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
  
recursive-include tests \*  
recursive-exclude \* \_\_pycache\_\_  
recursive-exclude \* \*.py\[co\]  
  
recursive-include docs \*.rst conf.py Makefile make.bat \*.jpg \*.png \*.gif
```

# Read data include in package

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