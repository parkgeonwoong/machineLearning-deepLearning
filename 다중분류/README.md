## ✅ 다중분류

- 클래스가 2개 아닌 3개 즉 1,0 이 아니라 여러 개 중에 어떤 것이 답인지를 예측하는 문제

<br>

### 🔸상관도 그래프

`참고` [pairplot](https://seaborn.pydata.org/generated/seaborn.pairplot.html)

- 3차원 이상의 데이터는 seaborn 패키지의 pairplot 명령을사용
- pairplot은 데이터프레임을 인수로 받아 그리드 형태로 각데이터 열의 조합에 대해 스캐터 플롯을 그린다
- 같은 데이터가 만나는 대각선 영역에는 히스토그램을 만듬

<br>

### 🔸원-핫 인코딩

- 0, 1, 2는 배운적이 없다 → 0, 1 로 바꿔줌
- 데이터 안에 문자열이 포함 → pandas로 데이터를 불러와 X,Y 구분
- 문자열을 숫자로 바꿔 주려면 클래스 이름을 숫자 형태로 바꿔줘야 함 → LabelEncoder()

  `참고` [LabelEncoder](https://scikit-learn.orgstable/modules/generated/sklearn.preprocessingLabelEncoder.html)

- **여러개의 Y값을 0, 1로만 이루어진 형태로 바꿔 주는 기법→ 원핫인코딩**

<br>

### 🔸소프트 맥스

- 확률 처럼 해석해서 0, 1로 바꿔준다.
- **총합이 1인 형태로 바꿔서 계산해 주는 함수**
- 예) 0.7 , 0.2 , 0.1 이것을 → 원핫 인코딩 → 1, 0 , 0
