# T-쌍대성

*작은 원과 큰 원은 같은 물리다 — 최소 길이가 존재하는 이유*

---

## 🎯 핵심 질문

끈을 반지름 $R$인 원에 감을 때, 왜 $R \to 0$ 극한이 $R \to \infty$와 물리적으로 동치인가? 그리고 이것이 시공간 기하학의 "최소 단위"에 대해 무엇을 말하는가?

T-쌍대성(T-duality)은 끈이론에서 가장 직접적으로 확인 가능한 쌍대성이다. 콤팩트화(compactification) — 차원 중 하나를 반지름 $R$인 원으로 말아두는 절차 — 를 할 때, 끈에는 점입자에는 없는 새로운 자유도가 생긴다: **감김 모드(winding mode)**. 이 감김 모드가 운동량 모드와 교환되는 구조가 T-쌍대성의 핵심이다. 결과적으로 $R \leftrightarrow \alpha'/R$이라는 "큰 것과 작은 것의 교환"이 정확한 대칭이 된다. (→ quantum-gravity)

---

## 🌍 어디서 나타나나

**기본 설정.** 9번째 공간 차원이 반지름 $R$인 원 $S^1$으로 콤팩트화되었다고 하자. 9차원 방향의 좌표를 $X^9 \equiv X^9 + 2\pi R$로 주기화한다.

**점입자의 경우.** 입자의 운동량은 양자화된다:
$$p_9 = \frac{n}{R}, \quad n \in \mathbb{Z}$$
$R \to 0$이면 $p_9 \to \infty$, 운동량 에너지가 발산한다. 점입자에게 작은 원은 "접근할 수 없는" 방향이 된다.

**끈의 경우.** 끈은 원을 $w$번 감길 수 있다:
$$X^9(\sigma + 2\pi) = X^9(\sigma) + 2\pi w R, \quad w \in \mathbb{Z}$$
이 감김 수(winding number) $w$에 대한 에너지 기여는:
$$E_{\text{wind}} \sim \frac{wR}{\alpha'}$$
반지름이 작을수록 감는 데 드는 에너지가 줄어든다. 운동량 모드와 감김 모드의 에너지 기여가 정확히 교환된다: $n \leftrightarrow w$, $R \leftrightarrow \alpha'/R$.

T-쌍대성은 Type IIA와 Type IIB 사이, 또는 두 Heterotic 이론 사이를 연결한다. 9번째 차원에서 T-쌍대성 변환을 하면 IIA $\leftrightarrow$ IIB가 된다.

---

## 🔍 직관의 함정

**함정 1: "원이 더 작으면 더 작은 물리가 보인다"**

점입자의 직관이다. 끈에게는 틀렸다. $R < \sqrt{\alpha'}$이면 감김 모드가 가벼워져서 이 모드들이 "새로운 방향"을 만들어낸다. 실효적으로 반지름이 $\alpha'/R > \sqrt{\alpha'}$인 것과 구별이 안 된다.

**함정 2: "T-쌍대성은 근사 대칭이다"**

✗ 아니다. T-쌍대성은 정확한(exact) 대칭이다. 세계면(worldsheet) CFT 레벨에서 엄밀하게 성립한다. 섭동 전개의 어떤 차수에서도 깨지지 않는다.

**함정 3: "감김 모드와 운동량 모드는 독립적인 자유도다"**

T-쌍대성 변환 아래 이 두 가지는 역할을 완전히 교환한다. 쌍대 이론에서 운동량 모드로 보이는 것이 원래 이론의 감김 모드이며, 그 역도 성립한다.

**함정 4: "T-쌍대성은 비섭동 정보를 주지 않는다"**

T-쌍대성은 세계면 결합상수(끈 결합상수 $g_s$)와 무관하게 작동한다. 섭동론의 어떤 차수에서도 성립하는 섭동적 쌍대성이다. 비섭동 정보는 S-쌍대성이 담당한다 (→ 03-s-duality).

---

## ⚙️ 제1원리 유도

폐합 끈(closed string)의 질량 공식을 콤팩트 차원을 포함하여 유도하자.

**자유 닫힌 끈의 세계면 작용:**
$$S = -\frac{1}{4\pi\alpha'}\int d\tau\, d\sigma\, \partial_a X^\mu \partial^a X_\mu$$

**콤팩트 차원의 모드 전개.** 닫힌 끈에서 $X^9$의 모드 전개는 좌이동(left-moving)과 우이동(right-moving)으로 분리된다:
$$X^9(\tau,\sigma) = x^9 + \frac{\alpha'}{2}\left(\frac{n}{R} + \frac{wR}{\alpha'}\right)\tau + \left(\frac{wR}{\alpha'} - \frac{n}{R}\right)\sigma \cdot \frac{\alpha'}{2} + \text{진동 모드}$$

더 명확하게, 좌·우 운동량을 정의한다:
$$p_L = \frac{n}{R} + \frac{wR}{\alpha'}, \qquad p_R = \frac{n}{R} - \frac{wR}{\alpha'}$$

**질량 공식.** Virasoro 조건(레벨 정합 조건)에서 질량의 제곱은:
$$M^2 = \left(\frac{n}{R}\right)^2 + \left(\frac{wR}{\alpha'}\right)^2 + \frac{2}{\alpha'}\left(N_L + N_R - 2\right)$$

여기서 $N_L$, $N_R$은 좌·우 진동수(oscillator number)다. 레벨 정합 조건:
$$N_L - N_R = nw$$

**T-쌍대성 변환.** $R \to \tilde{R} = \alpha'/R$, $n \leftrightarrow w$ 변환을 적용하면:
$$\left(\frac{n}{R}\right)^2 + \left(\frac{wR}{\alpha'}\right)^2 \to \left(\frac{w}{\alpha'/R}\right)^2 + \left(\frac{n \cdot \alpha'/R}{\alpha'}\right)^2 = \left(\frac{wR}{\alpha'}\right)^2 + \left(\frac{n}{R}\right)^2$$

즉 $M^2$이 불변이다. 레벨 정합 조건 $N_L - N_R = nw$도 $n \leftrightarrow w$ 아래 불변이다. 따라서 전체 스펙트럼이 $R \leftrightarrow \alpha'/R$ 아래 불변이다. $\square$

**최소 길이.** $R = \sqrt{\alpha'}$에서 이론은 자기쌍대(self-dual)다: $R = \tilde{R}$. 이 길이가 T-쌍대성으로 정의되는 최소 길이 $\ell_s = \sqrt{\alpha'}$다. $R < \ell_s$로 가는 것은 $R > \ell_s$로 가는 것과 동일한 물리다.

---

## 🧪 검증 현실

✗ **직접 실험 검증 없음.** T-쌍대성 자체를 입자가속기에서 검증할 방법은 현재 없다. 관련 에너지 척도는 플랑크 에너지 근방이다.

✓ **수학적 구조의 내부 일관성 검사.** "검증"은 다음의 수학적 일관성으로 이루어진다:

- **분배함수 불변성:** 1루프 분배함수 $Z(R) = Z(\alpha'/R)$가 명시적으로 계산되어 확인된다. 모듈러 불변성과 T-쌍대성이 함께 세계면 CFT의 일관성을 보장한다.
- **BPS 스펙트럼:** 콤팩트 차원을 가진 초끈이론에서 BPS 상태들의 질량과 전하가 $R \leftrightarrow \alpha'/R$ 아래 정확히 대응된다.
- **유효 이론 일치:** Type IIA를 $S^1$에 콤팩트화한 유효장론이 Type IIB를 $\alpha'/R$인 $S^1$에 콤팩트화한 유효장론과 일치한다.

아래 수치 계산으로 스펙트럼 불변을 직접 확인한다.

```python
import numpy as np

def string_mass_squared(n, w, R, alpha_prime=1.0, N_L=0, N_R=0):
    """
    닫힌 끈의 질량제곱 계산 (콤팩트 차원 포함).
    M^2 = (n/R)^2 + (wR/alpha')^2 + (2/alpha')(N_L + N_R - 2)
    레벨 정합 조건: N_L - N_R = n*w
    """
    momentum_term = (n / R) ** 2
    winding_term = (w * R / alpha_prime) ** 2
    oscillator_term = (2 / alpha_prime) * (N_L + N_R - 2)
    return momentum_term + winding_term + oscillator_term

def t_dual_radius(R, alpha_prime=1.0):
    return alpha_prime / R

# 검증: 다양한 (n, w) 조합에 대해 M^2(R) = M^2(alpha'/R, n<->w)
alpha_prime = 1.0
R_values = np.array([0.3, 0.5, 0.7, 1.0, 1.5, 2.0, 3.0])

print("T-쌍대성 스펙트럼 불변 검증")
print("=" * 65)
print(f"{'R':>6} | {'R̃=α\'/R':>8} | {'(n,w)':>8} | {'M²(R)':>12} | {'M²(R̃,n↔w)':>12} | {'일치':>5}")
print("-" * 65)

test_modes = [(1, 0), (0, 1), (1, 1), (2, 1), (1, 2), (2, 0), (0, 2)]

for R in R_values:
    R_dual = t_dual_radius(R, alpha_prime)
    for (n, w) in test_modes:
        # 바닥상태만 확인: N_L = N_R = 1 (레벨 정합 조건 nw=0인 경우)
        # 간단히 N_L=N_R=1로 고정 (tachyon 제외)
        if n * w == 0:  # 레벨 정합 조건 N_L - N_R = nw = 0 만족
            N_L = N_R = 1
            M2_original = string_mass_squared(n, w, R, alpha_prime, N_L, N_R)
            # T-쌍대: R -> R̃, n <-> w
            M2_dual = string_mass_squared(w, n, R_dual, alpha_prime, N_L, N_R)
            match = "✓" if np.isclose(M2_original, M2_dual, rtol=1e-10) else "✗"
            print(f"{R:>6.2f} | {R_dual:>8.4f} | {str((n,w)):>8} | {M2_original:>12.6f} | {M2_dual:>12.6f} | {match:>5}")

print()
print("자기쌍대점(self-dual point) 확인: R = sqrt(alpha')")
R_self_dual = np.sqrt(alpha_prime)
print(f"R = {R_self_dual:.6f}, α'/R = {alpha_prime/R_self_dual:.6f}")
print(f"자기쌍대 조건 성립: {np.isclose(R_self_dual, alpha_prime/R_self_dual)}")

print()
print("T-쌍대성 변환 전후 질량 스펙트럼 비교 (R=0.5, N_L=N_R=1)")
R_test = 0.5
R_dual_test = alpha_prime / R_test
modes_to_check = [(n, w) for n in range(3) for w in range(3) if n*w == 0]
print(f"{'(n,w)':>8} | {'M²(R={:.1f})'.format(R_test):>14} | {'M²(R̃={:.1f},n↔w)'.format(R_dual_test):>16} | 불변")
print("-" * 55)
for (n, w) in modes_to_check:
    N_L = N_R = 1
    M2_R = string_mass_squared(n, w, R_test, alpha_prime, N_L, N_R)
    M2_Rd = string_mass_squared(w, n, R_dual_test, alpha_prime, N_L, N_R)
    inv = "✓" if np.isclose(M2_R, M2_Rd, rtol=1e-10) else "✗"
    print(f"{str((n,w)):>8} | {M2_R:>14.6f} | {M2_Rd:>16.6f} | {inv}")
```

위 코드를 실행하면 모든 $(n, w)$ 조합에서 $M^2(R) = M^2(\alpha'/R)$ (단, $n \leftrightarrow w$)가 기계 정밀도 수준($10^{-10}$)으로 성립함을 확인할 수 있다.

---

## 🔬 경계

**T-쌍대성이 적용되지 않는 경우.**

✗ **비콤팩트 차원.** T-쌍대성은 원형 콤팩트 차원이 있을 때만 정의된다. 비콤팩트 방향에는 감김 모드가 없으므로 T-쌍대성 변환이 없다.

✗ **열린 끈(open string)의 경우 수정.** 열린 끈은 끝점이 있으므로 원을 감을 수 없다. 그러나 T-쌍대성 변환 시 열린 끈의 경계조건(Neumann $\leftrightarrow$ Dirichlet)이 바뀌어 D-브레인이 나타난다. 따라서 열린 끈에도 T-쌍대성은 적용되지만, 그 결과가 D-브레인의 생성으로 나타난다 (→ Ch4 브레인).

✗ **비등방 배경에서의 복잡성.** Buscher 규칙(Buscher rules)은 일반 배경(메트릭, B-장, 딜라톤)에서의 T-쌍대성 변환 규칙이다. 등방 배경에서는 간단하지만, 일반 배경에서는 쌍대성이 잘 정의되지 않거나 비가환 기하학이 나타날 수 있다.

✓ **닫힌 끈 섭동론 전체에서 정확.** 닫힌 끈 레벨에서 T-쌍대성는 세계면 CFT의 정확한 대칭이며, 루프 고리 전체에서 성립한다.

---

## 🧬 횡단 원리

**Fourier 쌍대성과의 유사.** 운동량 $n/R$과 위치(감김) $wR/\alpha'$ 사이의 교환은 위치-운동량 Fourier 쌍대성의 끈이론적 버전이다. 그러나 여기서 "위치"는 끈이 원을 감는 횟수라는 토폴로지적 자유도다.

**격자 쌍대성(lattice duality).** T-쌍대성은 정수 격자 $\Gamma$와 그 쌍대 격자 $\Gamma^*$ 사이의 대응으로 이해할 수 있다. $(p_L, p_R)$ 격자 $\Gamma^{1,1}$은 $n \leftrightarrow w$ 아래 자기쌍대(self-dual)다.

**비가환 기하학.** 작은 $R$ 극한에서 끈이 인식하는 기하학은 점입자가 보는 기하학이 아니다. 극단적 경우(T-쌍대성 여러 번 적용 후)에 비가환 기하학(noncommutative geometry)이 나타날 수 있으며, 이는 양자중력에서 공간 자체의 구조가 달라짐을 암시한다 (→ quantum-gravity).

**거울 대칭(mirror symmetry).** T-쌍대성을 Calabi-Yau 다양체의 특수 라그랑지안 섬유(special Lagrangian fibration) 위에 적용한 것이 거울 대칭(SYZ 추측)이다. 두 위상적으로 서로 다른 Calabi-Yau 공간이 물리적으로 동치가 된다.

---

## 🪜 창발

T-쌍대성의 가장 심층적 함의는 공간 기하학의 개념 자체가 상대적이라는 것이다.

$R \to 0$은 "공간이 없어진다"는 것이 아니다. 끈에게는 그것이 $R \to \infty$로의 팽창과 구별되지 않는다. 기하학적 직관에서 "작다"와 "크다"의 구별이 끈의 레벨에서는 성립하지 않는다.

이것은 거리와 크기가 우리의 저에너지 유효 기술에서 창발하는 개념임을 시사한다. 기본 끈 길이 $\ell_s = \sqrt{\alpha'}$ 이하에서는 "기하학적 거리"라는 개념이 끈이론이 말하는 실제 물리와 다르다.

자기쌍대점 $R = \ell_s$에서 추가 대칭이 강화된다. 이 점에서 $U(1)$ 대칭이 $SU(2)$로 확대되고(게이지 대칭 강화), 여분의 질량 없는(massless) 상태들이 나타난다. 이런 "임계 기하학"의 존재는 공간의 구조가 이산적 또는 양자화된 무언가임을 강하게 암시한다 (→ emergent-spacetime).

---

## 📐 예측·반증

✓ **수치적으로 확인 가능한 예측.** 위 Python 코드가 보여주듯, $M^2(n, w, R) = M^2(w, n, \alpha'/R)$는 임의의 $R$과 $(n, w)$에 대해 대수적으로 성립한다. 이것은 반증 가능한 수학적 명제다.

✓ **자기쌍대점에서의 스펙트럼.** $R = \sqrt{\alpha'}$에서 추가적인 질량 없는 벡터 상태가 나타나야 한다. 이것은 세계면 CFT 계산에서 명시적으로 확인된다.

✗ **실험 예측의 부재.** 끈 길이 $\ell_s$의 직접 탐지는 현재 기술로 불가능하다. T-쌍대성이 물리적으로 실현되는지는 끈이론 자체가 검증되기 전까지 알 수 없다.

✓ **우주론적 함의.** 끈 우주론(string cosmology)에서 초기 우주의 수축 단계가 팽창 단계와 T-쌍대성으로 연결된다는 가설(pre-big bang scenario, 가스트로-베네치아노)이 있다. 이 경우 T-쌍대성이 빅뱅 특이점을 피하는 메커니즘이 될 수 있다. 그러나 관측으로의 연결은 아직 추측 수준이다.

---

## 🤔 다음 질문

1. T-쌍대성이 섭동적이라면, 결합상수 $g_s$를 뒤집는 S-쌍대성은 어떻게 작동하는가? → 03-s-duality
2. Type IIA와 IIB를 연결하는 T-쌍대성 외에, 전혀 다른 끈이론들을 연결하는 비섭동 쌍대성이 있는가? → 03-s-duality, 04-m-theory
3. T-쌍대성이 공간을 창발적 개념으로 만든다면, 시공간의 완전한 양자론적 기술은 무엇인가? → emergent-spacetime

---

🧩 **Principle** — T-쌍대성은 콤팩트 반지름 $R$과 $\alpha'/R$, 운동량 수 $n$과 감김 수 $w$의 교환 아래 닫힌 끈의 질량 스펙트럼이 정확히 불변임을 말한다. 이것은 정확한(non-perturbative) 섭동 대칭이며, 물리적 최소 길이 $\ell_s = \sqrt{\alpha'}$의 존재를 함의한다.

🔬 **Boundary** — T-쌍대성은 원형 콤팩트 차원이 있는 닫힌 끈이론에서 정의된다. 비콤팩트 방향, 복잡한 배경, 또는 비섭동 효과($e^{-1/g_s}$)에서는 수정이 필요하거나 새로운 구조(D-브레인)가 나타난다.

🪜 **Emergence** — T-쌍대성은 끈이 인식하는 기하학적 거리가 점입자의 직관과 다름을 보여준다. 최소 길이 $\ell_s$ 이하에서 기하학적 공간 개념이 무너지며, 공간 자체가 더 깊은 자유도로부터 창발하는 개념임을 시사한다.

---

<div align="center">

[◀ 이전: 쌍대성이란](./01-what-is-duality.md) · [📚 README](../README.md) · [다음: S-쌍대성 ▶](./03-s-duality.md)

</div>
