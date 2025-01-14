***[5차 교육세션] 통계 ***


# 수치 기술 통계량들 이해하기(ex : 평균, 분산, 상관계수 등등…)

### 중심위치 척도
1. 평균
- 모든 자료의 값을 더한 후 전체 개수로 나눈 값
- 이상치(outlier)와 측정 오차(measurement error)에 민감하게 반응함
2. 중앙값
- 자료를 크기 순으로 늘어 놓았을 때 가운데에 해당하는 값
3. 최빈값
- 자료 중에서 그 빈도수가 최대인 값

### 변동성 척도

1. 사분위수(quartile)
- 데이터 표본을 4개의 동일한 부분으로 나눈 값 (n은 총 도수)
2. 사분위간 범위 (IQR)
- 사분위간 범위 (Interquartile range, IQR) : Q3-Q1

3. 분산 (variance)
- 자료 각각이 평균으로부터 떨어져 있는 정도
- 편차의 제곱의 평균

4. 표준편차 (standard deviation)
- 분산의 제곱근

5. 변동 계수 (coefficient of variation)
- 표준편차를 평균에 대한 상대적인 값으로 표현
- 변동 계수(%) = 표준편차/평균 * 100

### 연관성 척도

1. 분산 (covariance)
- 두 변수가 각자의 평균으로부터 떨어진 값을 서로 곱한 후 평균 낸 값
- Cov(X,Y)>0이면 X와 Y는 양의 관계
- Cov(X,Y)<0이면 X와 Y는 음의 관계
- Cov(X,Y)=0이면 X와 Y는 양도 음도 아닌 관계
2. 상관계수 (correlation)
- 공분산을 각 변수의 변동성(표준편차)을 이용하여 표준화 한 값. -1과 1사이의 값을 가짐


# 여러 분포들과 표본과 모집단

확률분포(probability distribution)은 확률변수가 특정한 값을 가질 확률을 나타내는 함수를 의미한다.

### 이산확률분포의 종류
1. 베르누이분포(Bernoulli Distribution)
2. 이항분포(Binomial Distribution)
 - 연속된 n번의 독립시행에서 각 시행이 성공할 (또는 일어날) 확률 p를 가질 때 만들어지는 이산 확률 분포
3. 기하분포(Geometric Distribution)와 음이항분포(Negative Binomial Distribution)
4. 초기하분포(Hypergeometric Distribution)
5. 포아송분포(Poisson Distribution)
 - 단위 시간 안에 어떤 사건이 몇 번 일어날 것인지를 표현하는 이산 확률 분포입

### 연속확률분포의 종류
1. 정규분포(Normal Distribution)
- 모든 정규분포는 종 모양을 나타내고 좌우 대칭
- 정규곡선의 위치는 평균 μ 에 의해서 정해지고, 그 모양은 표준편차 σ 크기에 의해서 결정됨

2. T분포
- t분포는 표준정규분포처럼 0을 중심으로 종형의 모습을 가진 대칭 분포
- t분포는 자유도 n에 따라 모습이 변하는데, 자유도 n이 커짐에 따라 표준정규분포 N(0,1)에 수렴
> 자유도: 데이터에서 독립적인 정보의 수를 의미

3. F분포
- 정규분포를 이루는 모집단에서 독립적으로 추출한 표본들의 분산비율이 나타내는 연속 확률 분포입니다.
- 카이제곱분포와 마찬가지로 “분산”을 다룰 때 사용하는 분포인데, 카이제곱분포가 한 집단의 분산을 다뤘다면, F분포는 두 집단의 분산
- 회귀분석의 F-test를 이해하는데 필요한 분포(독립변수들의 변동과 종속변수의 변동을 확인해서 전체 회귀식이 유의한지 결정)

4. 감마분포(Gamma Distribution)
5. 지수분포(Exponential Distribution)
6. 카이제곱분포(Chi-squared Distribution)
- k개의 서로 독립적인 표준정규 확률변수를 각각 제곱한 다음 합해서 얻어지는 분포
- 정규분포의 제곱은 카이스퀘어 분포
- 제곱이 되어서 음수의 값들이 없는 모습
7. 베타분포(Beta Distribution)
8. 균일분포(Uniform Distribution)



# 가설검정의 절차와 해석

### 가설 설정
- 귀무가설 H0와 대립가설 H1를 설정합니다
- 귀무가설은 주로 확인하기 용이하거나 기각하고자하는 명제로 설정합니다

### 유의수준 설정
- 유의수준은 이 가설이 어느 정해진 수치를 벗어나면 귀무가설이 오류라고 인정할 것인가를 판단하는 기준
> - 1종 오류: 귀무가설이 실제로 참이었는데 기각할 확률(= 유의수준)
> - 2종 오류: 귀무가설이 실제로 거짓인데 기각하지 못할(채택) 확률

### 검정통계량 산출
- 검정통계량은 어떤 확률분포(정규분포, t분포, 이항분포 등)에서 가설 검정 목적으로 그 확률분포의 통계량을 산출하는 것  
- 검정통계량을 통해 기각 및 채택 여부를 결정하게 됩니다.
- 데이터가 분포나 특징에 따라 Z통계량, T통계량 등 어떤 검정통계량을 사용할지 정해야 함

### 기각/채택 판단
- 이 검정통계량이 신뢰구간에 위치해 있을 때는 대립가설 기각, 벗어날 시에는 대립가설을 채택


```python

```
