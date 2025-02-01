---
icon: python
description: 비트블록용 파이썬 라이브러리
---

# pyblebb

### 설치

```powershell
pip install pyblebb
```



### 샘플 코드

```python
from bitblock import *

# MAC 주소가 "48:27:E2:38:39:81" 의 경우 
# "39:81"만 입력하거나,  
# "48:27:E2:38:39:81" 전체를 입력 가능) 
# address = '48:27:E2:38:39:81
address = '39:81' 

board = Bitblock(address)
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



### MAC 주소 확인

비트블록 보드의 MAC 주소를 확인하는 방법은 스마트폰 앱을 이용하면 편리하다. &#x20;

<figure><img src="../.gitbook/assets/mac_01.png" alt=""><figcaption></figcaption></figure>

nRF Connect for Mobile 앱을 설치하고, 실행한다.

<figure><img src="../.gitbook/assets/nrf_01.png" alt=""><figcaption></figcaption></figure>

비트블록 보드는 "BitBlock MINI"라는 이름으로 검색된다. 그 아래에 있는 "64:E8:33:6D:86:29" 가 MAC 주소이다. 이 MAC 주소를 사용해서 파이썬 코드에서 비트블록에 연결한다.&#x20;

