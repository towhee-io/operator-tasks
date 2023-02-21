```python
from datetime import datetime
from towhee.dc2 import pipe, ops, DataCollection


example_doc = {
    'title': 'Test Title',
    'author': 'Towhee',
    'content': 'This is an example.',
    'timestamp': datetime.now()
    }

es_insert = (
    pipe.input('doc')
        .map('doc', 'res', ops.elasticsearch.index_client(
            host='localhost', port=9200, index_name='test_index'
        ))
        .output('doc', 'res')
)

res = es_insert(example_doc) # OR: es_insert([example_doc])
DataCollection(res).show() # Optional: display output data
```
