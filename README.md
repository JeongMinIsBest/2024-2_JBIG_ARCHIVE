# 2024-2학기 JBIG 학습 코드 아카이브 🔥
| 주차 | 학습 내용 정리 |
| :---: | :---: |
| 1주차 | [1주차 코드 과제 인사이트 정리](https://sly-increase-7b5.notion.site/1-31dfb4f8761580d688d2f57f8e655017?source=copy_link)     |
| 2주차 |      |
| 3주차 |      |
| 4주차 |      |
| 5주차 |      |
| 6주차 |      |
| 7주차 |      |
| 8주차 |      |
| 9주차 |      |
<br/>

## 🔠 Colab Seaborn, Matplotlib 한글 깨짐 현상 해결
- 나눔 폰트 설치
```
!sudo apt-get install -y fonts-nanum
!sudo fc-cache -fv
!rm ~/.cache/matplotlib -rf
```
  
- 폰트 설정
```
import matplotlib.pyplot as plt
plt.rc('font', family='NanumBarunGothic') 
plt.rcParams['axes.unicode_minus'] =False
```
  
출처 : [구글 코랩(colab) seaborn, matplotlib 한글 깨짐 현상 해결방법](https://giveme-happyending.tistory.com/192)
<br/>

## 🔠 로컬 환경에서 한글 깨짐 현상 해결
```
import matplotlib.pyplot as plt
from matplotlib import rc
import platform

# 시스템별 폰트 지정
if platform.system() == 'Windows':
    plt.rc('font', family='Malgun Gothic')  # 윈도우일 경우
elif platform.system() == 'Darwin':  # MacOS
    plt.rc('font', family='AppleGothic')
else:
    plt.rc('font', family='NanumGothic')  # 리눅스일 경우 추천

# 마이너스 깨짐 방지
plt.rcParams['axes.unicode_minus'] = False
```
</br>
