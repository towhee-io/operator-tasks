```python
from towhee.dc2 import pipe, ops

p = (
    pipe.inputs('vec')
    .map('vec', (), ops.ann_insert.milvus_client(host='127.0.0.1', port='19530', collection_name='test_collection'))
    .output()
    )
p(vec)
```
