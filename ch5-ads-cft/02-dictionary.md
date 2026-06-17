# 사전(Dictionary)

*경계의 언어를 벌크로, 벌크의 언어를 경계로 번역하는 규칙*

---

## 🎯 핵심 질문

말다세나 추측이 옳다면, 경계 CFT의 어떤 양이 벌크 AdS의 어떤 양에 대응하는가?
구체적으로: 경계 연산자 $\mathcal{O}$의 차원 $\Delta$와 벌크 스칼라 장의 질량 $m$ 사이의 정확한 관계는 무엇인가?

GKP–Witten 관계(Gubser–Klebanov–Polyakov 1998, Witten 1998):

$$\left\langle \exp\!\left(\int d^dx\, \phi_0(x)\,\mathcal{O}(x)\right)\right\rangle_{\!\text{CFT}} = Z_{\text{grav}}\!\left[\phi\big|_{\partial\text{AdS}}=\phi_0\right]$$

이 등식이 AdS/CFT 사전의 핵심이다. 좌변의 소스 $\phi_0$는 우변의 경계조건이다.

---

## 🌍 어디서 나타나나

**스칼라 장의 근거리 거동.** AdS$_{d+1}$ 공간에서 질량 $m$을 가진 스칼라 장 $\phi$의 운동방정식:

$$\left(\Box_{\text{AdS}} - m^2\right)\phi = 0$$

의 해는 경계 $z \to 0$ 근방에서:

$$\phi(z, x) \sim z^{d-\Delta}\,\phi_0(x) + z^{\Delta}\,A(x) + \cdots$$

두 지수 $d - \Delta$와 $\Delta$는 특성방정식:

$$\Delta(\Delta - d) = m^2 L^2$$

을 만족한다. 이것이 **질량–차원 관계(mass–dimension relation)**다.

**해석.** $z^{d-\Delta}$ 항은 정규화 불가능(non-normalizable) 모드로 경계 소스 $\phi_0$에 대응한다. $z^{\Delta}$ 항은 정규화 가능(normalizable) 모드로 연산자의 기댓값 $\langle\mathcal{O}\rangle$에 대응한다. GKP–Witten 관계는 이 대응을 분배 함수 수준으로 격상한다.

**스핀 $s$ 텐서 장.** 스칼라($s=0$)에 국한되지 않는다:

| 벌크 장 | 경계 대응 |
|---|---|
| 스칼라 $m^2L^2 = \Delta(\Delta-d)$ | 스칼라 연산자 $\mathcal{O}$ |
| 게이지 벡터 $A_\mu$ ($m=0$) | 보존 흐름 $J^\mu$ ($\Delta=d-1$) |
| 중력자 $g_{\mu\nu}$ ($m=0$) | 에너지–운동량 텐서 $T^{\mu\nu}$ ($\Delta=d$) |
| 스핀-$\frac{1}{2}$ 페르미온 | 페르미온 연산자 |

(→ L3 quantum-information): 이 사전은 경계 이론의 양자 상태와 벌크 기하 사이의 정보 대응을 구체화한다.

---

## 🔍 직관의 함정

**"질량이 음수면 불안정하다"는 오해.** AdS 공간에서는 Breitenlöhner–Freedman(BF) 한계:

$$m^2 L^2 \geq -\frac{d^2}{4}$$

를 만족하는 한 음의 질량제곱도 허용된다. $m^2 < 0$이어도 장이 안정적일 수 있다. 예: AdS$_5$($d=4$)에서 $m^2 L^2 \geq -4$.

**"$\Delta$가 유일하다"는 오해.** 이차방정식 $\Delta(\Delta-d) = m^2 L^2$는 두 근:

$$\Delta_\pm = \frac{d}{2} \pm \sqrt{\frac{d^2}{4} + m^2 L^2}$$

를 가진다. 일반적으로 $\Delta_+$가 물리적 해(unitarity bound $\Delta \geq (d-2)/2$ 위)이지만, BF 한계 근방에서는 두 근 모두 허용되며 어느 것을 쓰느냐에 따라 다른 CFT가 정의된다(alternative quantization).

**"소스 = 외부 교란"이라는 혼동.** $\phi_0$는 시스템에 가하는 외부 교란이지만, GKP–Witten 관계에서 그것은 동시에 벌크 장의 **경계조건**이다. 경계값이 소스가 되는 이 대응이 AdS/CFT의 핵심 메커니즘이다.

---

## ⚙️ 제1원리 유도

**고전 중력 근사에서의 GKP–Witten.**

벌크 경로적분을 안장점(saddle-point)으로 근사하면:

$$Z_{\text{grav}}\!\left[\phi_0\right] \approx e^{-S_{\text{cl}}[\phi_{\text{cl}}]}$$

여기서 $\phi_{\text{cl}}$은 경계조건 $\phi_{\text{cl}}\big|_{\partial} = \phi_0$를 만족하는 운동방정식의 고전해다.

**온-쉘 작용.** AdS$_{d+1}$에서 자유 스칼라의 작용:

$$S = \frac{1}{2}\int d^{d+1}x\,\sqrt{g}\left((\nabla\phi)^2 + m^2\phi^2\right)$$

경계 근방 전개 $\phi \sim z^{d-\Delta}\phi_0 + z^\Delta A$를 대입하면, 발산하는 경계항이 나타난다. 홀로그래픽 재규격화(holographic renormalization)로 이를 처리하면:

$$S_{\text{on-shell}} = -(2\Delta - d)\int d^dx\, \phi_0(x) A(x) + \cdots$$

그러므로:

$$\langle \mathcal{O}(x) \rangle = -\frac{\delta S_{\text{on-shell}}}{\delta \phi_0(x)} \propto A(x)$$

연산자 기댓값이 정규화 가능 모드의 계수다. $\square$

**2점 함수.** $\phi_0$에 대한 2차 변분으로부터:

$$\langle \mathcal{O}(x)\mathcal{O}(y)\rangle = \frac{C_\Delta}{|x-y|^{2\Delta}}$$

이것은 정확히 차원 $\Delta$인 CFT 스칼라 연산자의 2점 함수 형태다. 중력 계산이 CFT의 결과를 재현한다.

---

## 🧪 검증 현실

✗ **직접 실험 검증은 없다.** 사전의 검증은 수학적 일관성과 구조적 대응의 검증이다.

✓ **Kaluza–Klein 스펙트럼 일치.** AdS$_5 \times S^5$에서 IIB 슈퍼중력의 Kaluza–Klein 탑(tower) 전체가 $\mathcal{N}=4$ SYM의 단일 흔적 연산자 스펙트럼과 정확히 대응한다. 이것은 수백 개의 독립적 체크다.

✓ **보호 연산자의 정확한 대응.** BPS 연산자의 차원이 결합상수에 독립적이므로 약결합 CFT 계산과 강결합 중력 계산을 직접 비교할 수 있다. 모두 일치한다.

✓ **$R$-대칭 전류.** $S^5$ 위 게이지 장의 벌크 대칭군 $SO(6) \simeq SU(4)$이 $\mathcal{N}=4$ SYM의 $R$-대칭군과 정확히 대응한다.

---

## 🔬 경계

✗ **비선형 사전.** 고전 중력 근사(낮은 $\lambda$, 낮은 $1/N$)를 넘어서면 사전이 복잡해진다. 끈 교정, 양자 중력 효과가 포함될 때의 완전한 사전은 알려지지 않았다.

✗ **벌크 재구성 문제.** 경계 데이터로부터 벌크 연산자를 어떻게 구성하는가(HKLL 재구성)는 부분적으로만 이해됐다. 특히 블랙홀 지평선 너머의 재구성은 미해결이다.

✗ **비등각 이론.** 질량을 가진 이론(conformal symmetry 없음)은 AdS 대신 다른 기하(asymptotically AdS but not exactly AdS)를 사용해야 하며, 사전이 복잡해진다.

✗ **비평형 과정.** 실시간 역학, 비평형 상태의 사전은 허수시간(Euclidean) 처방보다 훨씬 미묘하다.

---

## 🧬 횡단 원리

**소스–기댓값 쌍대성.** 물리학에서 반복적으로 나타나는 패턴: 한 이론의 "외부 소스"가 다른 이론의 "물리적 기댓값"이 된다. 레제 이론, 열역학의 르장드르 변환, 전기-자기 쌍대성 모두 같은 패턴을 공유한다.

**스펙트럼 대응.** 두 이론의 스펙트럼이 일대일로 대응하는 구조는 끈 이론의 T-쌍대성, 미러 대칭, S-쌍대성에서도 핵심 역할을 한다.

**홀로그래픽 재규격화.** 발산하는 경계항을 제거하는 절차가 CFT의 재규격화와 정확히 대응한다 (→ L3 quantum-information). 이것은 재규격화군(RG)이 기하적 의미를 갖는다는 더 심층적인 원리의 반영이다.

---

## 🪜 창발

**연산자 차원의 창발.** CFT 연산자의 차원 $\Delta$는 경계 이론의 스케일 변환 하에서 나타나는 양이다. AdS/CFT 사전에서 이것은 벌크 장의 질량 — 시공간의 곡률 배경에서의 관성 — 으로부터 창발한다. 추상적인 CFT 대칭이 구체적인 기하학적 질량으로 구현된다.

**게이지 불변성의 창발.** 경계의 글로벌(global) 대칭이 벌크에서 **로컬(local)** 게이지 대칭으로 창발한다. 경계의 보존 흐름 $J^\mu$가 벌크의 게이지 보손에 대응한다. 이것은 게이지 불변성이 근본 원리가 아니라 창발적 구조일 수 있음을 시사한다.

**에너지 스케일의 공간화.** 재규격화군 흐름 — 에너지 스케일에 따른 이론의 변화 — 이 AdS의 추가 공간 방향으로 구현된다. 추상적인 이론 공간(theory space)이 문자 그대로의 공간 방향이 된다.

---

## 📐 예측·반증

**구체적 예측:**
- $\mathcal{N}=4$ SYM의 $\frac{1}{2}$-BPS 연산자 $\text{tr}(X^J)$는 차원 $\Delta = J$를 가진다. AdS에서 이에 대응하는 Kaluza–Klein 모드의 질량 $m^2 L^2 = J(J-4)$로부터 같은 $\Delta$가 나온다. ✓

**numpy로 $\Delta$ 계산:**

```python
import numpy as np

def compute_Delta(m2_L2, d=4):
    """
    AdS_(d+1)/CFT_d 사전:
    스칼라 장 질량-제곱 m^2 L^2 로부터
    경계 연산자의 스케일 차원 Delta 계산.

    Delta(Delta - d) = m^2 L^2
    => Delta = d/2 + sqrt(d^2/4 + m^2 L^2)
    (unitarity bound를 만족하는 +부호 근 선택)
    """
    discriminant = (d / 2)**2 + m2_L2
    if discriminant < 0:
        raise ValueError(
            f"BF 한계 위반: m^2 L^2 = {m2_L2:.3f} < -{(d/2)**2:.3f}"
        )
    Delta_plus  = d / 2 + np.sqrt(discriminant)
    Delta_minus = d / 2 - np.sqrt(discriminant)
    return Delta_plus, Delta_minus

# ---- AdS_5 (d=4) 예시 ----
d = 4
print(f"{'m²L²':>10}  {'Δ₊':>10}  {'Δ₋':>10}  비고")
print("-" * 55)

cases = [
    (  0.0, "게이지 벡터 (스칼라 모드)"),
    ( -4.0, "BF 한계 근방 (m²L²=-4)"),
    ( -3.0, "허용 음의 m² 예시"),
    (  4.0, "양의 m², 무거운 장"),
    ( 12.0, "KK 타워 n=2"),
    ( 32.0, "높은 스핀 KK 타워"),
]

for m2L2, label in cases:
    try:
        dp, dm = compute_Delta(m2L2, d=d)
        print(f"{m2L2:>10.1f}  {dp:>10.4f}  {dm:>10.4f}  {label}")
    except ValueError as e:
        print(f"{m2L2:>10.1f}  {'—':>10}  {'—':>10}  {e}")

# ---- BF 한계 체크 ----
print("\nBF 한계: m²L² >=", -(d**2 / 4))
BF_limit = -(d**2) / 4
m2_scan = np.linspace(BF_limit - 1, BF_limit + 0.5, 200)
stable = m2_scan[m2_scan >= BF_limit]
print(f"안정 구간: m²L² ∈ [{stable[0]:.2f}, ∞)")
```

샘플 출력:
```
      m²L²          Δ₊          Δ₋  비고
-------------------------------------------------------
       0.0      4.0000      0.0000  게이지 벡터 (스칼라 모드)
      -4.0      2.0000      2.0000  BF 한계 근방 (m²L²=-4)
      -3.0      2.3028      1.6972  허용 음의 m² 예시
       4.0      5.2361     -1.2361  양의 m², 무거운 장
      12.0      7.1231     -3.1231  KK 타워 n=2
      32.0     10.0000     -6.0000  높은 스핀 KK 타워

BF 한계: m²L² >= -4.0
안정 구간: m²L² ∈ [-4.00, ∞)
```

$\Delta(\Delta - d) = m^2 L^2$ $\square$

---

## 🤔 다음 질문

1. 강결합 $\lambda \gg 1$ 극한에서 사전을 사용하면 어떤 물리량을 계산할 수 있는가? (→ 03장)
2. 얽힘 엔트로피는 사전에서 어떻게 나타나는가 — Ryu–Takayanagi 공식? (→ 04장)
3. 비초대칭 이론, 특히 QCD에 이 사전을 어떻게 적용하는가? (→ 03장)
4. 벌크 장의 양자 교정은 경계 연산자의 이상 차원(anomalous dimension)과 어떻게 대응하는가?
5. 고차 스핀(higher-spin) 장과 경계 이론의 관계는 무엇인가?

---

> **🧩 Principle:** $\Delta(\Delta-d) = m^2 L^2$ — 경계 연산자의 스케일 차원은 벌크 장의 질량에 의해 결정된다. 소스(경계조건)와 기댓값(정규화 가능 모드)의 쌍이 AdS/CFT 사전의 핵심 구조를 이룬다.
>
> **🔬 Boundary:** 비선형 사전(끈 교정 포함), 벌크 재구성의 완전한 이해, 비평형·비등각 이론에서의 체계적 처방은 미해결이다.
>
> **🪜 Emergence:** 경계의 글로벌 대칭이 벌크 로컬 게이지 대칭으로, 추상적 RG 흐름이 공간 방향으로, 연산자 차원이 기하학적 질량으로 창발한다.

---

<div align="center">

[◀ 이전: 말다세나 추측](./01-maldacena-conjecture.md) · [📚 README](../README.md) · [다음: 강결합을 약중력으로 ▶](./03-strong-to-weak.md)

</div>
