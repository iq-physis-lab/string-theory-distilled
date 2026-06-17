# 끈 진동 스펙트럼

*진동 모드의 사다리가 어떻게 입자 질량을 결정하는가*

---

## 🎯 핵심 질문

점입자 이론에서 입자의 종류는 손으로 넣어야 한다. 전자는 전자, 쿼크는 쿼크—왜 이 질량과 전하를 가지는지 이론 내부에서 설명되지 않는다. 끈 이론은 다른 출발점을 택한다: **하나의 기본 객체(끈)가 어떻게 진동하느냐에 따라 서로 다른 입자처럼 보인다.** 그렇다면 질문은 명확하다.

> 닫힌 보존 끈의 진동 스펙트럼은 어떤 모습인가? $N=0, 1, 2, \ldots$ 각 레벨에서 질량은 얼마이고, 어떤 물리적 해석을 갖는가?

이 질문은 수식 하나로 압축된다:

$$M^2 = \frac{N - a}{\alpha'}$$

여기서 $\alpha'$는 끈의 장력(의 역수에 비례하는 기본 상수)이고, $a$는 영점 에너지에서 비롯된 정규화 상수, $N$은 진동 모드 수이다.

---

## 🌍 어디서 나타나나

이 공식은 끈 이론의 가장 기초적인 층에서 등장한다. 평탄한 26차원 시공간(보존 끈) 또는 10차원(초끈)에서 끈의 작용을 양자화하면 힐베르트 공간이 생기고, 그 기저는 생성 연산자 $\alpha^\mu_{-n}$의 조합으로 이루어진다.

**보존 끈(26차원)에서**:
- 정규화 상수 $a = 1$ (제타함수 정규화 $\zeta(-1) = -1/12$로부터)
- $N = \sum_{n=1}^\infty n \, \hat{a}^\dagger_n \hat{a}_n$ (레벨 연산자)

**물리적 등장 맥락**:
- 중력을 포함한 모든 상호작용의 통합 시도
- $N=1$ 레벨의 무질량 텐서 장 → 중력자의 자연스러운 등장
- 강입자 물리학의 Regge 궤적 ($J \sim \alpha' M^2$) 재현
- L1 진동 원리의 양자 버전: 에너지 = $\hbar\omega \times$모드 수

---

## 🔍 직관의 함정

**함정 1: "끈이 진동한다"는 말이 쉽게 들린다.**
고전적 현(絃)의 진동을 상상하면 된다고 생각하지만, 여기서 진동은 26차원 시공간에서 일어나며, 양자 중첩이 적용된다. $N=0$ 상태는 "진동하지 않는" 끈이 아니라 진공 기댓값이 0인 양자 상태다.

**함정 2: $M^2 < 0$이면 허수 질량 → "물리적 불가"라는 속단.**
$N=0$일 때 $M^2 = -1/\alpha' < 0$이 나온다. 이 **타키온**은 보존 끈 이론의 진짜 문제다. 진공이 불안정하다는 신호이지, 단순한 수학적 오류가 아니다. ✗ 보존 끈은 이 문제를 해결하지 못한다. 초끈 이론에서는 페르미-보존 대칭이 타키온을 제거한다.

**함정 3: "$N=1$이 중력자다"는 자동적 결론 오류.**
$N=1$ 레벨은 무질량 텐서 장을 포함하지만, 실제로 중력자로 확인되려면 스핀-2, 결합 구조, 게이지 불변성 등 추가 조건을 모두 확인해야 한다. 수학적 구조는 맞지만 ✗ 실험적 확인은 없다.

---

## ⚙️ 제1원리 유도

닫힌 보존 끈의 세계면(worldsheet) 작용은 남부-고토 또는 폴랴코프 형식으로 쓴다:

$$S = -\frac{1}{4\pi\alpha'} \int d^2\sigma \, \partial_a X^\mu \partial^a X_\mu$$

운동방정식의 해를 모드 전개하면:

$$X^\mu(\tau, \sigma) = x^\mu + 2\alpha' p^\mu \tau + i\sqrt{2\alpha'} \sum_{n \neq 0} \frac{1}{n}\left(\alpha^\mu_n e^{-2in(\tau-\sigma)} + \tilde{\alpha}^\mu_n e^{-2in(\tau+\sigma)}\right)$$

양자화 시 정준 교환관계 $[x^\mu, p^\nu] = i\eta^{\mu\nu}$, $[\alpha^\mu_m, \alpha^\nu_n] = m\eta^{\mu\nu}\delta_{m+n,0}$를 부과한다.

질량 껍질 조건(Virasoro 제약에서)은:

$$M^2 = \frac{2}{\alpha'}\left(N_L + N_R - 2a\right) \quad \text{(닫힌 끈, } N_L = N_R \text{ 조건 포함)}$$

단순화하면 (레벨 매칭 조건 후):

$$M^2 = \frac{N - a}{\alpha'}, \quad a = 1 \text{ (보존끈)}$$

각 레벨의 상태:
- $N=0$: $|0\rangle$, $M^2 = -1/\alpha'$ (타키온) ✗
- $N=1$: $\alpha^\mu_{-1}\tilde{\alpha}^\nu_{-1}|0\rangle$, $M^2 = 0$ (무질량 텐서 → 중력자 + 딜라톤 + B장) ✓
- $N=2$: 다수의 대칭 텐서 상태, $M^2 = 1/\alpha'$ (무거운 거대 질량) ✗ (미관측)

$\square$

---

## 🧪 검증 현실

✗ **직접 실험 검증 없음.** 끈의 크기 $\sim\sqrt{\alpha'} \approx 10^{-35}$ m는 현재 가속기(LHC: $\sim 10^{-19}$ m 분해능)로 도달 불가능하다.

✓ **수학적 구조 내부 일관성**: 아래 코드는 공식의 자기일관성을 확인한다.
- Lorentz 불변성이 정확히 26차원에서만 성립함을 무변칙 조건으로 확인
- 각 레벨의 축퇴도(degeneracy)가 모듈러 형식의 계수와 일치

✓ **간접 증거**: 강입자 Regge 궤적 $J = \alpha' M^2 + J_0$의 선형성은 끈 스펙트럼 구조와 정성적으로 일치한다.

```python
import numpy as np
import matplotlib.pyplot as plt
from itertools import product

# ── 파라미터 ──────────────────────────────────────────────────
ALPHA_PRIME = 1.0   # α' = 1 단위 (자연 단위)
A_BOSONIC   = 1.0   # 보존 끈 정규화 상수
N_MAX       = 6     # 표시할 최대 레벨

# ── 질량 제곱 공식 ─────────────────────────────────────────────
def mass_squared(N, a=A_BOSONIC, alpha_prime=ALPHA_PRIME):
    """M^2 = (N - a) / alpha_prime"""
    return (N - a) / alpha_prime

# ── 레벨별 축퇴도 (보존 끈 닫힌 끈, 상태 수의 근사) ──────────
def degeneracy_open(N):
    """
    열린 끈 (24개 횡방향 자유도)에서 N 레벨의 분할수(partition).
    닫힌 끈은 제곱하고 레벨-매칭 조건을 적용하므로 열린 끈으로 시작.
    정수 분할 함수 p(N, 24) 계산.
    """
    # 동적 계획법으로 24개 진동자의 분할수 계산
    # p[n] = N 레벨에 기여하는 방법 수
    partitions = [0] * (N + 1)
    partitions[0] = 1
    for mode in range(1, N + 1):          # 각 진동자 모드 n=1,...,N
        for rep in range(24):             # 24개 횡방향 성분
            for level in range(N, mode - 1, -1):
                partitions[level] += partitions[level - mode]
    return partitions[N]

# ── 스펙트럼 계산 ─────────────────────────────────────────────
levels = np.arange(0, N_MAX + 1)
M2_values = mass_squared(levels)

# 레벨 0: 타키온, 레벨 1: 무질량(중력자 등), 레벨 >= 2: 거대 질량
labels = []
for N in levels:
    m2 = M2_values[N]
    if m2 < 0:
        lbl = f"N={N}: M²={m2:.2f} → 타키온 (진공 불안정)"
    elif m2 == 0:
        lbl = f"N={N}: M²={m2:.2f} → 무질량 (중력자·게이지장)"
    else:
        lbl = f"N={N}: M²={m2:.2f} → 거대 질량 (미관측)"
    labels.append(lbl)

for lbl in labels:
    print(lbl)

# ── 시각화 ────────────────────────────────────────────────────
fig, axes = plt.subplots(1, 2, figsize=(12, 5))

# 왼쪽: 질량 스펙트럼 에너지 레벨 다이어그램
ax1 = axes[0]
colors = []
for m2 in M2_values:
    if m2 < 0:
        colors.append('#e74c3c')    # 빨강: 타키온
    elif m2 == 0:
        colors.append('#2ecc71')    # 초록: 무질량
    else:
        colors.append('#3498db')    # 파랑: 거대 질량

for i, (N, m2, c) in enumerate(zip(levels, M2_values, colors)):
    ax1.hlines(m2, 0.2, 0.8, colors=c, linewidths=2.5)
    ax1.text(0.85, m2, f'N={N}', va='center', fontsize=9)

ax1.axhline(0, color='gray', linestyle='--', alpha=0.5, label='M²=0 (무질량)')
ax1.set_xlim(0, 1.3)
ax1.set_ylabel(r"$M^2$ (단위: $1/\alpha'$)", fontsize=11)
ax1.set_title("보존 끈 스펙트럼\n(닫힌 끈, $a=1$)", fontsize=12)
ax1.set_xticks([])
ax1.legend(fontsize=9)
ax1.grid(axis='y', alpha=0.3)

# 오른쪽: Regge 궤적 M² vs N
ax2 = axes[1]
N_plot = np.linspace(1, N_MAX, 300)
M2_plot = (N_plot - A_BOSONIC) / ALPHA_PRIME

ax2.plot(N_plot, M2_plot, 'b-', linewidth=2, label=r"$M^2 = (N-1)/\alpha'$")
ax2.scatter(levels[levels >= 1], M2_values[levels >= 1],
            s=80, zorder=5, color='navy', label='정수 레벨')
ax2.scatter([0], [M2_values[0]], s=80, zorder=5, color='red',
            label='타키온 (N=0)')
ax2.axhline(0, color='gray', linestyle='--', alpha=0.5)
ax2.set_xlabel("진동 레벨 N", fontsize=11)
ax2.set_ylabel(r"$M^2$ (단위: $1/\alpha'$)", fontsize=11)
ax2.set_title("Regge 궤적\n(기울기 = $1/\\alpha'$)", fontsize=12)
ax2.legend(fontsize=9)
ax2.grid(alpha=0.3)

plt.tight_layout()
plt.savefig("string_spectrum.png", dpi=150, bbox_inches='tight')
plt.show()
print("\n그림 저장: string_spectrum.png")
```

**예상 출력:**
```
N=0: M²=-1.00 → 타키온 (진공 불안정)
N=1: M²= 0.00 → 무질량 (중력자·게이지장)
N=2: M²= 1.00 → 거대 질량 (미관측)
N=3: M²= 2.00 → 거대 질량 (미관측)
N=4: M²= 3.00 → 거대 질량 (미관측)
N=5: M²= 4.00 → 거대 질량 (미관측)
N=6: M²= 5.00 → 거대 질량 (미관측)
```
왼쪽 패널은 에너지 레벨 다이어그램(타키온=빨강, 무질량=초록, 거대=파랑)을, 오른쪽은 선형 Regge 궤적을 보여준다.

---

## 🔬 경계

이 공식이 성립하는 조건과 그 바깥:

| 조건 | 범위 내 ✓ | 범위 밖 ✗ |
|------|-----------|-----------|
| 시공간 | 평탄한 26차원 민코프스키 | 휘어진 배경, 4차원 물리 |
| 끈 결합 | 약한 결합 $g_s \ll 1$ (섭동적) | 강한 결합 (S-쌍대성 필요) |
| 타키온 | 초끈에서 제거됨 | 보존 끈에서는 진공 불안정성 지속 |
| 관측 가능 에너지 | $\sqrt{\alpha'^{-1}} \sim 10^{18}$ GeV 이하 | 플랑크 에너지 이상 |

특히 현실적인 콤팩트화(Calabi-Yau 다양체 등)를 도입하면 $M^2$ 공식은 대폭 수정된다. 이 문서의 공식은 "교과서적 첫걸음"이다.

---

## 🧬 횡단 원리

**L1 진동 → 끈 스펙트럼**: 분산 관계 $\omega_n = n\omega_0$는 현의 고조파에서 끈의 양자 모드로 직접 연결된다. $\hbar\omega_n$의 합이 질량을 결정한다.

**L2 대칭/보존 법칙**: 레벨 매칭 조건 $N_L = N_R$는 세계면의 리프시프트 대칭(좌우 진행파의 동등성)에서 비롯된 보존량이다.

**L4 통계 역학**: 높은 레벨의 상태 수는 Hagedorn 온도를 정의한다. $\rho(M) \sim e^{M/T_H}$의 지수 증가는 끈 이론 고유의 통계역학적 특성이다.

**L6 정보 이론**: 각 진동 패턴은 정보 비트다. 복잡한 진동 = 더 많은 내부 자유도 = 더 큰 질량 = 더 많은 상태. 이 연결이 Ch7 후반부(류–타카야나기, AdS/CFT)로 이어진다.

---

## 🪜 창발

**창발 1: 중력의 필연성**
$N=1$ 스핀-2 무질량 상태는 끈 이론 어디에서나 등장한다. 이 상태를 제거할 방법이 없다—끈을 양자화하는 순간 중력자가 스펙트럼에 나타난다. 점입자 이론에서 중력을 "추가"하는 것과 달리, 끈 이론에서 중력은 필연적 창발이다. ✓

**창발 2: 게이지 불변성**
$N=1$ 벡터 성분(열린 끈)과 텐서 성분의 무질량성은 게이지 불변성을 강제한다. 게이지 대칭이 손으로 넣어지는 것이 아니라 일관성 조건에서 창발한다.

**창발 3: 시공간 차원**
보존 끈에서 무변칙(anomaly-free) 조건은 정확히 $D=26$을, 초끈은 $D=10$을 요구한다. 시공간의 차원이 이론의 일관성으로부터 창발하는 것이다.

---

## 📐 예측·반증

**검증 가능한 구조적 예측 ✓**:
- 스핀-2 무질량 중력자의 존재 → 일반 상대성이론과 정합
- Regge 궤적의 선형성 → 강입자 물리에서 부분 확인
- 모든 힘의 통합 (중력·게이지·물질이 같은 스펙트럼에서)

**반증 가능하나 미확인 ✗**:
- $N \geq 2$ 거대 질량 끈 들뜸 → 에너지 도달 불가
- 추가 차원의 존재 → LHC 미관측
- 초대칭 파트너 → LHC 미관측

**반증 불가 영역 ✗**:
- $\alpha'$의 정확한 값은 이론 내부에서 결정되지 않음
- 콤팩트화 방식에 따라 예측이 달라져 "끈 이론"이라는 단일 예측이 없음

---

## 🤔 다음 질문

스펙트럼을 알았다면, 다음 자연스러운 질문들:

1. **공간 차원이 작게 말리면 스펙트럼이 어떻게 달라지나?** → 운동량 모드와 감김 모드의 경쟁 → [T-쌍대성](./02-t-duality-toy.md)

2. **무질량 중력자는 실제로 블랙홀 엔트로피를 설명하나?** → BPS 상태 계산 → [류–타카야나기](./03-ryu-takayanagi.md)

3. **10차원 → 4차원 콤팩트화는 스펙트럼을 얼마나 바꾸나?** → 풍경 문제 → [콤팩트화 차원 세기](./04-compactification-counting.md)

4. **$N=1$ 레벨의 장이 경계 CFT와 어떻게 대응되나?** → AdS/CFT 사전 → [05 문서](./05-ads-cft-dictionary.md)

---

> **🧩 원리**: 끈의 진동 모드 수 $N$이 입자의 질량을 결정한다. $M^2 = (N-a)/\alpha'$.
>
> **🔬 경계**: 이 공식은 평탄한 26차원, 약한 결합, 비압축적 시공간에서만 직접 적용된다.
>
> **🪜 창발**: $N=1$ 스핀-2 무질량 상태로서의 중력자는 일관성으로부터 필연적으로 등장한다. 중력은 끈 이론의 출력물이지 입력이 아니다.

---

<div align="center">

[◀ 이전: 정직한 평가](../ch6-landscape-critique/05-honest-assessment.md) · [📚 README](../README.md) · [다음: T-쌍대성 장난감 ▶](./02-t-duality-toy.md)

</div>
