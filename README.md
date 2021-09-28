# 📌Colaboratory란?

`참고` [Colaboratory](https://colab.research.google.com/)

줄여서 'Colab'이라고도 하는 Colaboratory를 사용하면 브라우저에서 Python을 작성하고 실행할 수 있습니다. Colab은 다음과 같은 이점을 자랑합니다.

- 구성이 필요하지 않음
- GPU 무료 액세스
- 간편한 공유
<br/>

## matplotlib

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
