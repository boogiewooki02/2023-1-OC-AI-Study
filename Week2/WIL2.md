어떤 커널에서는 plt.plot으로 표현한다 -> stateful API 방식
: 현재의 figure(그래프를 그릴 공간), 현재의 ax(axes)(그 공간 중 지금 내가 사용할 부분)에 그림을 그리는 방법

어떤 커널에서는 ax.plot 혹은 axes[0,0].plot으로 표현한다 -> stateless API 방식 : 내가 지정한 figure, 내가 지정한 ax에 그림을 그리는 방법

stateless API
*figure 와 ax 객체를 생성하는 방법
#1. fig = plt.figure() : ax 없는 빈 figure 생성 (이후에 ax를 추가해야함)
#2. fig, ax = plt.subplots() : 하나의 ax 만을 가지는 하나의 figure 생성
#3. fig, axes = plt.subplots(2,2) : 4개(2*2) ax들을 가지는 하나의 figure 생성


penguin_df = sns.load_dataset("penguins") 의미: penguin_df 변수에 dataset인 penguins를 로드한다. (sns. 는 모듈 seaborn을 import할 때 sns라는 별칭을 붙였기에 쓴 것 -> 
import seaborn as sns)

부채꼴 스타일 -> plt.pie() 사용. 시작 각도, 퍼센트 소수점, 색깔, 음영, 떨어져너간정도 등등을 표현 가능

Boxplot은 Q1 - 1.5*IQR 에서부터 Q3 + 1.5*IQR의 범위 내에서 그려집니다.
만약 데이터 중 가장 작은 값이 Q1 - 1.5*IQR 값보다 작다면 범위에서 벗어나기 때문에,
Q1 - 1.5*IQR가 최솟값이 됩니다.
데이터 중 가장 큰 값이 Q3 + 1.5*IQR보다 크다면 범위에서 벗어나기 때문에,
Q3 + 1.5*IQR가 최댓값이 됩니다.
범위에서 벗어나는 값을 이상치(outlier)라고 하며 아래의 그림과 같이 boxplot의 위나 아래에 동그란 점으로 표시됩니다.