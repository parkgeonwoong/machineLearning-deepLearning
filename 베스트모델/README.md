- 모델 업데이트

모델을 그냥 저장하는 것이 아니라 에포크마다 모델의 정확도를 함께 기록하면서 저장

```python
import os
MODEL_DIR = '/content/drive/My Drive/Colab Notebooks/model/'
if not os.path.exists(MODEL_DIR):
   os.mkdir(MODEL_DIR)

modelpath = '/content/drive/My Drive/Colab Notebooks/model/{epoch:02d}-{val_loss:4f}.hdf5'
```

<br>

- sample() 함수를 사용하여 원본 데이터의 몇 %를 사용할지를 지정한다

```python
df = df_pre.sample(frac=1) # 전체 데이터의 몇 % 사용할지를
```

<br>

- 학습 자동 중단

학습이 진행될수록 학습셋의 정확도는 올라가지만 과적합 때문에 테스트셋의 실험 결과 점점 나빠지게 된다. 케라스에는 테스트셋 오차가 줄지 않으면 학습을 멈추게 하는 함수가 있다.

EarlyStopping()함수
