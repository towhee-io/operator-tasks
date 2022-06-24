```python
import towhee

(
    towhee.glob['path']('test.wav')
          .audio_decode.ffmpeg['path', 'frames']()
          .runas_op['frames', 'frames'](func=lambda x:[y[0] for y in x])
          .audio_classification.panns['frames', ('labels', 'scores', 'vec')]()
          .show() 
)
```
