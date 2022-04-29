```python
import towhee

towhee.glob['path']('./alan_turing.jpeg') \
  .image_decode['path', 'img']() \
  .face_embedding.deepface['img', 'vec']() \
  .select['img','vec']() \
  .show()
```
