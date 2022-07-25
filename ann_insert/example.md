```python
import towhee

towhee.dc['vec'](your_embeddings) \
    .ann_insert.milvus['vec', 'results'](collection=collection) \
    .show()
```
