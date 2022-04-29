```python
import towhee

towhee.glob['path']('./avengers.jpg') \
  .image_decode['path', 'img']() \
  .face_detection.retinaface['img', ('box','score')]()\
  .image_crop[('img', 'box'), 'crop'](clamp = True)\
  .select['img','crop']()\
  .show()
```
