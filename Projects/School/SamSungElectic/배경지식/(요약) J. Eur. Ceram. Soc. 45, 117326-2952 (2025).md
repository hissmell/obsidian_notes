[[1-s2.0-S0955221925001463-main.pdf]]
## 인트로
- Dy 는 BT에 donor 와 accpetor으로 모두 도핑 될 수 있음
	- __donor__
		- Ba 치환
		- 자유전자 생성: 전기전도도 증가
		- 상온 유전율 증가 (퀴리온도 감소)
	- __acceptor__
		- Ti 치환
		- $V_{O}$ 생성: 전기전도도 감소
		- 유전율 감소: Ti보다 Dy의 이온 반지름이 더 커서 tetragonality 감소
- MgO를 반응물에 넣어서 코어쉘 구조를 형성할 수 있음 (사전 연구를 통해 많이 보고되었음)
- __Dy-pre BT 와 Mg-pre BT__ 파우더의 전기적 성질 비교

## 실험 결과

### Fig 1
![[Pasted image 20250618123546.png]]
- Dy precoated powder: 코어 -> Dy -> 쉘 구조 형성
- Mg precoated powder: 코어 -> 쉘 구조 형성, Mg 쉘은 큰 의미 없을 듯?

### Fig 2. (a), (b)
![[Pasted image 20250618123857.png]]

- 온도 변화에 따른 누설 전류 분석 진행함
- 일관되게 Mg-precoated powder 가 누설 전류가 더 높게 나옴 -> MLCC 로서 비선호
- 아레니우스 식으로 변환하여 ln(A) vs 1/T 기울기 분석함
	- ![[Pasted image 20250618124114.png]]
	- 두 샘플이 거의 유사한 기울기 가지는 걸 확인, 0.98 vs 0.94
	- Dy 확산 정도 차이가 전기 전도의 메커니즘을 바꾸지는 않는 걸로 생각

### Fig 2. (c), (d)
![[Pasted image 20250618124323.png]]
- 고온 영역에서 V vs A 그래프 그려봄
- power law fit 진행 결과 기울기 m 이 유사하게 나옴 + 1과 근접한 값 (0.86 vs 0.87)
- Ohmic 저항을 갖는 걸로 확인

### Fig 3. (a)
![[Pasted image 20250618124555.png]]
- 히스테리시스 분석 진행함
- maximum polarization: Mg > Dy
- remnat polarization: Mg > Dy
- coercive field: Mg > Dy

### Fig 3. (c), (d)
![[Pasted image 20250618124959.png]]
- Maximum dielectric temperature $T_{m}$: Dy 가 약간 더 낮음
- 유전율은 모든 주파수에서 Mg가 더 높음 -> 정전 용량은 더 큼
- 손실전류는 모든 주파수에서 Dy가 더 낮음
- 주파수에 따른 유전율, 손실 전류의 변화는 Mg 가 더 극적임
- Why?
	- 기본적으로 코어가 쉘보다 고온 영역에서 유전율이 더 높음
	- Mg의 경우, Mg가 BT 내부로 Dy의 확산을 방해함.
	- BT 내부로 못 들어간 Dy가 서로 aggregation 됨.
	- interfacial 분극이 생성됨. -> 정전 용량 상승 + 전류 손실 커짐
	- 따라서 Mg 의 경우의 경우 손실 전류가 더 커지게 됨

### Fig 4
![[Pasted image 20250618125946.png]]
- EDS mapping 으로 코어쉘 구조 형성된 모습 확인 가능
- Mg 의 경우 코어가 더 두꺼움
-  elemental line profiles 으로 정량적 분포 확인 가능

## 결론

- 뭘 먼저 코팅하느냐에 따라서 전류 전달의 메커니즘은 변화시키지 않는 선에서 유전체의 물성을 조절 가능함
	- if Mg pre-coating
		- 높은 정전용량
		- 낮은 insulating resistance
		- 높은 주파수 민감도
	- if Dy pre-coating
		- 낮은 정전용량
		- 높은 insulating resistance
		- 낮은 주파수 민감도