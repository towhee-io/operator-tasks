```python
import towhee

towhee.dc['vec'](query) \
    .ann_search.milvus['vec', 'result'](collection=collection) \
    .show()
```
