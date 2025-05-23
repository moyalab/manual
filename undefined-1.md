# 동영상

### 1. 동영상 파일 읽어서 표시

```python
from helloai import *
import os 

win = Window('hello-AI')

video_path = "C:\\Users\\user\\Downloads\\videos\\video.mp4"
video_reader = VideoReader(video_path)

# 비디오 정보 출력
info = video_reader.get_info()
print("Video Info:", info)

def loop():
    # 동영상에서 프레임 한개 읽음
    frame = video_reader.read()

    # 동영상이 끝까지 재생
    if video_reader.end_:
        stop()    # 프로그램 종료 

    win.show(frame)

# 프로그램이 끝날때 최종적으로 실행되는 함수 
def end():
    # 동영상의 최종 마무리를 위해서 반드시 필요 
    video_reader.release()

# ----------------------------------------
if __name__ == '__main__':
    run()
```
