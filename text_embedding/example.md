```python
import towhee

(
    towhee.dc['text'](["Hello, world."])
          .text_embedding.transformers['text', 'vec'](model_name="distilbert-base-cased")
          .show()
)
```
