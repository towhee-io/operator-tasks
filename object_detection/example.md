```python
import towhee

towhee.glob['path']('./test.png') \
	.image_decode['path','img']() \
	.object_detection.yolov5['img', ('box', 'class', 'score')]() \
	.image_crop[('img', 'box'), 'object'](clamp = True) \
	.select['img','object']() \
	.show()
```
