```python
import towhee

towhee.dc['smiles'](['Cc1ccc(cc1)S(=O)(=O)N']) \
  .molecular_fingerprinting['smiles', 'fingerprint']() \
  .show()
```
