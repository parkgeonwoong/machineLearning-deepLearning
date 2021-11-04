# 📌딥러닝 프레임워크

- 복잡한 딥러닝 네트워크를 구성할 수 있고, 오차역전파 알고리즘을 자동으로 수행해 주는 것이 핵심 기능
- 사전학습된 다양한 딥러닝 네트워크 구조를 활용할 수 있다.

</br>

## ✅ 텐서 플로우

- 구글에서 개발한 수치 계산과 딥러닝을 위한 오픈 소스 라이브러리
- 기본적으로 c++ 로 구현이지만 파이썬, 자바, 고 등 다양한 언어 지원
- 최대규모의 문서 및 커뮤니티를 가지고 있다.

<br>

## 🔥 Keras 케라스

- 케라스는 파이썬으로 작성된 오픈소스 딥러닝 라이브러리
- 케라스는 매우 쉽게 신경망을 사용할 수 있게 해주는 High level API이다.
- 케라스는 텐서플로우, MXNet 등 다른 프레임워크 위에서 동작

<br>

### 🔸케라스로 신경망을 작성하는 절차

- 케라스의 핵심 데이터 구조는 모델이며 이것은 레이어를 구성하는 방법을 나타낸다.

```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense
```

- Colab를 통해서 구현 및 구글드라이브

```python
from google.colab import drive
drive.mount('/content/drive')
```
