# 끈의 작용

*세계면의 넓이를 최소화하는 원리에서 끈의 운동 방정식과 비라소로 구속이 유도된다.*

---

## 🎯 핵심 질문

물리학에서 어떤 계의 역학을 기술하려면 **작용(action)**이 필요하다. 점입자에게는 세계선의 길이가 작용이었다. 끈에게는 무엇이 작용인가? 그 작용으로부터 어떻게 운동 방정식이 나오고, 끈 이론 특유의 구속 조건인 **비라소로 조건(Virasoro constraints)**은 어디서 오는가?

이 문서에서는 두 가지 등가적인 작용 형식을 소개한다. 첫 번째는 기하학적으로 직관적인 **남부–고토(Nambu–Goto) 작용**, 두 번째는 계산에 편리한 **폴랴코프(Polyakov) 작용**이다. 두 작용이 어떤 의미에서 동등한지, 그리고 폴랴코프 작용이 왜 더 강력한 도구인지를 설명한다. (→ L0 variational)

---

## 🌍 어디서 나타나나

끈 이론의 작용 원리는 고전역학의 최소 작용 원리의 직접적 확장이다. 뉴턴 역학에서 최소 작용 원리는 (→ L0 variational):

$$
\delta S = 0, \quad S = \int dt\, L(q, \dot{q})
$$

특수 상대성이론에서 점입자의 작용은 세계선의 고유 길이다:

$$
S_{\text{particle}} = -m \int d\tau \sqrt{-\eta_{\mu\nu}\dot{X}^\mu \dot{X}^\nu}
$$

끈 이론은 이것을 한 차원 올린다. 끈은 시공간에서 2차원 **세계면(worldsheet)**을 쓸어낸다. 가장 자연스러운 작용은 이 세계면의 넓이다.

이 접근은 보소닉(bosonic) 끈 이론의 출발점이며, 초끈(superstring) 이론에서도 보소닉 부분의 구조는 동일하게 유지된다.

---

## 🔍 직관의 함정

**함정 1: "남부–고토 작용이 더 근본적이다."**

남부–고토 작용은 기하학적으로 단순명료하다 — 세계면 넓이. 그러나 이것은 제곱근을 포함하므로 양자화가 매우 어렵다. 폴랴코프 작용은 **보조 계량**을 도입하여 이 제곱근을 제거한다. 보조 계량을 도입하고 그것을 적분하면(또는 방정식으로 소거하면) 남부–고토로 돌아온다. 따라서 두 작용은 **온쉘(on-shell)**에서 동등하지만, 계산 도구로는 폴랴코프가 훨씬 우월하다.

**함정 2: "재매개변수화 대칭은 그냥 좌표 선택이다."**

재매개변수화 대칭은 물리적 내용에 영향을 주지 않는 것처럼 보이지만, 실제로는 이론의 자유도를 줄이는 **게이지 대칭**이다. 이 대칭을 이용해 특별한 좌표계(공형 게이지, light-cone 게이지)를 선택하면 운동 방정식이 크게 단순해진다. 그 과정에서 남은 잔여 대칭이 **등각 대칭**이며, 이것이 세계면 이론을 2차원 등각장론(2d CFT)으로 만든다.

**함정 3: "비라소로 조건은 부가 조건이다."**

비라소로 조건은 "별도로 붙이는" 것이 아니다. 이것은 폴랴코프 작용에서 보조 계량의 운동 방정식으로부터 **자동으로** 나온다. 에너지-운동량 텐서가 0이 된다는 조건이 바로 비라소로 조건이다. 양자 수준에서 이 조건은 비라소로 대수(Virasoro algebra)로 발전하며, 임계 차원 $D = 26$의 기원이 된다.

---

## ⚙️ 제1원리 유도

### 남부–고토 작용

세계면을 내부 좌표 $\xi^a = (\tau, \sigma)$로 매개변수화하자. 시공간 좌표는 $X^\mu(\tau, \sigma)$이며 $\mu = 0, 1, \ldots, D-1$. 세계면이 시공간에서 유도하는 계량은:

$$
h_{ab} = \eta_{\mu\nu}\, \partial_a X^\mu\, \partial_b X^\nu
$$

여기서 $\eta_{\mu\nu} = \text{diag}(-1, +1, \ldots, +1)$은 $D$차원 민코프스키 계량이다. 남부–고토 작용은 세계면 넓이:

$$
\boxed{S_{\text{NG}} = -\frac{1}{2\pi\alpha'} \int d\tau\, d\sigma\, \sqrt{-\det(h_{ab})}}
$$

$T = 1/(2\pi\alpha')$를 **끈의 장력(string tension)**이라 한다. $\alpha'$는 차원 $[\text{length}]^2$를 가지며 끈의 크기를 결정한다.

### 폴랴코프 작용

남부–고토의 제곱근을 피하기 위해 독립적인 세계면 계량 $\gamma_{ab}(\tau, \sigma)$를 보조 변수로 도입한다:

$$
\boxed{S_{\text{P}} = -\frac{1}{4\pi\alpha'} \int d\tau\, d\sigma\, \sqrt{-\gamma}\, \gamma^{ab}\, \partial_a X^\mu\, \partial_b X_\mu}
$$

여기서 $\gamma = \det(\gamma_{ab})$, $\gamma^{ab}$는 역계량이다.

**두 작용의 동등성 증명:** $\gamma_{ab}$에 대한 운동 방정식을 구한다. $S_{\text{P}}$를 $\gamma^{ab}$에 대해 변분하면:

$$
\frac{\delta S_{\text{P}}}{\delta \gamma^{ab}} = 0 \implies T_{ab} \equiv \partial_a X^\mu \partial_b X_\mu - \frac{1}{2}\gamma_{ab}\, \gamma^{cd}\, \partial_c X^\mu \partial_d X_\mu = 0
$$

이것이 **에너지-운동량 텐서의 영(零) 조건**이다. 이 방정식을 풀면:

$$
\gamma_{ab} = e^{2\phi} h_{ab}
$$

즉, 세계면 계량은 유도 계량에 비례한다. 이를 $S_{\text{P}}$에 대입하면:

$$
S_{\text{P}}\big|_{\text{on-shell}} = -\frac{1}{4\pi\alpha'} \int d\tau\, d\sigma\, \sqrt{-h}\, h^{ab}\, h_{ab} = -\frac{1}{4\pi\alpha'} \int d\tau\, d\sigma\, \sqrt{-h} \cdot 2 = S_{\text{NG}}
$$

$h^{ab} h_{ab} = \delta^a{}_a = 2$ (2차원 세계면이므로). $\square$

### 대칭

폴랴코프 작용은 다음 세 가지 대칭을 가진다:

**1. 재매개변수화 불변성:** $\xi^a \to \tilde{\xi}^a(\xi)$ 변환 아래 $S_{\text{P}}$는 불변이다. 계량은 텐서처럼 변환되고 $X^\mu$는 스칼라처럼 변환된다.

**2. 바일(Weyl) 불변성:** $\gamma_{ab} \to e^{2\omega(\xi)}\gamma_{ab}$ 변환 아래 $S_{\text{P}}$는 불변이다. 확인:

$$
\sqrt{-\gamma} \to e^{2\omega}\sqrt{-\gamma}, \quad \gamma^{ab} \to e^{-2\omega}\gamma^{ab}
$$

두 인자가 상쇄되므로 $S_{\text{P}}$는 불변이다. 이 바일 불변성이 2차원 등각 대칭의 기원이다.

**3. 폰카레 불변성:** 표적 시공간(target space)의 폰카레 변환 $X^\mu \to \Lambda^\mu{}_\nu X^\nu + a^\mu$.

### 등각 게이지와 운동 방정식

재매개변수화 대칭과 바일 대칭을 이용해 **등각 게이지(conformal gauge)**를 선택한다:

$$
\gamma_{ab} = e^{2\phi(\tau,\sigma)} \eta_{ab}, \quad \eta_{ab} = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}
$$

등각 게이지에서 $S_{\text{P}}$는 더욱 단순해진다 ($\phi$ 인자가 상쇄):

$$
S_{\text{P}} = -\frac{1}{4\pi\alpha'} \int d\tau\, d\sigma\, \eta^{ab}\, \partial_a X^\mu\, \partial_b X_\mu = \frac{1}{4\pi\alpha'} \int d\tau\, d\sigma\, \left[(\dot{X})^2 - (X')^2\right]
$$

여기서 $\dot{X}^\mu = \partial_\tau X^\mu$, $X'{}^\mu = \partial_\sigma X^\mu$. 오일러-라그랑주 방정식:

$$
\frac{\delta S_{\text{P}}}{\delta X_\mu} = 0 \implies \left(-\partial_\tau^2 + \partial_\sigma^2\right) X^\mu = 0
$$

즉, $X^\mu$는 2차원 **파동 방정식**을 만족한다! $\square$

### 비라소로 구속 조건

등각 게이지를 선택하더라도 에너지-운동량 텐서의 영(零) 조건은 **구속 조건**으로 남는다:

$$
T_{ab} = 0 \implies \begin{cases} T_{00} = \tfrac{1}{2}[(\dot{X})^2 + (X')^2] = 0 \\ T_{01} = \dot{X} \cdot X' = 0 \end{cases}
$$

빛뿔 좌표 $\xi^\pm = \tau \pm \sigma$에서 이 조건은:

$$
T_{++} = \partial_+ X^\mu \partial_+ X_\mu = 0, \quad T_{--} = \partial_- X^\mu \partial_- X_\mu = 0
$$

이것이 **비라소로 구속 조건(Virasoro constraints)**이다. 정현파 모드로 전개하면 모드 계수 $L_m$이 되고, 이것이 비라소로 대수를 이룬다. (→ `03-vibration-modes-particles.md`)

### 경계 조건

$\sigma$ 방향의 경계에서 표면항의 소거 조건을 분석하면:

$$
\delta S_{\text{P}} \supset -\frac{1}{2\pi\alpha'} \int d\tau\, X'_\mu \delta X^\mu \Big|_{\sigma=0}^{\sigma=\pi} = 0
$$

이것은 두 가지 방식으로 만족된다:

- **노이만(Neumann) 경계 조건** (열린 끈): $X'^\mu\big|_{\sigma=0,\pi} = 0$
- **주기적(periodic) 경계 조건** (닫힌 끈): $X^\mu(\tau, \sigma + 2\pi) = X^\mu(\tau, \sigma)$

열린 끈과 닫힌 끈은 서로 다른 경계 조건을 가지며, 이로부터 서로 다른 진동 스펙트럼이 나온다. 닫힌 끈의 스펙트럼에서 스핀-2 중력자가 나온다. (→ `04-graviton-necessity.md`)

---

## 🧪 검증 현실

**중요한 전제:** 끈이론은 직접적인 실험 검증이 없다. 아래의 "검증"은 수학적 구조의 내부 일관성 확인이다.

**✓ 확립: 폴랴코프 작용의 경로 적분**

폴랴코프 작용의 경로 적분은 엄밀하게 정의된다. 세계면 위상을 위상수(genus $g$)로 분류하면, 각 위상에서의 적분이 유한함이 수학적으로 확인된다. 이것이 끈 이론의 UV 유한성의 기반이다.

**✓ 확립: 바일 이상(Weyl anomaly)과 임계 차원**

등각 게이지에서 바일 대칭이 양자 수준에서 이상(anomaly)을 가지는지 여부가 중요하다. 이상이 없으려면 중심 전하(central charge)가 0이어야 한다. 보소닉 끈에서 $X^\mu$ 각각의 기여는 $c = 1$이므로 $D$개 좌표의 기여는 $c_X = D$. 고스트 기여는 $c_{\text{ghost}} = -26$. 일관성 조건:

$$
c_{\text{total}} = D + (-26) = 0 \implies D = 26
$$

이것이 보소닉 끈의 임계 차원 $D = 26$의 유도다. 수학적으로 엄밀한 결과다.

**Python 시연: 폴랴코프 작용 변분**

```python
import numpy as np
import matplotlib.pyplot as plt

# 단순화된 1+1차원 세계면에서 폴랴코프 작용의 수치 변분
# X^mu = (X^0, X^1) 두 성분만 고려

N_tau, N_sigma = 50, 50
tau = np.linspace(0, np.pi, N_tau)
sigma = np.linspace(0, np.pi, N_sigma)
dtau = tau[1] - tau[0]
dsigma = sigma[1] - sigma[0]

# 배경: 단순 진행파 X^1 = A * cos(tau) * cos(sigma)
A = 0.5
T, S = np.meshgrid(tau, sigma, indexing='ij')
X0 = T  # 시간성분 (gauge)
X1 = A * np.cos(T) * np.cos(S)

# 편미분 수치 계산
dX0_dtau = np.gradient(X0, dtau, axis=0)
dX0_dsigma = np.gradient(X0, dsigma, axis=1)
dX1_dtau = np.gradient(X1, dtau, axis=0)
dX1_dsigma = np.gradient(X1, dsigma, axis=1)

# 유도 계량 성분 h_ab = eta_mu_nu * dX^mu_a * dX^nu_b
# eta = diag(-1, +1), 등각 게이지에서 gamma_ab = eta_ab
# S_P ∝ ∫ [-(dX0/dtau)^2 + (dX1/dtau)^2 + (dX0/dsigma)^2 - (dX1/dsigma)^2] dtau dsigma
integrand = (-(dX0_dtau**2) + (dX1_dtau**2)
             + (dX0_dsigma**2) - (dX1_dsigma**2))
action = np.trapz(np.trapz(integrand, dx=dsigma, axis=1), dx=dtau)

# 파동 방정식 잔차 확인
d2X1_dtau2 = np.gradient(dX1_dtau, dtau, axis=0)
d2X1_dsigma2 = np.gradient(dX1_dsigma, dsigma, axis=1)
wave_residual = d2X1_dtau2 - d2X1_dsigma2  # 운동방정식 위반량

print(f"폴랴코프 작용 S_P ∝ {action:.6f}")
print(f"파동방정식 잔차 RMS: {np.sqrt(np.mean(wave_residual**2)):.2e}")
print(f"(진행파는 파동방정식을 정확히 만족하므로 잔차 ≈ 0)")

# 비라소로 구속 확인: T_{01} = dot{X} . X' = 0
T01 = (dX0_dtau * dX0_dsigma) * (-1) + (dX1_dtau * dX1_dsigma) * (+1)
print(f"비라소로 T_01 최대값: {np.max(np.abs(T01)):.2e}")
```

---

## 🔬 경계

**확립된 것:**
- 남부–고토와 폴랴코프 작용의 온쉘 동등성 — 수학적으로 엄밀
- 등각 게이지에서의 운동 방정식(2차원 파동 방정식) — 확립
- 비라소로 구속 조건의 도출 — 확립
- 보소닉 끈의 임계 차원 $D = 26$ — 바일 이상 소거 조건에서 확립

**유망하나 완전하지 않은 것:**
- 폴랴코프 작용의 경로 적분의 수학적 엄밀성 — 위상수 $g \leq 1$에서 확립, $g \geq 2$에서 완전히 엄밀한 정의는 활발한 연구 주제

**미배달:**
- 끈의 장력 $T = 1/(2\pi\alpha')$ 의 값을 제1원리로부터 예측 — 현재 실험 입력 필요
- 비평탄 배경 시공간에서의 완전한 비선형 끈 이론 — 부분적으로만 이해됨

---

## 🧬 횡단 원리

**최소 작용 원리의 보편성:** 폴랴코프 작용은 표적 시공간의 스칼라장 $X^\mu$를 세계면 위에서 정의된 2차원 QFT로 해석할 수 있다. 이 관점에서 끈 이론은 **2차원 등각장론(2d CFT)**이며, 통계역학의 임계 현상, 리만 곡면 이론과 깊이 연결된다.

**대칭과 구속:** 바일 대칭이 게이지 대칭으로서 구속 조건(비라소로)을 만드는 패턴은 일반 상대성이론에서 미분 동형 대칭이 에너지-운동량 텐서 보존을 만드는 패턴과 동일하다. (→ L4 GR)

**양자 이상(anomaly):** 고전적으로 존재하는 대칭이 양자화 과정에서 깨지는 이상(anomaly) 현상이 임계 차원을 결정한다. 이것은 QFT 전반에 걸쳐 나타나는 근본 원리다. (→ L3 QFT)

---

## 🪜 창발

폴랴코프 형식에서 2차원 세계면 이론은 $D$차원 시공간에 사는 $D$개의 스칼라장을 포함한다. 그런데 일관성 조건($D = 26$ 또는 초끈에서 $D = 10$)이 목적 시공간의 차원을 **고정**한다. 2차원 세계면 이론의 내부 조건으로부터 더 높은 차원의 시공간이 출현하는 것이다.

이 창발 패턴은 AdS/CFT 대응(→ holographic-principle)에서 극단적으로 확장된다: $d$차원 게이지 이론으로부터 $(d+1)$차원 중력 이론이 창발한다.

---

## 📐 예측·반증

**이론 내부의 예측:**
- 보소닉 끈: 임계 차원 $D = 26$, 타키온 존재 (질량² < 0), 스핀-2 무질량 중력자
- 초끈: 임계 차원 $D = 10$, 타키온 없음, 페르미온 존재

**반증 시나리오:**
- 만약 세계면 이론이 바일 이상 없이 $D = 26$ 이외의 차원에서도 일관되게 양자화됨이 증명된다면, 임계 차원 논증이 흔들린다.
- 폴랴코프 경로 적분의 높은 위상수 기여가 발산함이 증명된다면, UV 유한성 주장이 위협받는다.

---

## 🤔 다음 질문

1. 파동 방정식의 해를 푸리에 모드로 전개하면 어떤 진동 패턴이 나오는가? 각 모드는 어떤 입자에 해당하는가? (→ `03-vibration-modes-particles.md`)
2. 닫힌 끈의 진동 스펙트럼에 반드시 스핀-2 입자가 있는 이유는 무엇인가? (→ `04-graviton-necessity.md`)
3. 보소닉 끈의 타키온 문제는 어떻게 해결되는가? 초끈이론은 무엇을 추가하는가? (→ `../ch3-superstrings/01-superstring-intro.md`)
4. 컴팩트 차원에서의 경계 조건은 어떻게 달라지는가? (→ `../ch2-extra-dimensions/`)

---

🧩 **Principle** — 세계면 넓이를 최소화하는 남부–고토 작용은 폴랴코프 형식으로 선형화되고, 보조 계량의 운동 방정식이 비라소로 구속을 생성하며, 바일 이상 소거가 임계 차원을 결정한다.

🔬 **Boundary** — ✓ 확립: 폴랴코프-남부고토 동등성 $\square$, 비라소로 구속 유도, 임계 차원 $D=26$. ✗ 미배달: 끈 장력의 제1원리 예측, 일반 배경에서의 완전한 이론.

🪜 **Emergence** — 2차원 세계면의 일관성 조건이 10/26차원 시공간을 창발시키고, 이 창발 패턴이 AdS/CFT에서 $(d+1)$차원 시공간의 홀로그래픽 창발로 일반화된다.

---

<div align="center">

[◀ 이전: 왜 끈인가](./01-why-strings.md) · [📚 README](../README.md) · [다음: 진동 모드 = 입자 ▶](./03-vibration-modes-particles.md)

</div>
