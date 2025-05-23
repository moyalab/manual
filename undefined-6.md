# 연속 그리기

코드를 실행시켜서 실제 동작을 확인하세요.

### 1. 선 그리기

```python
from helloai import *

win = Window('fun-programming')

# 무한 반복 코드 
def loop():
    # 시작점
    x = random(300)
    y = random(300)
    color = (random(256), 0, 0)
    
    win.line((0, 0), (x, y), color, 1)
    win.show()


if __name__ == '__main__':
    run()
```



```python
from helloai import *

win = Window('fun-programming')

# 무한 반복 코드 
def loop():
    # 시작점
    x1 = random(win.width)
    y1 = random(win.height)
    
    # 끝점 
    x2 = random(win.width)
    y2 = random(win.height)
    
    win.line((x1, y1), (x2, y2), Color.RED, 2)
    win.show()


if __name__ == '__main__':
    run()
```



```python
from helloai import *

win = Window('fun-programming')

# 무한 반복 코드 
def loop():
    # 시작점
    x1 = random(win.width)
    y1 = random(win.height)
    
    # 끝점 
    x2 = random(win.width)
    y2 = random(win.height)
    
    color = (random(246), random(246), random(246))
    win.line((x1, y1), (x2, y2), color, 1)
    win.show()


if __name__ == '__main__':
    run()
```



ㄹ







