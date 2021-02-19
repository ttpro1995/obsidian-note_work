[Stackoverflow: How to filter rows in pandas by regex](https://stackoverflow.com/questions/15325182/how-to-filter-rows-in-pandas-by-regex/48884429)


Define function

```
def regex_filter(val):
    if val:
        mo = re.search(r,val)
        if mo:
            return True
        else:
            return False
    else:
        return False
```

dataframe

```
import pandas as pd
import re 

foo = pd.DataFrame({'a' : [1,2,3,4], 'b' : ['hi', 'foo', 'fat', 'cat']})
r = r"fat|cat"
```

Apply

```
df_filtered = foo[foo['b'].apply(regex_filter)]

```