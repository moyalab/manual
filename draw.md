# 그리기 기능

### 1.이미지 읽어서 표시하기

png 이미지 파일을 읽어서 화면에 표시한다.

```python
from helloai import *

wnd = Window('Retriever')

# 경로와 파일명에 한글이 들어있으면 안된다. 
img = load_image("C:\\Users\\iamto\\Downloads\\Retriever.png")
 
def loop():
    # 이미지 크기 표시 (너비, 높이)
    print(img.size_)
    # 이미지 표시 
    wnd.show(img)

if __name__ == '__main__':
    run()
```

### 2. 선 긋기

```python
from helloai import *

wnd = Window('Retriever')

# 경로와 파일명에 한글이 들어있으면 안된다. 
img = load_image("C:\\Users\\iamto\\Downloads\\Retriever.png")
 
def loop():
    # 이미지 크기 표시 (너비, 높이)
    print(img.size_)

    # 원본 이미지는 변경되지 않기 때문에, 변경된 이미지는 반드시 변수에 저장해서 사용
    img_updated =  img.line((20, 0), (120, 100), (255, 0, 0), 15)

    # 변경된 이미지 표시 
    wnd.show(img_updated)

if __name__ == '__main__':
    run()
```

### 3. 원 그리기&#x20;

```python
from helloai import *

wnd = Window('Retriever')

# 경로와 파일명에 한글이 들어있으면 안된다. 
img = load_image("C:\\Users\\iamto\\Downloads\\Retriever.png")
 
def loop():
    # 이미지 크기(너비, 높이)
    size = img.size_
    # 이미지의 중심 좌표 계산 
    center = (size[0]/2, size[1]/2)

    # ellipse(<타원의 중심>, <원의 폭>, <원의 높이>, <윤곽선의 색상>, <칠하기색상>, <윤곽선두께> )
    img_updated = img.ellipse(center, 100, 100, (255,0,0), (0, 255, 0), 3)

    # 변경된 이미지 표시 
    wnd.show(img_updated)

if __name__ == '__main__':
    run()
```

### 4. 사각형 그리기&#x20;

```python
from helloai import *

wnd = Window('Retriever')

# 경로와 파일명에 한글이 들어있으면 안된다. 
img = load_image("C:\\Users\\iamto\\Downloads\\Retriever.png")
 
def loop():

    # rectangle(<시작좌표>, <끝좌표>, <윤곽선 색상>, <칠하기색상>, <윤곽선 두께>)
    img_updated = img.rectangle((100, 100), (300, 300), (255, 0, 0), (255, 255, 0), 5)

    # 변경된 이미지 표시 
    wnd.show(img_updated)

if __name__ == '__main__':
    run()
```

### 5. 텍스트 입력



```python
from helloai import *

wnd = Window('Retriever')

# 경로와 파일명에 한글이 들어있으면 안된다. 
img = load_image("C:\\Users\\iamto\\Downloads\\Retriever.png")
 
def loop():

    # text(<시작좌표>, <표시할 텍스트>, <글자크기>, <색상>)
    img_updated = img.text((100,100), text='리트리버', size=60, color=(255,0,0))

    # 변경된 이미지 표시 
    wnd.show(img_updated)

if __name__ == '__main__':
    run()
```







