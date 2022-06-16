```python
import towhee

towhee.glob['path']('./towhee.jpg') \
      .image_decode['path', 'img']() \
      .image_text_embedding.clip['img', 'vec'](model_name='clip_vit_b32', modality='image') \
      .select['img', 'vec']() \
      .show()
```
