```python
import towhee

towhee.dc['text'](["Hello, world."])
      .machine_translation.opus_mt['text', 'vec'](model_name="opus-mt-en-zh")
      .show()
```
