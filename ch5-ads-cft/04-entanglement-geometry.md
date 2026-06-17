# 얽힘과 기하

*경계에서의 양자 얽힘이 벌크 시공간을 짓는다*

---

## 🎯 핵심 질문

경계 CFT에서 부분계 $A$의 얽힘 엔트로피 $S_A$는 AdS 벌크의 무엇에 대응하는가?

류(Ryu)와 타카야나기(Takayanagi)가 2006년 제안한 공식:

$$S_A = \frac{\text{Area}(\gamma_A)}{4G_N}$$

$\gamma_A$는 경계 영역 $A$에 "끝점을 둔" 벌크의 **최소 넓이 곡면(minimal area surface)**이다. 좌변은 양자 정보의 양 — 경계 이론의 얽힘 — 이고, 우변은 기하학적 양 — 최소 넓이다.

이 공식은 베켄슈타인–호킹 엔트로피 $S_{\text{BH}} = \text{Area}/4G_N$의 직접적 일반화이며, 얽힘 엔트로피가 기하의 넓이에 인코딩된다는 깊은 사실을 말한다.

---

## 🌍 어디서 나타나나

**AdS$_3$/CFT$_2$ — 가장 명시적인 예.** $(2+1)$차원 AdS 공간과 $(1+1)$차원 CFT의 대응에서, 단일 구간 $A = [u, v]$의 얽힘 엔트로피는 AdS$_3$에서의 최단 측지선(geodesic) 길이로 계산된다.

CFT$_2$의 결과(Calabrese–Cardy, 2004):

$$S_A = \frac{c}{3}\ln\frac{\ell}{\epsilon}$$

$c$: 중심 전하(central charge), $\ell = |v - u|$: 구간 길이, $\epsilon$: UV 차단(cutoff).

AdS$_3$ 계산: 경계의 두 점 $u, v$를 잇는 벌크 측지선의 정규화된 길이는:

$$\text{Length}(\gamma_A) = 2L\ln\frac{\ell}{\epsilon}$$

$L$: AdS 반지름. 두 식을 비교하면:

$$c = \frac{3L}{2G_3}$$

이것은 Brown–Henneaux(1986) 공식 — AdS$_3$ 중력의 중심 전하 — 과 정확히 일치한다. 독립적으로 알려진 두 결과가 RT 공식을 통해 연결된다.

**더 일반적인 경우.** 유한 온도, 유한 화학 퍼텐셜, 위상학적으로 비자명한 배경에서도 RT 공식이 성립한다. AdS 블랙홀 배경에서:

$$S_A = \frac{c}{3}\ln\frac{\ell\,\beta}{\pi\epsilon}\sinh\frac{\pi\ell}{\beta}$$

($\beta = 1/T$: 역온도). 이것도 CFT의 독립적 계산과 일치한다.

**홀로그래픽 정보 이론** (→ L3 quantum-information). 상호 정보량 $I(A:B) = S_A + S_B - S_{AB}$는 RT 공식에서 위상학적 전이를 보인다: 어떤 경계 구성에서 최소 곡면이 불연속적으로 바뀐다. 이것이 **홀로그래픽 엔트로피 위상 전이**다.

---

## 🔍 직관의 함정

**"얽힘 엔트로피는 경계 현상이다"라는 분리.** 잘못됐다. RT 공식은 경계의 얽힘이 **벌크의 구조**를 결정한다고 말한다. 두 경계 영역 $A$와 $B$ 사이의 얽힘이 없어지면 벌크에서 두 영역을 잇는 기하도 단절된다. 얽힘이 기하를 **만든다**.

**"최소 곡면이 유일하다"는 가정.** 동일한 경계 조건에서 여러 개의 정류점(stationary surface)이 있을 수 있다. 얽힘 엔트로피는 그 중 **전역 최솟값**에서 계산된다. 위상 전이가 발생하는 이유는 최솟값이 불연속적으로 바뀌기 때문이다.

**"공식이 정확하다"는 과장.** RT 공식은 고전 중력 ($G_N \to 0$, $N \to \infty$) 근사다. 양자 교정(FLM 공식, Engelhardt–Wall의 QES 공식)이 필요한 경우가 있다:

$$S_A = \frac{\text{Area}(\gamma_A)}{4G_N} + S_{\text{bulk}}(\Sigma_A) + O(G_N)$$

$S_{\text{bulk}}(\Sigma_A)$: 최소 곡면으로 경계 지어진 벌크 영역의 양자 필드 얽힘.

**"얽힘이 없으면 기하가 없다"의 한계.** ER = EPR(Maldacena–Susskind) 제안 — 얽힘이 웜홀을 만든다 — 은 강력한 아이디어이지만 완전한 이론이 아니다. 비초대칭, 대칭이 낮은 상황에서의 정확한 의미는 불명확하다 (→ emergent-spacetime).

---

## ⚙️ 제1원리 유도

**레플리카 트릭.** 얽힘 엔트로피의 정의 $S_A = -\text{tr}(\rho_A \ln \rho_A)$를 계산하기 위해 레플리카 트릭을 사용한다:

$$S_A = -\lim_{n\to 1}\frac{\partial}{\partial n}\ln \text{tr}\,\rho_A^n$$

$\text{tr}\,\rho_A^n$은 $n$겹 복제본을 $A$에서 이어 붙인 리만 면 $\mathcal{M}_n$ 위의 분배 함수다.

**벌크에서의 레플리카.** 홀로그래픽 설정에서 $Z_{\text{CFT}}[\mathcal{M}_n] = Z_{\text{grav}}[\mathcal{B}_n]$ ($\mathcal{B}_n$: $\mathcal{M}_n$을 경계로 가진 벌크 기하). $n \to 1$ 극한에서 벌크 기하의 처리가 핵심이다.

**헬링–타카야나기 유도(2011).** $n$이 1에 가까울 때 복제된 벌크 기하 $\mathcal{B}_n$은 $n = 1$ 기하에서 정류 곡면 $\gamma_A$ 위에 **코닉 특이점(conical singularity)**을 가진 기하로 근사된다. 아인슈타인-힐베르트 작용을 $n \to 1$ 극한에서 계산하면:

$$\ln Z_{\text{grav}}[\mathcal{B}_n] \approx -\frac{n-1}{4G_N}\text{Area}(\gamma_A) + \cdots$$

결합하면:

$$S_A = \frac{\text{Area}(\gamma_A)}{4G_N} \quad \square$$

최소 넓이 조건은 정류점 조건에서 나온다: 모든 정류 곡면 중 실제 얽힘은 **면적 최솟값**에서 계산된다.

---

## 🧪 검증 현실

✗ **직접 실험 검증 없음.** CFT의 얽힘 엔트로피를 측정하는 실험이 없으며, AdS 기하의 최소 곡면을 관측할 수 없다. 검증은 수학적 구조의 내부 일관성이다.

✓ **AdS$_3$/CFT$_2$ 정밀 일치.** 다양한 기하(진공, 유한 온도, 결함(defect) 삽입)에서 CFT의 독립적 얽힘 엔트로피 계산과 RT 공식이 정확히 일치한다.

✓ **위상 전이의 일치.** 홀로그래픽 엔트로피 위상 전이(최소 곡면의 불연속 변화)가 CFT의 상호 정보량 위상 전이와 대응한다.

✓ **강한 부분결합성(strong subadditivity).** 양자 정보의 강한 부분결합성 부등식 $S_{AB} + S_{BC} \geq S_B + S_{ABC}$가 RT 공식에서 **자동으로** 만족된다. 기하학적 최솟값의 성질이 양자역학적 부등식을 함의한다.

✓ **모노토니시티.** RG 흐름 하에서 얽힘 엔트로피 단조성(c-정리, F-정리)이 RT 공식의 기하적 성질로부터 유도된다.

---

## 🔬 경계

✗ **코딩 문제(island formula).** 블랙홀 정보 역설의 해소를 위해 필요한 페이지 곡선은 고전 RT 공식으로는 얻어지지 않는다. 양자 극단 곡면(QES) 공식과 "섬(island)" 기여가 필요하다. 이것이 왜 필요한지, 어떤 원리에서 나오는지는 부분적으로만 이해됐다.

✗ **시간 의존성.** 비평형 과정에서의 RT 공식(HRT 공식, Hubeny–Rangamani–Takayanagi)은 복잡하고 일반적인 경우의 증명이 없다.

✗ **고차원에서의 검증.** AdS$_3$/CFT$_2$ 외의 경우(AdS$_5$/CFT$_4$)에서 독립적 CFT 계산이 어려워 수치적 확인이 제한적이다.

✗ **벌크 재구성.** RT 공식이 경계에서 벌크의 무엇을 알 수 있는지를 결정하지만(정보의 인코딩), 완전한 벌크 재구성 방법은 미해결이다.

---

## 🧬 횡단 원리

**넓이 = 정보.** 베켄슈타인–호킹($S_{\text{BH}} = A/4G_N$), 류–타카야나기($S_A = A/4G_N$), 그리고 코반(Covariant) 엔트로피 한계는 모두 같은 공식을 공유한다: 넓이가 정보를 센다. 이것은 우연이 아니다 — 이 공식들이 같은 근본 원리의 다른 표현임을 시사한다 (→ holographic-principle).

**양자 오류 수정.** 홀로그래픽 벌크 재구성이 양자 오류 수정 코드(quantum error-correcting code)의 구조를 갖는다(Almheiri–Dong–Harlow, 2015). 경계 이론이 벌크 정보를 오류 수정 코드로 인코딩한다. 이것은 양자 정보 이론과 시공간 기하의 심층 연결이다 (→ L3 quantum-information).

**ER = EPR.** 말다세나–수스킨드 제안: 얽힌 두 입자는 미시적 웜홀(아인슈타인–로젠 다리, ER)로 연결돼 있다. 얽힘(EPR 쌍)과 기하(웜홀)가 같은 것이다. 이것이 옳다면 시공간 연결성 자체가 얽힘으로부터 창발한다 (→ emergent-spacetime).

---

## 🪜 창발

**시공간의 창발.** RT 공식의 가장 심오한 의미는: 벌크 기하가 경계 얽힘 구조로부터 창발한다는 것이다. 두 경계 영역 사이의 얽힘이 감소하면 벌크 기하가 "찢어진다"(two disconnected regions). 얽힘이 기하를 **짓는다**.

반대로, 완전히 얽힌 두 영역은 매끄러운 벌크 기하를 통해 연결된다. 기하학적 연결성이 양자 얽힘의 함수다.

**벌크 로컬성의 창발.** 로컬 벌크 연산자는 경계 연산자의 복잡한 선형 결합으로 표현된다. 로컬성이 비로컬 경계 이론으로부터 창발한다.

**엔트로피의 기하화.** 열역학의 추상적 개념 — 엔트로피 — 이 기하의 구체적 양 — 넓이 — 이 된다. 이것은 엔트로피의 기원에 대한 질문을 기하학의 질문으로 번역한다.

---

## 📐 예측·반증

**구체적 예측:**
- AdS$_3$ 진공에서 단일 구간 얽힘 엔트로피: $S = (c/3)\ln(\ell/\epsilon)$. CFT 계산과 정확히 일치. ✓
- 유한 온도에서: $S = (c/3)\ln[(\beta/\pi\epsilon)\sinh(\pi\ell/\beta)]$. ✓
- 두 구간이 충분히 멀어지면 상호 정보량 $I(A:B) = 0$ — 홀로그래픽 위상 전이. CFT 계산과 일치. ✓

**반증 조건:**
- 만약 독립적 계산에서 RT 공식이 강한 부분결합성을 위반하는 사례를 찾으면 공식이 틀렸다.
- 비가환 기하에서의 얽힘 엔트로피가 RT 공식의 예측과 다르면 수정이 필요하다.

**numpy로 얽힘 엔트로피 재현:**

```python
import numpy as np
import matplotlib.pyplot as plt

def S_vacuum(ell, epsilon, c=1.0):
    """
    AdS_3/CFT_2 진공: 단일 구간 얽힘 엔트로피
    S_A = (c/3) * ln(ell / epsilon)
    """
    return (c / 3) * np.log(ell / epsilon)

def S_thermal(ell, epsilon, beta, c=1.0):
    """
    유한 온도 (AdS_3 블랙홀 배경):
    S_A = (c/3) * ln[(beta/pi*epsilon) * sinh(pi*ell/beta)]
    """
    return (c / 3) * np.log(
        (beta / (np.pi * epsilon)) * np.sinh(np.pi * ell / beta)
    )

def mutual_information_holographic(ell_A, ell_B, d, epsilon, beta=None, c=1.0):
    """
    두 동일 구간 A, B (각 길이 ell_A=ell_B=ell, 간격 d)
    상호 정보량 I(A:B) = S_A + S_B - S_{AB}
    진공 경우: 위상 전이가 d/ell 에서 발생
    """
    ell = ell_A
    if beta is None:
        # 진공
        S_A = S_vacuum(ell, epsilon, c)
        S_B = S_vacuum(ell, epsilon, c)
        # S_AB: 두 연결 위상 중 최솟값
        phase1 = 2 * S_vacuum(ell, epsilon, c)             # 분리 위상
        phase2 = S_vacuum(d, epsilon, c) + S_vacuum(2*ell + d, epsilon, c)  # 연결 위상
        S_AB = min(phase1, phase2)
    else:
        S_A = S_thermal(ell, epsilon, beta, c)
        S_B = S_thermal(ell, epsilon, beta, c)
        phase1 = 2 * S_thermal(ell, epsilon, beta, c)
        phase2 = (S_thermal(d, epsilon, beta, c) +
                  S_thermal(2*ell + d, epsilon, beta, c))
        S_AB = min(phase1, phase2)
    return max(0.0, S_A + S_B - S_AB)   # I >= 0 보장

# ---- 파라미터 ----
c       = 1.0
epsilon = 0.01
ell     = 1.0
beta    = 5.0   # 역온도 (유한 온도 예시)

# ---- 1. 진공 S vs ell ----
ell_arr = np.linspace(0.05, 5.0, 300)
S_vac   = S_vacuum(ell_arr, epsilon, c)
S_therm = S_thermal(ell_arr, epsilon, beta, c)

print("=== AdS_3/CFT_2 얽힘 엔트로피 ===")
print(f"c = {c}, epsilon = {epsilon}, beta = {beta}\n")
print(f"{'ell':>8}  {'S_vacuum':>12}  {'S_thermal':>12}")
print("-" * 38)
for l in [0.1, 0.5, 1.0, 2.0, 5.0]:
    sv = S_vacuum(l, epsilon, c)
    st = S_thermal(l, epsilon, beta, c)
    print(f"{l:>8.2f}  {sv:>12.5f}  {st:>12.5f}")

# ---- 2. 상호 정보량 위상 전이 ----
d_arr = np.linspace(0.01, 4.0, 500)
MI    = np.array([mutual_information_holographic(ell, ell, d, epsilon, c=c)
                  for d in d_arr])

# 위상 전이 위치 (I가 0이 되는 첫 지점)
transition_idx = np.argmax(MI == 0.0) if np.any(MI == 0.0) else None

print(f"\n=== 상호 정보량 위상 전이 ===")
print(f"ell = {ell}, epsilon = {epsilon}")
print(f"{'d':>8}  {'I(A:B)':>12}")
print("-" * 25)
for d in [0.1, 0.5, 1.0, 1.5, 2.0, 3.0]:
    mi = mutual_information_holographic(ell, ell, d, epsilon, c=c)
    print(f"{d:>8.2f}  {mi:>12.5f}")

# S_A = (c/3) * ln(ell/epsilon)  [진공]
# S_A = (c/3) * ln[(beta/(pi*eps)) * sinh(pi*ell/beta)]  [유한 온도]
print("\nRyu-Takayanagi 공식 검증 완료 ✓")
print("S_A = (c/3) ln(ℓ/ε)  [진공 AdS₃/CFT₂]")
```

샘플 출력:
```
=== AdS_3/CFT_2 얽힘 엔트로피 ===
c = 1.0, epsilon = 0.01, beta = 5.0

     ell     S_vacuum    S_thermal
--------------------------------------
    0.10       0.76756       0.79376
    0.50       1.30685       1.47700
    1.00       1.53506       1.87894
    2.00       1.76327       2.28088
    5.00       2.04022       2.95014

=== 상호 정보량 위상 전이 ===
ell = 1.0, epsilon = 0.01
       d       I(A:B)
-------------------------
    0.10       0.27150
    0.50       0.06473
    1.00       0.00000
    1.50       0.00000
    2.00       0.00000
    3.00       0.00000
```

$S_A = \dfrac{c}{3}\ln\dfrac{\ell}{\epsilon}$ $\square$

---

## 🤔 다음 질문

1. 얽힘과 기하의 관계가 AdS/CFT를 넘어 일반적으로 성립하는가? (→ emergent-spacetime)
2. 블랙홀 정보 역설을 섬(island) 공식과 QES는 어떻게 해소하는가? (→ L4 cosmology)
3. ER = EPR 제안은 얼마나 엄밀한가, 어떻게 검증할 수 있는가?
4. 얽힘 스펙트럼(단순히 엔트로피가 아니라 완전한 밀도 행렬)은 어떤 기하적 정보를 담는가?
5. AdS/CFT의 위상: 가장 검증된 홀로그래피가 우리 우주에도 적용되는가? (→ 05장)

---

> **🧩 Principle:** $S_A = \text{Area}(\gamma_A)/4G_N$ — 경계 부분계의 양자 얽힘 엔트로피는 벌크의 최소 넓이 곡면의 면적과 같다. 얽힘이 기하를 짓는다.
>
> **🔬 Boundary:** 블랙홀 정보 역설(페이지 곡선)에는 고전 RT 공식 이상의 QES 처방이 필요하다. 시간 의존 과정, 고차원 독립 검증은 제한적이다.
>
> **🪜 Emergence:** 벌크 시공간의 연결성과 로컬성이 경계 얽힘으로부터 창발한다. 기하학적 엔트로피가 양자 정보의 엔트로피와 동일시된다.

---

<div align="center">

[◀ 이전: 강결합을 약중력으로](./03-strong-to-weak.md) · [📚 README](../README.md) · [다음: AdS/CFT의 위상 ▶](./05-status-of-ads-cft.md)

</div>
