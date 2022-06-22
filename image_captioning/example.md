```python
import towhee

towhee.glob['path']('./animals.jpg') \
      .image_decode['path', 'img']() \
      .image_captioning.blip['img', 'text'](model_name='blip_base') \
      .select['img', 'text']() \
      .show()
```
