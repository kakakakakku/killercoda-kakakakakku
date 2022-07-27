# step1

Ubuntu のバージョンをを確認します。

`lsb_release -a`{{exec}}

空の Python ファイルを作成します。

`touch hello.py`{{exec}}

Killercoda Editor を開きます。

`hello.py` に以下のコードを実装し、保存します。

```python
import sys

print(sys.version)

print('Hello, World!')
```

Killercoda Terminal に戻り、Python ファイルを実行します。

`python hello.py`{{exec}}
