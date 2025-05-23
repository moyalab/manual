---
description: HelloAi 파이썬 라이브러리를 사용하기 위한 환경 설정
---

# 환경 설정

HelloAI 파이썬 라이브러리는 파이썬 버전 3.10과 **3.11.x**을 지원합니다.  현재 [파이썬 공식 사이트](https://www.python.org/)에서는 파이썬 3.11 버전의 설치 파일을 다운로드 받을 수 없습니다.&#x20;

아나콘다(Anaconda) 또는 미니콘다(Miniconda) 를 설치하고, 파이썬 버전 3.11 의 가상환경을 만들어서 사용합니다.

{% embed url="https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html" %}

꼭 필요한 기능만 설치되는 Miniconda의 설치를 권합니다.  Miniconda를 설치한 후,   터미널에서 아래 명령으로 파이썬 3.11의 가상 환경을 만들고 활성화 시킬 수 있습니다. &#x20;

```
conda create -n <가상환경 이름> python=3.11
conda activate <가상환경 이름>
```

<가상환경 이름>에는 적당한 이름을 사용하면 됩니다.  예를 helloai 라는 이름을 사용한다면,

```
conda create -n peylconda create -n <가상환경 이름> python=3.11
conda activate <가상환경 이름>thon=3.11
conda activate <가상환경 이름>
```



HelloAI 팩키지를 설치합니다.

```
pip install helloai
```

