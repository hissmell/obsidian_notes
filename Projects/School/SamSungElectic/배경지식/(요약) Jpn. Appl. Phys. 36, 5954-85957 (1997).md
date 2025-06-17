[[Kishi_1997_Jpn._J._Appl._Phys._36_5954.pdf]]

## 인트로
- 코어쉘 구조 BTO
	![[Pasted image 20250617132918.png]]

- __코어__: 순수한 BTO, 강유전체(ferroelectric), 높은 유전계수 -> 고성능
- __쉘__: 도핑된 BTO, 상유전체(dielectric), 높은 열적안정성 -> 고안정성
- 코어-쉘 구조를 통해서, 고성능 + 고안정성 유전체를 설계하고자 함.
- __논문을 통해 분석하고자 하는것__
	- __왜 이런 코어쉘 구조가 형성되는가?__
	- __각 dopant가 어떤 역할을 하는가?__

## 실험 결과


### BT-0.0006MgO-0.0008Ho2O3-BaSiO3 TEM 이미지
![[Pasted image 20250617133551.png]]
전형적인 ferroelectric 패턴이 보인다고 하네요. 저는 전형적 패턴이 뭔지 몰라서 잘 몰것음

### grain shell EDX 스펙트럼
![[Pasted image 20250617133713.png]]
BTO에 Mg, Ho 가 모두 도핑된걸 확인할 수 있음

### XRD profile
![[Pasted image 20250617133843.png]]

1150 도 -> 1200 도 단계에서 tetragonal 에서 pseudocubic 으로 상이 전이 되는걸 관찰하였음. tetragonal 은 BTO 의 상이므로, 이 단계에서 shell이 형성된다고 판단하였음.

### DSC profile of Mg-BTO and Ho-BTO
![[Pasted image 20250617134144.png]]
Mg-rich 한 샘플이 두 온도 모두에서 더 날카로운 DSC peak을 보여주고 있음. 이건 화학반응 단계에서 전형적으로 diffusion limiting 반응이 보여주는 DSC peak 양상임. 따라서 Mg 가 BTO으로 확산되는게 더 느린 반응인걸 알 수 있음. Mg의 비율을 조절해서 Ho/Mg의 확산을 조절 가능

### XRD profile of Mg-doped and Ho-doped BT at 1100 
![[Pasted image 20250617134608.png]]

실제 합성 온도보다 낮은 1100도에서 Mg와 Ho를 도핑 및 신터링시켰을 때, Mg의 XRD 픽이 더 브로드하게 뽑힘. 이거 보면 Mg는 어느정도 반응이 진행 된 걸 판단할 수 있음. 따라서 Mg와 Ho 중에서 Mg가 더 낮은 온도에서 반응이 먼저 진행 될 거임

### SEM of Mg-doped and Ho-doped BT at 1350 

![[Pasted image 20250617134828.png]]
- Mg 는 그레인 바운더리 성장에 인히비터로 작용
- Ho는 안그럼

### Change in 200 peak of Mg-BT and Ho-BT as a function of sintering Temp

![[Pasted image 20250617134943.png]]

- brag's rule 에 의해서 "픽의 각도가 낮아진다 -> 격자 상수가 증가함" 으로 판단 가능
	![[Pasted image 20250617135133.png]]
- Mg 는 온도가 증가하면 격자 상수가 증가함
	- why? Mg는 일반적으로 Ti를 대체하며 acceptor으로 작용 (Ti4+ -> Mg2+)
	- 전하 균형을 맞추기 위해서 정공($V^{00}_{O}$)이 생성됨
	- 온도 증가시 정공의 부피가 증가하면서 격자 상수 증가
	- 이건 일반적으로 보고된 결과와 일치해서 따로 추가적 분석은 진행하지 않았음
- Ho 는 온도 증가해도 격자 상수 그대로임
	- Ho는 A-site와 B-site 모두 대체함. (A site: Ba2+ -> Ho3+, Ti4+ -> Ho3+)
	- 따라서 전하 균형이 이미 맞춰져 있기 때문에 정공이 생성되지 않음.
	- 온도가 증가해도 격자상수가 비교적 일정하게 유지됨.
	- 좀 더 자세한 이유 분석은 이후 설명


### Lattice parameters of Bt-xHo2O3 solid solution at 300
![[Pasted image 20250617140230.png]]
- 이온 반지름
	1. Ba2+(CN=12): 1.61
	2. Ho3+(CN=12): 1.20 정도? 정확한 값은 안 나와있음.
	3. Ho3+(CN=6): 0.901
	4. Mg2+(CN=6): 0.72
	5. Ti4+(CN=6): 0.745
- 1st zone
	- x 가 증가하면서 lattice parameter 상승
	- Ho3+(CN=6)는 Ti4+(CN=6) 보다 이온 반지름 큼
	- Ho가 Ti를 대체하기 때문에 lattice parameter 증가하는 것으로 추정
- 2nd zone
	- x가 증가하면서 lattice parameter 하락
	- Ho3+(CN=12)는 Ba2+(CN=12) 보다 이온 반지름 작음
	- Ho가 Ba를 대체하기 때문에 lattice paramter가 감소하는 것으로 추정

## 결론
- __왜 코어쉘 구조가 형성되는가?__
	1. MgO가 Ho2O3보다 더 낮은 온도에서 BT 와 반응함.
	2. 하지만 Mg는 diffusivity가 낮음 + 최대 0.01 비율 만큼 BT와 섞임
	3. 코어-쉘 구조 형성 (바깥쪽에 MgO 존재)
	4. 이후 Ho2O3 반응 시작
	5. Mg가 Ho의 diffusivity를 낮추는 작용을 하기 때문에 코어 쉘 구조가 유효하게 유지됨.
- __왜 코어-쉘 구조가 다른 물성이 나타나는가?__
	1. 코어 쪽은 순수한 BT 구조 유지됨. 일반적 BT와 동일한 물성
	2. 쉘 쪽은 Ho의 비율이 높음
	3. Ho는 A-site와 B-site에 모두 치환됨. 정공 생성 안함.
	4. tetragonal -> pseudocubic으로 상 변함
	5. 열적 안정성 Good!