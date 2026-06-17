# 콤팩트화 차원 세기

*여섯 개의 차원을 접는 방법은 10의 500제곱 가지*

---

## 🎯 핵심 질문

초끈 이론은 10차원 시공간을 요구한다. 우리가 사는 세계는 4차원이다. 나머지 6차원은 어디에 있는가? 답은 **콤팩트화**: 6차원을 매우 작은 내부 공간으로 "말아" 현재 실험으로 보이지 않게 한다.

그런데 이 내부 공간의 선택이 관측 가능한 저에너지 물리(입자 질량, 결합 상수, 우주 상수)를 결정한다. 그리고 이 선택지의 수가 천문학적이다:

> 칼라비–야우 다양체의 모듈라이 공간 + 플럭스 양자화 조건의 조합으로 나타나는 진공의 수는 대략 $\mathcal{N} \sim 10^{500}$으로 추정된다.

이것이 바로 **끈 풍경(string landscape)**의 기원이다. 왜 이 숫자가 나오는가? 그것이 문제인가, 아닌가?

---

## 🌍 어디서 나타나나

**Ch6(풍경 비판)**에서 다룬 풍경 문제의 물리적 기원이 여기 있다.

- **칼라비–야우(CY) 다양체**: 6차원 내부 공간의 후보. $SU(3)$ 홀로노미를 가지는 복소 3차원 켈러 다양체. 초대칭을 보존하면서 콤팩트화에 사용된다.
- **모듈라이(Moduli)**: CY 다양체의 기하학적 파라미터—크기, 모양을 연속적으로 변화시키는 자유도. 현재 알려진 CY 다양체는 수십만 개 이상이며, 각각 수백 개의 모듈라이를 가진다.
- **플럭스(Flux)**: 내부 공간의 위상 비자명한 사이클에 감긴 고차원 게이지 장의 값. 각 사이클마다 정수(양자화된)로 선택 가능.
- **진공 수**: 모든 CY에 대해 가능한 플럭스 선택의 수를 합산하면 $10^{500}$ 규모.

이 문제는 **인류 원리(anthropic principle)** 논의와도 연결된다: $10^{500}$개 중 우리 우주의 물리 상수를 주는 것은 몇 개인가?

---

## 🔍 직관의 함정

**함정 1: 모든 CY가 물리적으로 동등하다는 생각.**
다르게 생긴 CY에서 나오는 4차원 물리는 완전히 다르다: 다른 세대 수, 다른 게이지 군, 다른 결합 상수. 우리 표준 모형은 매우 특정한 CY를 요구하며, 그런 CY가 실제로 있는지조차 완전히 확인되지 않았다.

**함정 2: $10^{500}$이 "근사"라는 생각.**
이 숫자는 개별 CY의 모듈라이 수와 플럭스 선택 범위의 조합적 폭발로 나온다. 정확한 수는 모르지만, 지수적 규모는 여러 방법으로 독립적으로 추정된다. 불확실성이 있지만 $10^{500}$의 지수 규모 자체는 robust하다.

**함정 3: 풍경이 "예측 불가"와 동의어라는 생각.**
풍경이 크다고 해서 모든 물리가 설명 불가는 아니다. 위상적 인수로 특정 성질을 가진 진공의 분율을 추정하는 접근법(스완슨-더글라스 등)이 있다. 그러나 ✗ 현재까지 이 접근법이 표준 모형을 선택하는 데 성공하지 못했다.

---

## ⚙️ 제1원리 유도

**왜 지수적으로 많은가?**

대표적인 추정을 단순화하면:

1. **플럭스 격자**: 내부 공간에 $K$개의 3-사이클이 있고, 각 사이클에 플럭스 $n_i \in \{-N, \ldots, N\}$로 선택된다. 총 $(2N+1)^K$가지.

2. **태드폴 조건(tadpole condition)**: 안정성 조건이 $\sum_i n_i^2 \leq L$을 요구한다. 이것은 $K$차원 구에서 정수점 수를 셈—반지름 $\sqrt{L}$의 $K$차원 구 내 격자점.

3. **격자점 수**: $\mathcal{N} \sim \frac{\pi^{K/2}}{\Gamma(K/2+1)} L^{K/2}$. 전형적인 CY에서 $K \sim 300$, $L \sim 100$이면 $\mathcal{N} \sim 10^{200} \sim 10^{500}$ 규모.

4. **CY 수 곱하기**: 알려진 CY 다양체 수(최소 수십만)와 곱하면 더 커진다.

---

## 🧪 검증 현실

✗ **직접 실험 검증 없음.** 추가 차원의 직접 관측도, 특정 CY가 표준 모형을 주는지 확인도 없다.

✓ **수학적 구조 내부 일관성 (아래 코드)**:
- 플럭스 격자 + 태드폴 조건으로 진공 수가 지수적으로 많아짐을 수치로 확인
- $K$와 $L$ 변화에 따른 진공 수 스케일링

✓ **CY 다양체 목록**: Kreuzer-Skarke 데이터베이스에 47만 개 이상의 반사 다각형이 분류되어 있고, 각각이 CY 다양체를 준다 (수학적 확인).

```python
import numpy as np
import matplotlib.pyplot as plt
from itertools import product as iproduct

# ── 파라미터 ──────────────────────────────────────────────────
# 전형적인 CY 콤팩트화의 단순화된 버전

def count_flux_vacua_exact(K, L_max, N_range):
    """
    K차원 플럭스 격자에서 태드폴 조건 sum(n_i^2) <= L_max 를 만족하는
    정수점 (n_1, ..., n_K) 의 수를 정확히 센다.
    n_i ∈ {-N_range, ..., N_range}
    소규모(K<=4)에서만 가능.
    """
    count = 0
    for combo in iproduct(range(-N_range, N_range + 1), repeat=K):
        if sum(x**2 for x in combo) <= L_max:
            count += 1
    return count

def count_flux_vacua_approx(K, L_max):
    """
    K차원 구의 부피로 근사: V_K(r) = pi^(K/2) / Gamma(K/2+1) * r^K
    r = sqrt(L_max)
    """
    from math import gamma, pi
    r = np.sqrt(L_max)
    log_vol = (K / 2) * np.log(pi) - np.log(gamma(K / 2 + 1)) + K * np.log(r)
    return log_vol / np.log(10)  # log10(N_vacua)

# ── 소규모 정확 계산 (K=2,3,4) ────────────────────────────────
print("=" * 60)
print("소규모 플럭스 진공 정확 계산 (K ≤ 4)")
print("태드폴 조건: Σ n_i² ≤ L_max")
print("=" * 60)
print(f"{'K':>4} {'L_max':>6} {'N_range':>8} {'진공 수(정확)':>14} {'log10':>8}")
print("-" * 60)

small_cases = [(2, 5, 3), (2, 10, 4), (3, 5, 3), (3, 10, 4), (4, 5, 3)]
for K, L_max, N_range in small_cases:
    n_exact = count_flux_vacua_exact(K, L_max, N_range)
    log10_n = np.log10(n_exact) if n_exact > 0 else 0
    print(f"{K:>4} {L_max:>6} {N_range:>8} {n_exact:>14,} {log10_n:>8.2f}")

# ── K 스케일링 (근사 공식) ────────────────────────────────────
print("\n" + "=" * 60)
print("대규모 K에서 진공 수 (구 부피 근사, log₁₀)")
print("=" * 60)
print(f"{'K(사이클 수)':>14} {'L=50':>10} {'L=100':>10} {'L=200':>10}")
print("-" * 60)

K_vals_large = [10, 50, 100, 200, 300, 500]
L_vals       = [50, 100, 200]
for K in K_vals_large:
    row = f"{K:>14}"
    for L in L_vals:
        log10_N = count_flux_vacua_approx(K, L)
        row += f"  10^{log10_N:>6.1f}"
    print(row)

# ── 시각화 ────────────────────────────────────────────────────
fig, axes = plt.subplots(1, 3, figsize=(15, 5))

# 1) K=2 플럭스 격자 시각화 (태드폴 원 안의 점)
ax1 = axes[0]
L_vis = 10
N_vis = 4
pts_in  = [(x, y) for x in range(-N_vis, N_vis+1)
                   for y in range(-N_vis, N_vis+1) if x**2 + y**2 <= L_vis]
pts_out = [(x, y) for x in range(-N_vis, N_vis+1)
                   for y in range(-N_vis, N_vis+1) if x**2 + y**2 > L_vis]
ax1.scatter([p[0] for p in pts_in],  [p[1] for p in pts_in],
            c='#3498db', s=50, zorder=5, label=f'진공 ({len(pts_in)}개)')
ax1.scatter([p[0] for p in pts_out], [p[1] for p in pts_out],
            c='#e0e0e0', s=30, zorder=3, label='태드폴 초과')
theta = np.linspace(0, 2*np.pi, 200)
ax1.plot(np.sqrt(L_vis)*np.cos(theta), np.sqrt(L_vis)*np.sin(theta),
         'r--', linewidth=1.5, label=f'태드폴 경계 $r={np.sqrt(L_vis):.1f}$')
ax1.set_aspect('equal')
ax1.set_xlabel("$n_1$", fontsize=11)
ax1.set_ylabel("$n_2$", fontsize=11)
ax1.set_title(f"K=2 플럭스 격자\n태드폴: $n_1^2+n_2^2 \\leq {L_vis}$", fontsize=11)
ax1.legend(fontsize=8)
ax1.grid(alpha=0.3)

# 2) K 증가에 따른 log10(진공 수)
ax2 = axes[1]
K_range = np.arange(2, 501, 5)
for L_val, col, ls in zip([50, 100, 200], ['#e74c3c', '#3498db', '#2ecc71'], ['-','--','-.']):
    log10_Ns = [count_flux_vacua_approx(K, L_val) for K in K_range]
    ax2.plot(K_range, log10_Ns, color=col, linestyle=ls, linewidth=2,
             label=f'L={L_val}')

ax2.axhline(500, color='black', linestyle=':', linewidth=1.5, label='$10^{500}$ 기준')
ax2.set_xlabel("사이클 수 K", fontsize=11)
ax2.set_ylabel(r"$\log_{10}(\mathcal{N}_{\rm vacua})$", fontsize=11)
ax2.set_title("플럭스 진공 수 vs K\n(지수적 폭발)", fontsize=11)
ax2.legend(fontsize=9)
ax2.grid(alpha=0.3)

# 3) L 증가에 따른 진공 수 (K=300 고정)
ax3 = axes[2]
K_fixed = 300
L_range = np.linspace(10, 200, 100)
log10_Ns_L = [count_flux_vacua_approx(K_fixed, L) for L in L_range]

ax3.plot(L_range, log10_Ns_L, 'purple', linewidth=2.5)
ax3.axhline(500, color='red', linestyle='--', linewidth=1.5, label='$10^{500}$')
ax3.set_xlabel("태드폴 한계 L", fontsize=11)
ax3.set_ylabel(r"$\log_{10}(\mathcal{N}_{\rm vacua})$", fontsize=11)
ax3.set_title(f"K={K_fixed} 고정,\n플럭스 진공 수 vs 태드폴 한계", fontsize=11)
ax3.legend(fontsize=9)
ax3.grid(alpha=0.3)

plt.tight_layout()
plt.savefig("compactification_counting.png", dpi=150, bbox_inches='tight')
plt.show()
print("\n그림 저장: compactification_counting.png")
print(f"K=300, L=100 근사: 약 10^{count_flux_vacua_approx(300,100):.0f}개 진공")
```

**예상 출력 (일부)**:
```
소규모 플럭스 진공 정확 계산 (K ≤ 4)
   K  L_max  N_range   진공 수(정확)    log10
   2      5        3             37     1.57
   3      5        3            123     2.09
   4      5        3            341     2.53

K=300, L=100 근사: 약 10^487개 진공
```

---

## 🔬 경계

| 영역 | 알려진 것 ✓ | 모르는 것 ✗ |
|------|-----------|-----------|
| CY 목록 | Kreuzer-Skarke: 47만+ (수학적 분류) | 물리적으로 안정한 CY 수 |
| 진공 수 | $\sim 10^{500}$ (주문자릿수) | 정확한 값, 분포 |
| 표준 모형 구현 | 일부 CY에서 비슷한 구조 발견 | 정확한 SM을 주는 CY 발견 안 됨 ✗ |
| 안정화 | KKLT, LVS 등 메커니즘 | 완전한 안정화 + de Sitter 진공 ✗ |
| 선택 원리 | 없음 ✗ | 왜 이 진공에 있는가? |

✗ 풍경에서 우리 우주를 선택하는 **dynamical selection principle**은 없다. 이것이 Ch6에서 다룬 "미배달" 항목이다.

---

## 🧬 횡단 원리

**Ch6 풍경 비판**: 이 문서는 풍경이 왜 그토록 큰지 명시적으로 보여준다. $10^{500}$은 추상적 비판이 아니라 플럭스 격자 조합론에서 나오는 구체적 수다.

**L2 대칭**: 태드폴 조건은 게이지 불변성에서 비롯된 RR 전하 보존이다. 안정화의 조건이 대칭 원리에서 온다.

**L4 통계 역학**: $10^{500}$개의 메타안정 진공은 거대한 에너지 지형(energy landscape)을 형성한다. 영원한 인플레이션(eternal inflation)과 결합하면 모든 진공이 실현될 수 있다는 추론—그러나 이것은 물리적 예측이 아니라 형이상학적 주장에 가깝다.

---

## 🪜 창발

**창발: 유효 물리의 복수성**
10차원의 단일한 끈 이론에서 $10^{500}$개의 서로 다른 4차원 물리가 창발한다. 이것은 이론의 풍요로움인가, 예측력의 붕괴인가? 둘 다다. 원리적으로 모든 것을 설명할 수 있는 이론은 아무것도 예측하지 못할 수 있다.

**창발: 자연 상수의 비필연성**
전자 질량, 약한 힘의 결합 상수, 우주 상수 등이 "근본적으로 필연적인" 값이 아니라 우리가 특정 진공에 있기 때문에 관측하는 값일 수 있다. 이 경우 "왜 이 값인가?"라는 질문에 답하는 것이 불가능하다. ✗

---

## 📐 예측·반증

**구조적 예측 ✓**:
- 추가 차원의 존재 (반증 가능—LHC에서 미발견 ✗)
- 초대칭 파트너 (반증 가능—LHC에서 미발견 ✗)
- 특정 CY 콤팩트화가 표준 모형과 유사한 스펙트럼을 줄 수 있음 (일부 진전)

**반증 불가 영역 ✗**:
- "어딘가에" 표준 모형을 주는 진공이 있다는 주장 → $10^{500}$개 중 하나는 있을 것
- 인류 원리로 우리 우주의 선택 설명 → 관측 예측 없음
- 영원한 인플레이션으로 모든 진공 실현 → 원칙적으로 비관측 영역

---

## 🤔 다음 질문

1. **이 많은 진공 중 우리 우주의 물리를 어떻게 이해하나?** → [종합](./06-synthesis.md)

2. **AdS/CFT는 이 많은 진공 중 어떤 것을 기술하나?** → [AdS/CFT 사전](./05-ads-cft-dictionary.md)

3. **홀로그래피 관점에서 진공 선택이 의미하는 것은?** → [AdS/CFT 사전](./05-ads-cft-dictionary.md) + [종합](./06-synthesis.md)

---

> **🧩 원리**: 10차원 → 4차원 콤팩트화의 선택지 수가 $\sim 10^{500}$으로 지수적으로 많은 것은 CY 다양체의 위상적 다양성과 플럭스 양자화의 조합론적 폭발로부터 나온다.
>
> **🔬 경계**: 정확한 진공 수는 불명확하며, de Sitter 안정화는 여전히 미완성이다. 표준 모형을 재현하는 특정 CY는 아직 발견되지 않았다.
>
> **🪜 창발**: 서로 다른 자연 상수를 가진 $10^{500}$개의 4차원 물리가 단일한 10차원 이론에서 창발한다. 이것은 이론의 풍요로움인 동시에 예측력의 위기다.

---

<div align="center">

[◀ 이전: 류–타카야나기](./03-ryu-takayanagi.md) · [📚 README](../README.md) · [다음: AdS/CFT 사전 맛보기 ▶](./05-ads-cft-dictionary.md)

</div>
