![ViginereBreaker logo](https://mauricelambert.github.io/info/python/security/ViginereBreaker_small.png "ViginereBreaker logo")

# ViginereBreaker

## Description

This file implements a viginere breaker.

## Requirements

This package require :
 - python3
 - python3 Standard Library

## Installation
```bash
pip install ViginereBreaker
```

## Usages

### Python script

```python
from ViginereBreaker import ViginereBreaker
from codecs import encode

text=encode("""
Llanfairpwllgwyngyllgogerychwyrndrobwllllantysiliogogogoch
antidisestablishmentarianism
counterimmunoelectrophoresis
oesophagogastroduodenoscopy
ethylenediaminetetraacetate
hexadecyltrimethylammonium
diisopropylfluorophosphate
ethylenediaminetetraacetic
uvulopalatopharyngoplasty
great-great-granddaughter
styrene-butadiene-styrene
cholangiopancreatography
tetracyanoquinodimethane
oligodeoxyribonucleotide
phosphatidylethanolamine
proto-industrialization
hypergammaglobulinaemia
politico-administrative
intracerebroventricular
pancreaticoduodenectomy
electro-encephalography
electroencephalographic
polytetrafluoroethylene
lysophosphatidylcholine
first-come-first-served
""", 'rot_13').upper()  # rot_13 -> key="N"

breaker = ViginereBreaker(text, statistics={"E": 11, "A": 9})
print(breaker.breaker())

# {1: [['N']], 2: [['N'], ['N']], 4: [['N'], ['N'], ['N'], ['N']]}
# ViginereBreaker try to find a key with multiple key lengths
# The ciphertext with the key 'N' or 'NN' or 'NNNN' is identical
```

## Example

Using CustomCrypto:
 - [test_viginere_breaker.py](https://github.com/mauricelambert/ViginereBreaker/blob/main/test_viginere_breaker.py)
     - [text.txt](https://github.com/mauricelambert/ViginereBreaker/blob/main/text.txt)
     - [cipher.txt](https://github.com/mauricelambert/ViginereBreaker/blob/main/cipher.txt)

## Links

 - [Github Page](https://github.com/mauricelambert/ViginereBreaker/)
 - [Documentation](https://mauricelambert.github.io/info/python/security/ViginereBreaker.html)
 - [Pypi package](https://pypi.org/project/ViginereBreaker/)

## Licence

Licensed under the [GPL, version 3](https://www.gnu.org/licenses/).