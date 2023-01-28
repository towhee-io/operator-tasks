```python
import towhee

(
    towhee.dc['text'](["Hello, world."])
          .sentence_embedding.transformers['text', 'vec'](model_name="distilbert-base-cased")
          .show()
)
```
