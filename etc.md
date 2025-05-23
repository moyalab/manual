# 기타 기능

### 1. 10% 확률로 발생하는 이벤트&#x20;

10% 확률로 이벤트를 발생시키는 방법을 생각해봅시다. 0부터 9까지 숫자를 랜덤으로 뽑아서, 뽑은 숫자가 0일 경우는 확률이 10%가 됩니다. 뽑은 숫자가 0일 경우, 색상을 바꾸면 됩니다.

```python
from helloai import *

win = Window('helloAI')
x_val = 0
color = (255, 215, 0)

# 무한 반복 코드 
def loop():
    global x_val, color 

    win.background((0, 0, 0))
    num = random(10)
    if num == 0:
        color = (random(256), random(256), random(256))
    
    win.ellipse((x_val, win.height/2), 100, 100, color)
    x_val = x_val + 5

    # 창을 벗어나는지 확인 
    if x_val > win.width :
        x_val = 0
    
    win.show()


if __name__ == '__main__':
    run()
```



### 2. Perlin 노이즈&#x20;

랜덤과 다른 노이즈를 생성하는 알고리즘인 Perlin을 이용하는 예제이다.

```python
from helloai import *

win = Window('helloAI')
xoff = 0
yoff = 0

def loop():
    global xoff, yoff
    
    win.background(Color.BACKGROUND)
    
    xn = noise(xoff) * win.width
    yn = noise(yoff) * win.height
    
    win.ellipse((xn, yn), 24, 24, Color.BLACK)
    win.show()
    xoff += 0.02
    yoff += 0.04
    

if __name__ == '__main__':
    run()
```
