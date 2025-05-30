# 🖱️기본 기능

PC에 연결된 카메라의 영상을 받아서 화면에 표시하는 기능을 작성합니다.

### 1. 코드작성

아래 코드는 HelloAI를 사용하는 뼈대가 되는 코드입니다.   기본적으로 아래 순서를 따릅니다.



1. 카메라 영상을 표시할 윈도우 만들기
2. 카메라 영상 읽어오기
3. (영상 처리 부분)
4. 윈도우에 표시하기&#x20;



```python
# HelloAI의 모든 기능을 임포트한다.
from helloai import *

# 카메라 영상을 표시하기 위한 윈도우를 생성한다.  
# 'wnd'는 윈도우의 이름으로 영문자만 사용해야 한다.
wnd = Window('wnd')

# 카메라 객체를 만든다.
camera = Camera()

# 무한 루프 
def loop():
    # 카메라에서 이미지 읽어오기 
    img = camera.read()
    
    # 이미지를 윈도우에 표시 
    wnd.show(img)

# --------------------------------------------------------------------------
# HelloAI 를 사용하는 코드는 반드시 아랫부분을 포함해야 실행된다. 
# -------------------------------------------------------------------------
if __name__ == '__main__':
    run()
```



코드 실행하고 화면에 이미지가 표시될 때까지 약간의 시간이 필요합니다.



### 2. 종료

HelloAI를 종료하는 가장 좋은 방법은 카메라가 표시되는 화면을 한번 클릭한 후,  키보드의 Esc 키를 누르면 된다.  다만 내부적으로 안전하게 종료되는데 까지  약간의 시간이 걸린다.



또는 코드를 실행한 터미널 창에서 Control + C 키를 눌러서 종료하는 방법도 있다.

