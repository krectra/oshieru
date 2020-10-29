# Running functions sequentially

Example:

```python
def foo():
    print(f"running foo")

def bar():
    print(f"running bar")

>> [foo(), bar()]
```


# Unique value in two lists

Example:

```python
>> a = range(0, 10)
>> b = range(0, 20)
>> list((set(a) | set(b)) - (set(a) & set(b)))
[10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
```
