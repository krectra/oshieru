# Creating field subclass

Example:

```python
from django.db import models

class NameField(models.CharField):

    description = "Name field"

    def __init__(self, *args, **kwargs):
        kwargs['max_length'] = 150
        super().__init__(*args, **kwargs)


class User(models.Model):
    name = NameField()
```
