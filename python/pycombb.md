---
description: 카미봇 동글을 사용해서 보드와 연결하는 경우에 사용하는 비트블록 파이썬 라이브러리
---

# 👓 pycombb

### 설치

```powershell
pip install pycombb
```



### 샘플 코드

파이썬에서 비트블록을 블루투스로 연결하기위해서는 비트블록의 MAC 주소를 알고 있어야 한다. MAC주소를 확인하는 방법은 [MAC 확인방법](mac.md)을 참고하세요.

```python
from bitblock import *

# 카미봇동글이 꽂혀있는 COM포트 번호 
port = 'COM8'

board = Bitblock(port)
ret = board.connect()

rccar = board.rccar_init()

for i in range(10):
    rccar.move_forward(100)
    wait(1000)
    rccar.stop()
    rccar.move_backward(100)
    wait(1000)
    rccar.stop()
```





### 라이브러리 API 문서

pyblebb 라이브러리의 사용방법은 아래 링크를 참고하세요.

{% embed url="https://github.com/devdio/bitblock_tutorial/wiki/0.%ED%8A%9C%ED%86%A0%EB%A6%AC%EC%96%BC" %}
