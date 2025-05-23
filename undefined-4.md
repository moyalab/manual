---
icon: image-polaroid
---

# 사진, 데이터 저장

카메라에서 읽어들인 이미지를 파일로 저장하는 기능이다.

### 1. 카메라를 파일로 저장

화면에 표시된 카메라의 영상을 이미지 파일로 저장한다.

```python
from helloai import *

wnd = Window("wnd")

# 이미지를 저장할 폴더 경로. 폴더는 미리 만든다.
rock = "C:\\Users\\user\\Downloads\\rock"

# 저장될 이미지의 파일명에 번호를 붙이기 위한 변수 
no = 0

# 카메라 객체
camera = Camera()

def loop():
    global no
    # 카메라에서 이미지를 얻어온다.
    img = camera.read()

    # 키보드 's' 키가 눌러지면 
    if is_pressed('s'):
        if img is not None:
            img.save(f"{rock}\\image_{no}.png")
            # 저장된 이미지의 장수를 삽입
            img = img.text((5,5), text=str(no), size=40, color=(255, 0, 0))
            no = no + 1

    # 윈도우에 이미지 표시 
    wnd.show(img)

# ---------------------------------------
# For HelloAI
# ---------------------------------------
if __name__ == "__main__":
    run()
```



### 2. 랜드마크 정보를 csv파일로 저장

인식한 랜드마크 정보를 csv파일로 저장하는 코드를 작성한다.

```python
import csv
from helloai import *

wnd = Window('wnd')

# 카메라 객체 생성 
camera = Camera()

# 손 검출을 위한 객체 생성 
hands = HandsDetector()

# CSV파일로 저장할 객체 생성
file_path = "C:\\Users\\user\\Downloads\\rock\\landmarks.csv"
csv_writer = CSVWriter(file_path)

# 메인 루프 함수
def loop():
    img = camera.read()

    # 손 검출해서 랜드마크 검출 
    img, landmarks = hands.process(img, draw=True)
    
    if len(landmarks) > 0:
        # 랜드마크(다중 리스트)를 1차원 리스트로 만든다. 
        lst = flatten_list(landmarks)
        # 한 행의 데이터를 기록한다. 
        csv_writer.writerow(lst)

    wnd.show(img)

# ---------------------------------------
# For HelloAI
# ---------------------------------------
if __name__ == '__main__':
    run()
```





