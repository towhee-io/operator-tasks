```python
from towhee.dc2 import pipe, ops, DataCollection

p = (
    pipe.input('question')
        .map('question', 'answer', 
             ops.chatbot.openai(api_key=OPENAI_API_KEY))
        .output('question', 'answer')
)

DataCollection(p('Who are you?')).show()
```
