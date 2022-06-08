```python
import towhee

(
    towhee.glob['video']('./archery.mp4')
      .video_decode.ffmpeg['video', 'frames']()
      .video_classification.actionclip['frames', ('labels', 'scores')](model_name='clip_vit_b16', topk=5)
      .select['video', 'labels', 'scores']()
      .show(formatter={'video':'video_path'})
)
```
