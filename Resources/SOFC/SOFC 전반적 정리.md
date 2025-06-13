![[Pasted image 20250528194333.png]]

# Background
## Electronic-Conducting cathode (EC) in the High-Temperature SOFC (HT-SOFC)


-  전통적 SOFC 에서 O2 의 환원 반응의 촉매로는 Pt가 사용되었음
-  하지만 Pt는 가격이 비싸다는 고질적 문제가 있음
-  Semiconducting ceramic 이 온도가 높아지면 충분히 전기전도도가 증가하기 떄문에 Pt를 대체할 물질로 주목 받고 있음 -> HT SOFC
-  다음의 요소들을 만족해야 함
	-  높은 전기전도도
	-  cycling 과정 중 높은 기계적 안정성
	-  마이크로 스케일에서 높은 porocity (~40%)
	-  ORR 단계에서 높은 촉매 활성
	-  Electrolyte와 비슷한 열 팽창 계수(TEC)
-  대표적 예시: $La_{1-x}Se_{x}Mn_{y}O_{3-\delta}$ (LSM) cathod with YSZ electrolyte
	![[Pasted image 20250528184834.png]]

-  ORR 반응이 일어나는 지점은 Cathod & Electrolyte & O2 gas 계면에서만 일어남 -> TPB
-  일반적으로 TPB 는 electrolyte 에서 $1 \mu$ 정도임.
- 일반적으로 Cathode는 $O_{V}$ 가 상대적으로 적고, 따라서 산소 이온 전도도가 낮게 됨. 

- 만약에 $La^{3+}$ -> $Sr^{2+}$ 으로 치환하면?
	- 가능한 시나리오 01: 산소 베이컨시를 늘려서 -> - 전하를 줄여서 -> 전하 균형 맞춤
	- 가능한 시나리오 02: B site 원자의 산화수를 늘림 -> + 전하를 늘려서 -> 전하 균형 맞춤

-  일반적으로 EC type SOFC는 __B site 원자의 산화수가 늘어남__!
-  왜냐면 B site 원자는 일반적으로 valence stability가 좋은 편임.
-  이렇게 B site 원자가 산화되는 경우에는 산소 베이컨시가 늘어나는 거에 비해서 화학적 안정성이 높음 -> 고온 안정성 상승 경향 LSM이 대표적인 예시



## Mixed Ionic and Electronic Conducting (MIEC) Cathodes in the Intermediate-Temperature SOFC (IT-SOFC)

- HT-SOFC는 작동온도가 섭씨 1000 도 정도로 매우 높음 -> 작동온도를 600 - 800 도로 낮춘게 특징 (IT-SOFC)
-  metal interconnect 를 개량 할 수 있게 되어서, 가격을 낮출 수 있었음
-  열관리가 쉬워졌고, 복사열 손실이 적어짐
-  Starting up 시간이 줄어듬
-  solid component에서 열적 스트레스가 감소하였음

-  작동 온도가 HT SOFC에 비해서 낮아졌으므로 키네틱이 재료설계에 더 주요한 역할로 부각됨
-  일반적으로 작동온도에서 가장 높은 분극 과전압이 나타나는 곳은 캐소드임. 따라서 이 부분 개발이 요구됨

	![[Pasted image 20250528191336.png]]

-  MIEC 를 이용해서 낮은 작동온도로 야기된 키네틱의 하락을 보완하려는 연구가 활발함
-  어떻게 MIEC는 전체 ORR 반응의 키네틱을 촉진하는가?
	1.  MIEC는 전자전도도와 산소이온전도도가 적절히 있음
	2.  Cathod 벌크 내에서 O2 이온 전도가 가능함
	3.  반응영역이 Cathod & O2 gas (2D) 영역으로 넓어짐


-  MIEC 물질의 활성 영역을 결정하는 요인들
	1. Cathod 표면에서 산소교환속도 -> surfaxce exchange coefficient $k_{0}$
	2. Cathod 벌크 내에서 산소 디퓨전 속도 -> diffusion coefficient $D_{0}$
	![[Pasted image 20250528192640.png]]



# Cr - Poisoning of SOFC

## Introduction

-  MIEC의 등장으로 작동온도 하락 -> interconnector 의 전도도 상승 필요 -> ceramic 에서 metallic으로 바꿔야함
-  하지만 metallic interconnector는 고온에서 부식 위험성 있음 -> 표면 Cr으로 코팅하여 부식 방지
-  근데 또 그러면 도포한 Cr 종이 SOFC의 cathode 에서 내구성 하락을 야기함 -> __Chromium Poisoning__ 

-  __Chromium Poisoning 의 종류__
	1. $Cr_{2}O_{3}$의 합성
	2. 기화된 Cr이 cathod와 반응


## Development of SOFC interconnector material and Cr-poisoning


  - __Interconnector 의 역할__
	-  anode와 cathode의 전기적 연결
	-  SOFC를 물리적으로 stack 하는 단계에서 지지체


-  __Interconnector 의 필요조건__
	- 높은 밀도: 공기와 연료가 섞이면 안됨
	- 높은 전기전도도
	- 높은 creep resistance (열이 가해졌을 때 흘러내리는 것에 대한 저항성) & 낮은 열팽창계수 차이 (다른 요소들과)
	- 높은 열전도도: 균일한 열 분포를 유지해야함
	- 높은 산화 환원 안정성
	- cycling 중 phase 유지
	- 높은 기계적 안정성

- 발전과정
	- __극 초기__
		- Acceptor-doped LCO 페로브스카이트 -> 비쌈, 가공 힘듬, 낮은 열전도도 등으로 폐기

	- __초기__
		- ferritic steels: 철과 크롬으로 이뤄진 금속
		- $Cr_{2}O_{3}$ 가 바깥으로 성장함. 
		- bulk 쪽 Cr 베이컨시가 쌓이게 되고, 이게 $Cr_{2}O_{3}$ 의 부착력을 낮추게 함

	- __현재?__
		- interconnector 표면에 코팅을 빡세게 줘서 Cr의 기화를 막으려는 시도가 활발함
		- long term stability가 문제임. 상대적으로 낮은 시간동안만 유효 (15000h - 23000h)

## Chromium vaporisation

- __Cr 기체 활성종__
	-  $CrO_{3}(g)$ and $CrO_{2}(OH)_{2}(g)$ 이 가장 열역학적으로 dominant 한 Cr 기체 활성종

		![[Pasted image 20250528200840.png]]
	- 낮은 습도 -> $CrO_{3}(g)$ dominant
	- 높은 습도 -> $CrO_{2}(OH)_{2}(g)$ dominant


## Cr deposition
