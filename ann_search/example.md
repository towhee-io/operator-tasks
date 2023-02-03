```python
from towhee.dc2 import pipe, ops, DataCollection

p = pipe.input('text')  \
    .map('text', 'vec', ops.sentence_embedding.transformers(model_name='all-MiniLM-L12-v2')) \
    .flat_map('vec', 'rows', ops.ann_search.milvus_client(host='127.0.0.1', port='19530', collection_name='text_db2', **{'output_fields': ['text']})) \
    .map('rows', ('id', 'score', 'text'), lambda x: (x[0], x[1], x[2])) \
    .output('id', 'score', 'text')

DataCollection(p('cat')).show()
```
