
Define a type Numeric

```python
from typing import Sequence


import numpy as np
import pandas as pd
import pandas.api.types as pdt

import visions
from visions.relations import IdentityRelation, TypeRelation
from visions.typesets.typeset import get_type_from_path



class Numeric(visions.VisionsBaseType):
    @staticmethod
    def get_relations() -> Sequence[TypeRelation]:
        return [IdentityRelation(visions.Generic)]

    @classmethod
    def contains_op(cls, series: pd.Series, state: dict) -> bool:
        return pdt.is_numeric_dtype(series)
```

Detect if column is Numeric

```python
import plotly.express as px
df_stock["GOOG"] in Numeric
df_stock["date"] in Numeric
```

