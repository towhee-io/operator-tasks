```python
import towhee

towhee.glob['path']('./towhee.jpg') \
      .image_decode['path', 'img']() \
      .image_embedding.timm['img', 'vec'](model_name='resnet50') \
      .select['img', 'vec']() \
      .show()
```
