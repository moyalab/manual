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



레이저 효과&#x20;

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



### 2. 원과 사각형



```python
from helloai import *

win = Window('helloAI')


# 무한 반복 코드 
def loop():
    x = random(win.width)
    y = random(win.height)
    color = (random(256), random(256), random(256))
    win.ellipse((x, y), 100, 100, fill=color)
    win.show()


if __name__ == '__main__':
    run()
```



```python
from helloai import *

win = Window('helloAI')


# 무한 반복 코드 
def loop():
    win.background((0,0,0))

    x = random(win.width)
    y = random(win.height)
    color = (random(256), random(256), random(256))
    win.ellipse((x, y), 100, 100, fill=color)
    win.show()


if __name__ == '__main__':
    run()
```



```python
from helloai import *

win = Window('helloAI')

def setup():
    win.background((0,0,0))

# 무한 반복 코드 
def loop():
    size = 100
    x0 = random(win.width)
    y0 = random(win.height)
    x1 = x0 + size
    y1 = y0 + size
    color = (random(256), random(256), random(256))
    win.rectangle((x0, y0), (x1, y1), fill=color)
    win.show()


if __name__ == '__main__':
    run()
```



랜덤을 사용하지 않는 코드

```python
from helloai import *

win = Window('helloAI')
x_val = 0


# 무한 반복 코드 
def loop():
    global x_val
   
    win.ellipse((x_val, win.height/2), 100, 100, (255, 215, 0))
    x_val = x_val + 5    #    5픽셀씩 증가시킴
    win.show()


if __name__ == '__main__':
    run()
```



```python
from helloai import *

win = Window('helloAI')
x_val = 0


# 무한 반복 코드 
def loop():
    global x_val
   
    win.background((0, 0, 0))
    win.ellipse((x_val, win.height/2), 100, 100, (255, 215, 0))
    x_val = x_val + 5
    win.show()


if __name__ == '__main__':
    run()
```



