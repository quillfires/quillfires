### Hi there 👋

I'm **Ali Fayaz**, a developer from the Maldives building open source Python tools.

---

## 📦 Open Source Projects

### [bml-connect-python](https://github.com/quillfires/bml-connect-python)

[![PyPI version](https://badge.fury.io/py/bml-connect-python.svg)](https://badge.fury.io/py/bml-connect-python)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/bml-connect-python?color=orange&label=PIP%20Installs)](https://pypi.python.org/pypi/bml-connect-python/)
[![Python Support](https://img.shields.io/pypi/pyversions/bml-connect-python.svg)](https://pypi.org/project/bml-connect-python/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Python SDK for the **Bank of Maldives Connect API**, the only Python library for BML Connect payments.

- ✅ Sync and async support (Django, Flask, FastAPI, Sanic)
- ✅ Create, retrieve, and cancel transactions
- ✅ Webhook signature verification
- ✅ Typed response models and structured error handling

```bash
pip install bml-connect-python
```

```python
from bml_connect import BMLConnect, Environment

with BMLConnect(api_key="...", app_id="...", environment=Environment.SANDBOX) as client:
    transaction = client.transactions.create_transaction({
        "amount": 1500,
        "currency": "MVR",
        "provider": "alipay",
        "redirectUrl": "https://yourstore.com/success",
    })
    print(transaction.url)
```

---

### [SecurePasswordGenerator](https://github.com/quillfires/SecurePasswordGenerator)

[![PyPI version](https://img.shields.io/pypi/v/securepasswordgenerator.svg?color=4CBB17)](https://pypi.org/project/securepasswordgenerator/)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/securepasswordgenerator?color=orange&label=PIP%20Installs)](https://pypi.org/project/securepasswordgenerator/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A Python tool for generating cryptographically secure passwords, available as both a Python module and a CLI utility.

- ✅ Predefined strength presets: `decent`, `strong`, `fort_knox`
- ✅ WEP/WPA key generation (64, 128, 152, 256-bit)
- ✅ Fully configurable: length, charset, uppercase, numbers, special chars
- ✅ Command line interface included

```bash
pip install securepasswordgenerator
```

```python
import securepasswordgenerator as spw

spw.generate(length=16, use_lower_case=True, use_upper_case=True, use_numbers=True, use_special=True)
# or use presets:
spw.strong()
spw.fort_knox()
```

```bash
# CLI usage
securepasswordgenerator 16 -l -u -n -s
securepasswordgenerator -p fort_knox
```

---

## 📫 Contact

- Email: fayaz.quill@gmail.com
- PyPI: [bml-connect-python](https://pypi.org/project/bml-connect-python/) · [securepasswordgenerator](https://pypi.org/project/securepasswordgenerator/)

---

[![contributions](contributions.svg)](https://github.com/quillfires)

---

<p align="center">
  <a href="https://github.com/quillfires"><img src="https://komarev.com/ghpvc/?username=quillfires&label=Profile%20views&color=0e75b6&style=flat" alt="quillfires" /></a>
</p>
