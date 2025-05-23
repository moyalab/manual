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



### 3. 벽에 닿으면 튕기기

```python
from helloai import *

win = Window('helloAI')
x_val = 0
y_val = 0
x_delta = 5
y_delta = 5

color = (255, 215, 0)

# 무한 반복 코드 
def loop():
    global x_val, y_val, color 
    global x_delta, y_delta
    
    win.background((0, 0, 0))
        
    win.ellipse((x_val, y_val), 100, 100, color)
    x_val = x_val + x_delta
    y_val = y_val + y_delta

    # 창을 벗어나면
    if x_val > win.width or x_val < 0:
        x_delta = x_delta * -1

    if y_val > win.height or y_val < 0:
        y_delta = y_delta * -1

    win.show()


if __name__ == '__main__':
    run()
```



### 4. 무지개 만들기

```python
from helloai import *

win = Window('helloAI')

# 무한 반복 코드 
def loop():

    thickness = random(5, 20)
    color = (random(256), random(256), random(256) )
    el_width = randrange(win.width - 50, win.width)

    # 창의 아래쪽 벽면의 중간지점을 원의 중점으로 잡는다.
    win.ellipse((win.width/2, win.height),
                el_width,
                el_width,
                outline=color,
                thickness=10)
    win.show()


if __name__ == '__main__':
    run()
```



### 5. 바코드 모양 만들기&#x20;

```python
from helloai import *

win = Window('helloAI')
x_val = 0

def setup():
    win.background((255, 255, 255))

# 무한 반복 코드 
def loop():
    global x_val
    
    barcode_line()
    
    x_val += 2
    if x_val > win.width:
        x_val = 0
        
    win.show()


def barcode_line():
    global x_val
    if (random(100) > 50):
        color = Color.BLACK
    else:
        color = Color.WHITE  

    win.line((x_val, 100), (x_val, 300), color=color, thickness=2)

if __name__ == '__main__':
    run()
```



### 6. 스타필드 (별들의...)

```python
from helloai import *

x = []
y = []
speed = []

win = Window('helloai', (500, 400))
win.background(Color.BLACK)

def setup():
    win.background((0, 0, 0))
    for i in range(100):
        x.append(random_range(0, win.width))
        y.append(random_range(0, win.height))
        speed.append(random_range(1, 5))
    


def loop():
    win.background(Color.BLACK)

    for i in range(100):
        co = int(map(speed[i], 1, 5, 100, 255))
        color = (co, co, co)

        win.ellipse((x[i], y[i]), int(speed[i]), int(speed[i]), fill=color, outline=color)

        x[i] = x[i] - speed[i] / 2
        if x[i] < 0:
           x[i] = win.width
    win.show()


run()
```



### 7. sin 곡선

```python
from helloai import *
import math 

win = Window('helloAI')
deg = 0

def loop():
    global deg
    
    #x축 그림
    win.line((0, win.height/2), (win.width, win.height/2), Color.BLACK)
    
    y = math.sin(math.radians(deg))
    print(y)
    win.point(deg, y*win.height/2 + win.height/2)
    
    deg += 1
    if deg > win.width:
        deg = 0
        win.background(Color.BACKGROUND)
        
    win.show()
    
if __name__ == '__main__':
    run()
```



```python
from helloai import *
import math 

win = Window('helloAI')

a = 0
x = 0
px = 0
py = 0

def loop():
    global a, x, px, py 
    
    y = remap(math.sin(a) * math.sin(a * 2) * math.sin( a * 1.7), (-1, 1), (50, win.height))
    win.line((px, py), (x, y))

    px = x
    py = y

    x = x + 1
    a = a + 0.03
    
    
    if x > win.width:
        x = px = py = 0
        win.background(Color.BACKGROUND)
        
    win.show()
    
    
if __name__ == '__main__':
    run()
```











