```python
import towhee

(
    towhee.glob['path']('test.wav')
          .audio_decode.ffmpeg['path', 'frames']()
          .runas_op['frames', 'frames'](func=lambda x:[y[0] for y in x])
          .audio_embedding.vggish['frames', 'vecs']()
          .select['path', 'vecs']()
          .show()
)
```
