## 🔥 과적합 피하기

🔸과적합이란?

- 모델이 학습 데이터셋 안에서는 일정 수준 이상의 예측 정확도를 보이지만, 새로운 데이터에 적용하면 잘 맞지 않는 것

<br>

🔸원인

- 학습이 많거나, 모델 복잡도가 많으면 ⇒ 과적합 발생
- 층이 너무 많거나 변수가 복합해서 발생

<br>

🔸왜 안좋은가?

- 예측의 정확성이 중요한데, 훈련에만 정확성이 높고, 테스트에는 안좋다.

  - 완전히 새로운 데이터에 적용하면 정확히 두 그룹으로 나누지 못함

<br>

🔸과적합을 방지하려면 어떻게 해야 하는가?

- 테스트 셋, 학습 셋이 분리되지 않아 발생 ⇒ 데이터 분리

<br>

- 데이터 를 학습셋, 테스트셋 분리 함수

```python
from sklearn.model_selection import train_test_split
# 데이터 분리 = 학습 + 테스트
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.3)
```

<br>

🔸플롯팅(그래프)

- 정확도가 훈련, 검증이 갈라지는 부분에서 과적합 발생
- epoch이 너무 과하기에 훈련에만 많아 발생

<br>

🔸학습셋, 검증셋, 테스트셋

- Training set(훈련 데이터)은 모델을 학습하는데 사용

- Validation set(검증 데이터)은 학습을 하면서 모델의 성능을 측정하기 위해 사용

  - 일반적으로 어떤 모델이 가장 데이터에 적합한지 찾아내기 위해서 다양한 학습 파라미터를 사용해보게 되며, 그 중 validation set으로 가장 성능이 좋았던 모델을 선택

- Test set(테스트 데이터)은 validation set으로 사용할 모델이 결정 된 후, 마지막으로 딱 한번 해당 모델의 예상되는 성능을 측정하기 위해 사용

<br>

### ✅ 모델 저장과 재사용

- 데이터셋을 여러 개로 나누어 하나씩 테스트셋으로 사용하고 나머지를 모두 합해서 학습셋으로 사용하는 방법

```python
from keras.models import load_model

# 학습한 데이터 save
save_dir = '/content/drive/My Drive/Colab Notebooks/model_save/'
model.save(save_dir + 'my_model.h5' )

# 불러오기
model = load_model(save_dir + 'my_model.h5')
```

<br>

### ✅ K겹 교차 검증

- 데이터셋을 여러 개로 나누어 하나씩 테스트셋으로 사용하고 나머지를 모두 합해서 학습셋으로 사용하는 방법
- 이렇게 하면 가지고 있는 데이터의 100%를 테스트셋으로 사용할 수 있다.

<br>

데이터를 원하는 숫자만큼 쪼개 각각 학습셋과 테스트텟으로 사용되게 만드는 함수 sklearn의 `StratifiedKFold()`함수

```python
from sklearn.model_selection import StratifiedKFold

# k겹 교차 검증
n_fold = 10
skf = StratifiedKFold(n_splits=n_fold, shuffle= True)

accuracy = []
for train, test in skf.split(X, Y):
    model = Sequential()
    model.add(Dense(24, input_dim = 60, activation='relu'))
    model.add(Dense(10,  activation='relu'))
    model.add(Dense(1,  activation='sigmoid'))
    model.compile(loss="mse", optimizer="adam", metrics=["accuracy"])
    model.fit(X[train], Y[train], epochs=100, batch_size=5)
    test_loss, test_accuracy = model.evaluate(X[test], Y[test])
    accuracy.append(test_accuracy)

print(accuracy)
avg_accuracy = np.mean(accuracy)
print(avg_accuracy)
```
