```python
import towhee

towhee.glob['path']('./dog.jpg') \
  .image_decode['path', 'img']() \
  .select['path', 'img']() \
  .show()
```
