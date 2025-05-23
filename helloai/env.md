---
description: HelloAi 파이썬 라이브러리를 사용하기 위한 환경 설정
---

# 🌱환경 설정

HelloAI 파이썬 라이브러리는 파이썬 버전 3.10과 **3.11.x**을 지원합니다.  현재 [파이썬 공식 사이트](https://www.python.org/)에서는 파이썬 3.11 버전의 설치 파일을 다운로드 받을 수 없습니다.&#x20;

**아나콘다(Anaconda)** 또는 **미니콘다(Miniconda)** 를 설치하고, 파이썬 버전 3.11 의 <mark style="color:red;">**가상환경**</mark>을 만들어서 사용합니다.&#x20;



아래 사이트에서 확인하세요.

{% embed url="https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html" %}

아나콘다에   비해서 기본 기능만 설치되는 **Miniconda의 설치**를 권합니다.  윈도우즈 PC의 경우 아래 링크를 클릭하면 Miniconda 설치 파일이 다운로드 됩니다.  py312 버전으로 설치합니다.

{% embed url="https://repo.anaconda.com/miniconda/Miniconda3-py312_25.3.1-1-Windows-x86_64.exe" %}

설치 후,  윈도우즈의 PowerShell 환경에서사용한다면,   터미널에서 아래 명령을 실행합니다.

```powershell
conda init powershell
```

Powershell환경에서 실행   정책 관련 에러가 발생한다면,&#x20;

```powershell
# 현재 실행 정책 확인
Get-ExecutionPolicy
```

실행 정책을변경해야한다면,    Powershell을관리자 권한으로 실행한 후, 아래 명령을 실행한다.

```powershell
# 만약 Restricted라면 관리자 권한으로 PowerShell을 열고:
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Powershell을 닫고, 다시 일반 사용자로 Powershell을 실행한 후,  아래 명령을 실행한다.

```
conda init powershell
```



Miniconda를 설치한 후,   터미널에서 아래 명령으로 파이썬 3.11의 가상 환경을 만들고 활성화 시킬 수 있습니다. &#x20;

```bash
conda create -n <가상환경 이름> python=3.11
conda activate <가상환경 이름>
```



<가상환경 이름>에는 적당한 이름을 사용하면 됩니다.  예를 helloai 라는 이름을 사용한다면,

```bash
conda create -n helloai python=3.11
conda activate helloai
```



가상 환경이    활성화된 상태에서 파이썬의   버전을 확인합니다.

```bash
python --version
```

파이썬 버전이 3.11 인것을 확인하고, HelloAI 팩키지를 설치합니다.

```bash
pip install helloai
```

