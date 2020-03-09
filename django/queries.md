# Calculate an average

Example:

```python
from django.db.models import Avg

class Game(models.Model):
    wins = models.IntegerField()
    losses = models.IntegerField()


Game.objects.aggregate(Avg('wins'))

```
