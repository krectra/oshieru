# Pagination

Example:
```python
class TestView(generics.ListAPIView):
    queryset = Test.objects.all()
    pagination_class = TestPagination

    def get(self, request, *args, **kwargs):
        ...
        serializer = TestSerializer(toto, many=True)
        page = self.paginate_queryset(serializer.data)
        return self.get_paginated_response(page)
```


Example Mixin:

```python
class CustomFilter(CustomMixin):
    queryset = Test.objects.all()
    filter_backends = [DjangoFilterBackend]
    serializer_class = TestSerializer
    pagination_class = CustomPagination
    pagination_class.page_size = 100
```
