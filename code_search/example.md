```python
import towhee

(
    towhee.dc['text'](['return max value', 'def max(a,b): if a>b: return a else return b'])
          .code_search.unixcoder['text', 'embedding']()
          .show()
)
```
