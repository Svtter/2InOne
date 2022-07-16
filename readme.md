# Test multiple package

Could two packages share same folder?
The answer is yes.

1. packagea is in `apps`
2. packageb is in `apps`

And the mainc installed them all,
run [src/main.py](mainc/src/main.py) successfully.

The folder tree is:

```
├── mainc
│   ├── poetry.lock
│   ├── pyproject.toml
│   └── src
│       └── main.py
├── packagea
│   ├── apps
│   │   └── packagea
│   └── pyproject.toml
├── packageb
│   ├── apps
│   │   └── packageb
│   └── pyproject.toml
└── readme.md
```

The `main.py` is:

```python
from apps.packagea.a import printa
from apps.packageb.b import printb


if __name__ == "__main__":
    printa()
    printb()
```
