```python
import towhee

(
  towhee.glob['path']('./alan_turing.jpeg')
    .image_decode.cv2['path', 'img']()
    .face_landmark_detection.mobilefacenet['img', 'landmark']()
    .select['img','landmark']()
    .show()
)
```
