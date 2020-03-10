# Calculate an average

Example:

```python
from django.db.models import Avg

class Game(models.Model):
    wins = models.IntegerField()
    losses = models.IntegerField()


Game.objects.aggregate(Avg('wins'))

```


# Check if a related object exists
## Sanity check for `RelatedObjectDoesNotExist` error
```python
hasattr(model, 'related_object'):
```
