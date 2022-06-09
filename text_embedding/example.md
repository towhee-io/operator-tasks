```python
import towhee

towhee.glob['path']('./teddy.jpg') \
      .image_decode['path', 'img']() \
      .image_text_embedding.clip['img', 'vec'](model_name='clip_vit_b32', modality='image') \
      .select['img', 'vec']() \
      .show()

towhee.dc['text'](["A teddybear on a skateboard in Times Square."]) \
      .image_text_embedding.clip['text','vec'](model_name='clip_vit_b32', modality='text') \
      .select['text', 'vec']() \
      .show()
```
