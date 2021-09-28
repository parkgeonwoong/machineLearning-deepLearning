# 📌Colaboratory란?

`참고` [Colaboratory](https://colab.research.google.com/)

줄여서 'Colab'이라고도 하는 Colaboratory를 사용하면 브라우저에서 Python을 작성하고 실행할 수 있습니다. Colab은 다음과 같은 이점을 자랑합니다.

- 구성이 필요하지 않음
- GPU 무료 액세스
- 간편한 공유
<br/>

## ✅ Matplotlib

`참고` [matplotlib](https://matplotlib.org/)


- 파이썬으로 데이터를 시각화할 때 가장 많이 사용하는 라이브러리
- 2D 형태의 그래프, 이미지 등을 그릴 때 사용
- 실제 과학 컴퓨팅 연구 분야나 인공지능 연구 분야에서도 많이 활용
<br />

```python
import matplotlib.pyplot # 그래프 그리기 라이브러리
```

```python
import matplotlib.pyplot as plt # 편하게 쓰기 위한 것
```

```python
# 기본 그래프 그리기
# plt.plot 데이터 셋
import matplotlib.pyplot as plt
plt.plot([10, 20, 30, 40])
plt.show()
```

```python
# 그래프에 옵션 추가하기
import matplotlib.pyplot as plt
plt.title("Graph Title")
plt.plot([10, 20, 30, 40], [1, 2, 3, 4], color="pink", marker='o', label='Label' ) 
# x,y축, 색깔,  그래프 선 모양, label 범례 
plt.legend()
plt.show()
```
<br />

### 🔥 선형대수에서 벡터란 ? 
  - 선형대수(linear algebra)는 데이터 분석에 필요한 각종 계산을 돕는 학문
  - 데이터 분석을 하려면 수많은 숫자로 구성된 데이터를 다루어햐 함
  - 선형대수를 사용하면 대량의 데이터를 포함하는 복잡한 계산 과정을 몇 글자 되지 않는 간단한 수식으로 서술
<br />


### 🔥 인공지능에서 왜 벡터를 사용하는가?
  - 인공지능에서 벡터는 **숫자의 집합 및 배열** 이라고 이해하면 쉼다
  - 인공지능에서는 특징 벡터라는 명칭을 사용한다.
  - 인공지능을 하려면 데이터에 어떤 특징이 있는지 찾아 벡터로 만들어야 함
  - 즉 데이터를 벡터로 만드는 것이 인공지능의 시작이라고 할 수 있다.
---

