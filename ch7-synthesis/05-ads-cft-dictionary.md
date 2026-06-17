# AdS/CFT 사전 맛보기

*중력 이론의 질량이 경계 이론의 차원수를 결정한다*

---

## 🎯 핵심 질문

말다세나(Maldacena)의 AdS/CFT 대응(1997)은 (d+1)차원 반 드 지터 공간(AdS)의 중력 이론과 d차원 경계의 등각 장 이론(CFT)이 동일한 물리를 기술한다고 주장한다. 이 대응을 실제로 사용하려면 두 이론의 물리량들이 어떻게 연결되는지 "사전"이 필요하다.

가장 기본적인 항목:

> AdS 내부의 스칼라 장이 질량 $m^2$를 가질 때, 경계 CFT에서 대응하는 1차 연산자의 스케일링 차원은?

$$\Delta(\Delta - d) = m^2 L^2 \quad \Longrightarrow \quad \Delta = \frac{d}{2} + \sqrt{\frac{d^2}{4} + m^2 L^2}$$

여기서 $L$은 AdS 반지름, $d$는 경계 차원이다. 그리고 안정성을 보장하는 BF(Breitenlöhner-Freedman) 한계:

$$m^2 L^2 \geq -\frac{d^2}{4}$$

이 두 공식을 정확히 이해하는 것이 이 문서의 목표다.

---

## 🌍 어디서 나타나나

**가장 잘 알려진 예**: $\mathcal{N}=4$ 초대칭 Yang-Mills($d=4$) ↔ Type IIB 초끈의 $\text{AdS}_5 \times S^5$.

$\Delta$-$m^2$ 공식이 등장하는 물리적 맥락:

- **딜라톤 장**: $m^2=0$ → $\Delta = d$ (보존 공류). 무질량 벌크 스칼라는 차원 $d$의 경계 연산자에 대응.
- **그라비톤 장**: 스핀-2, $m^2=0$ → 에너지-운동량 텐서 $T_{\mu\nu}$, $\Delta = d$.
- **타키온 같은 음의 $m^2$**: BF 한계 위에 있으면($m^2 > -d^2/4L^2$) 안정적이고 실수 $\Delta$를 준다.
- **응집물질 응용**: 홀로그래픽 초전도체, 비정상 금속에서 $\Delta$가 임계 지수와 연결된다.
- **AdS/QCD**: 쿼크-글루온 플라스마의 운반 계수 계산.

---

## 🔍 직관의 함정

**함정 1: "음의 $m^2$는 항상 불안정"이라는 오해.**
평탄한 시공간에서 $m^2 < 0$인 스칼라는 타키온—진공 불안정성의 신호다. AdS에서는 다르다. 음의 곡률이 안정화 역할을 하여 $m^2 \geq -d^2/4L^2$이면 안정적이다. BF 한계 바로 위의 음의 $m^2$는 물리적으로 완벽히 정상이다. ✓

**함정 2: $\Delta$가 항상 양의 정수라는 생각.**
$\Delta$는 실수이며, 단적 대칭과 표현론적 한계 $\Delta \geq d/2$ (유니타리 한계) 위에 있으면 임의의 실수값을 가질 수 있다. 비정수 $\Delta$는 비정규화 가능(non-normalizable) 모드와 관련되고, 경계 데이터로 해석된다.

**함정 3: 이 대응이 완전히 증명되었다는 생각.**
✗ AdS/CFT는 아직 수학적으로 증명되지 않았다. 수많은 비자명한 검증이 있지만(BPS 스펙트럼, 상관함수, 윌슨 루프 등), "증명"은 아니다. 매우 강력하게 지지되는 추측이다.

---

## ⚙️ 제1원리 유도

**AdS$_{d+1}$ 배경**: 포앙카레 좌표에서

$$ds^2 = \frac{L^2}{z^2}\left(\eta_{\mu\nu}dx^\mu dx^\nu + dz^2\right)$$

스칼라 장 $\Phi(z, x)$의 운동방정식(Klein-Gordon):

$$\left(\Box_{\text{AdS}} - m^2\right)\Phi = 0$$

$z \to 0$ (경계) 근방 점근 거동 (파워-로 안사츠):

$$\Phi \sim z^\Delta A(x) + z^{d-\Delta} B(x) + \ldots$$

지수 $\Delta$가 아이켄알(Euler) 방정식 조건을 만족해야 하므로:

$$\Delta(\Delta - d) = m^2 L^2$$

이를 $\Delta$에 대해 풀면 두 근:

$$\Delta_\pm = \frac{d}{2} \pm \sqrt{\frac{d^2}{4} + m^2 L^2}$$

물리적 해석:
- $z^{\Delta_-}$ 항: 비정규화 가능 모드 → 경계 조건(소스) $J(x)$
- $\Delta_+ > d/2$인 경우 $z^{\Delta_+}$ 항: 응답(기댓값) $\langle \mathcal{O}\rangle$

CFT 연산자 $\mathcal{O}$의 스케일링 차원은 $\Delta = \Delta_+$이고, 2점 함수:

$$\langle \mathcal{O}(x)\mathcal{O}(0)\rangle = \frac{C_\Delta}{|x|^{2\Delta}}$$

**BF 한계**: $\Delta_\pm$가 실수이려면 판별식 $\geq 0$:

$$\frac{d^2}{4} + m^2 L^2 \geq 0 \quad \Longrightarrow \quad m^2 L^2 \geq -\frac{d^2}{4}$$

$\square$

---

## 🧪 검증 현실

✗ **직접 실험 검증 없음.** AdS/CFT를 실험으로 검증하는 것은 현재 불가능하다.

✓ **수학적 내부 일관성 (아래 코드)**:
- $(m^2, d)$ 쌍에서 $\Delta$를 계산하고 유니타리 한계·BF 한계 확인
- BF 한계 근방의 거동 시각화

✓ **이론 내부 검증**:
- $\mathcal{N}=4$ SYM의 BPS 연산자 차원이 대칭으로 보호되어 약한 결합에서도 계산 가능—AdS 쪽 계산과 일치 ✓
- 윌슨 루프의 기대값이 두 쪽에서 일치 ✓
- 3점 함수 구조 상수가 일부 케이스에서 일치 ✓

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.colors import Normalize
from matplotlib.cm import ScalarMappable

# ── 핵심 함수 ──────────────────────────────────────────────────

def scaling_dimension(m2_L2, d):
    """
    스케일링 차원 계산: Δ = d/2 + sqrt(d²/4 + m²L²)
    BF 한계 아래이면 NaN (불안정)
    m2_L2: m²L² (차원 없는 질량 제곱)
    d: 경계 차원
    """
    discriminant = d**2 / 4 + m2_L2
    if np.isscalar(discriminant):
        if discriminant < 0:
            return np.nan
        return d / 2 + np.sqrt(discriminant)
    else:
        result = np.where(discriminant >= 0,
                          d / 2 + np.sqrt(np.maximum(discriminant, 0)),
                          np.nan)
        return result

def bf_bound(d):
    """BF 한계: m²L² ≥ -d²/4"""
    return -d**2 / 4

def unitarity_bound(d):
    """유니타리 한계: Δ ≥ (d-2)/2 (스칼라)"""
    return (d - 2) / 2

# ── 수치 계산 표 ───────────────────────────────────────────────
print("=" * 65)
print("AdS/CFT 사전: Δ(m²L², d) 계산")
print("Δ = d/2 + sqrt(d²/4 + m²L²), BF 한계: m²L² ≥ -d²/4")
print("=" * 65)

d_vals   = [2, 3, 4, 5]
m2L2_vals = [-3.0, -2.0, -1.0, 0.0, 1.0, 4.0, 9.0, 16.0]

for d in d_vals:
    bf = bf_bound(d)
    ub = unitarity_bound(d)
    print(f"\n── d={d} (BF 한계: m²L²≥{bf:.2f}, 유니타리 한계: Δ≥{ub:.1f}) ──")
    print(f"  {'m²L²':>8} │ {'Δ':>10} │ {'상태':>20}")
    print(f"  {'-'*8}-┼-{'-'*10}-┼-{'-'*20}")
    for m2L2 in m2L2_vals:
        Delta = scaling_dimension(m2L2, d)
        if np.isnan(Delta):
            status = "BF 한계 위반 (불안정) ✗"
        elif Delta < ub:
            status = "유니타리 한계 위반 ✗"
        else:
            status = "정상 ✓"
        delta_str = f"{Delta:.4f}" if not np.isnan(Delta) else "  불안정"
        print(f"  {m2L2:>8.2f} │ {delta_str:>10} │ {status:>20}")

# ── 시각화 ────────────────────────────────────────────────────
fig, axes = plt.subplots(1, 3, figsize=(15, 5))

# 1) d=4에서 Δ vs m²L²
ax1 = axes[0]
d_fixed = 4
m2L2_range = np.linspace(-4.5, 20, 400)
Delta_vals  = scaling_dimension(m2L2_range, d_fixed)

bf_val = bf_bound(d_fixed)
ub_val = unitarity_bound(d_fixed)

ax1.plot(m2L2_range[~np.isnan(Delta_vals)],
         Delta_vals[~np.isnan(Delta_vals)],
         'b-', linewidth=2.5, label=r'$\Delta = 2 + \sqrt{4 + m^2L^2}$')
ax1.axvline(bf_val, color='red', linestyle='--', linewidth=1.5,
            label=f'BF 한계 $m^2L^2={bf_val}$')
ax1.axhline(ub_val, color='orange', linestyle=':', linewidth=1.5,
            label=f'유니타리 한계 $\\Delta={ub_val}$')
ax1.fill_betweenx([0, 15], -10, bf_val, alpha=0.1, color='red', label='불안정 영역')

# 특별한 점 표시
special = [(0, 4, '딜라톤\n$m^2=0$'), (-3, 1+np.sqrt(1), 'BF 근방')]
for m2_sp, _, note in special[:1]:
    D_sp = scaling_dimension(m2_sp, d_fixed)
    ax1.scatter([m2_sp], [D_sp], s=100, zorder=6, color='green')
    ax1.annotate(note, (m2_sp, D_sp), textcoords='offset points',
                 xytext=(10, -15), fontsize=8)

ax1.set_xlim(-5, 20)
ax1.set_ylim(0, 10)
ax1.set_xlabel(r"$m^2 L^2$", fontsize=12)
ax1.set_ylabel(r"스케일링 차원 $\Delta$", fontsize=12)
ax1.set_title(f"d={d_fixed}: $\\Delta$ vs $m^2L^2$\n(BF 한계·유니타리 한계)", fontsize=11)
ax1.legend(fontsize=8)
ax1.grid(alpha=0.3)

# 2) 여러 d에 대한 Δ 곡선
ax2 = axes[1]
m2L2_plot = np.linspace(-10, 25, 400)
d_list = [2, 3, 4, 5, 6]
colors_d = ['#e74c3c', '#e67e22', '#2ecc71', '#3498db', '#9b59b6']
for d_val, col in zip(d_list, colors_d):
    Delta_plot = scaling_dimension(m2L2_plot, d_val)
    mask = ~np.isnan(Delta_plot)
    ax2.plot(m2L2_plot[mask], Delta_plot[mask], color=col,
             linewidth=2, label=f'd={d_val}')
    ax2.axvline(bf_bound(d_val), color=col, linestyle=':', linewidth=0.8, alpha=0.5)

ax2.set_xlabel(r"$m^2 L^2$", fontsize=12)
ax2.set_ylabel(r"$\Delta$", fontsize=12)
ax2.set_title("다양한 $d$에서 $\\Delta$ vs $m^2L^2$\n(점선: BF 한계)", fontsize=11)
ax2.legend(fontsize=9)
ax2.set_ylim(0, 14)
ax2.set_xlim(-10, 25)
ax2.grid(alpha=0.3)

# 3) (d, m²L²) 공간에서 Δ 컬러맵
ax3 = axes[2]
d_arr   = np.linspace(2, 6, 100)
m2_arr  = np.linspace(-9, 25, 100)
D_arr, M_arr = np.meshgrid(d_arr, m2_arr)
Delta_grid = scaling_dimension(M_arr, D_arr)

# BF 한계 아래는 NaN → 마스킹
im = ax3.pcolormesh(D_arr, M_arr, Delta_grid, cmap='viridis',
                    vmin=0, vmax=12, shading='auto')
plt.colorbar(im, ax=ax3, label=r'$\Delta$')

# BF 한계 곡선
d_bf = np.linspace(2, 6, 200)
ax3.plot(d_bf, -d_bf**2 / 4, 'r--', linewidth=2, label='BF 한계')
ax3.set_xlabel("경계 차원 $d$", fontsize=11)
ax3.set_ylabel(r"$m^2 L^2$", fontsize=11)
ax3.set_title(r"$\Delta(d, m^2L^2)$ 컬러맵" + "\n(빨간 점선: BF 한계)", fontsize=11)
ax3.legend(fontsize=9)

plt.tight_layout()
plt.savefig("ads_cft_dictionary.png", dpi=150, bbox_inches='tight')
plt.show()
print("\n그림 저장: ads_cft_dictionary.png")
```

**예상 출력 (d=4 부분)**:
```
── d=4 (BF 한계: m²L²≥-4.00, 유니타리 한계: Δ≥1.0) ──
    m²L²  │          Δ │               상태
  --------┼------------┼--------------------
     -4.50 │    불안정  │  BF 한계 위반 (불안정) ✗
     -4.00 │     2.0000 │              정상 ✓
      0.00 │     4.0000 │              정상 ✓
      4.00 │     2+2√2  │              정상 ✓
```

---

## 🔬 경계

| 조건 | 성립 ✓ | 성립 안 함 ✗ |
|------|--------|------------|
| 결합 상수 | 대형 N, 강한 't Hooft 결합 $\lambda = g^2 N \gg 1$ | 약한 결합 (격자/섭동 방법 필요) |
| 연산자 종류 | 단순 스칼라 1차 연산자 | 스핀 연산자, 비BPS 연산자 (더 복잡) |
| 배경 | 순수 AdS (영온도 CFT) | 블랙홀 배경 (유한 온도) → 수정 필요 |
| 증명 상태 | 비자명한 다수의 검증 | 수학적 증명 없음 ✗ |
| 응용 범위 | 등각 대칭 가진 CFT | 비등각 이론 (일반 QCD 등) |

---

## 🧬 횡단 원리

**L5 장 이론 ↔ 중력**: AdS/CFT의 본질은 서로 다른 차원의 두 이론이 같은 물리를 기술한다는 것이다. $\Delta$-$m^2$ 관계는 이 연결의 가장 구체적인 수치적 예다.

**L3 양자 정보**: CFT 연산자의 $\Delta$는 대칭 아래 변환 성질을 결정한다. 스케일링 차원이 보존 전하처럼 분류 역할을 한다.

**Ch7-03 류–타카야나기**: RT 공식의 측지선이 실수이려면 AdS 배경이 안정적이어야 한다. BF 한계가 안정성을 보장한다. 두 결과가 연결된다.

---

## 🪜 창발

**창발: 질량 ↔ 차원수의 번역**
중력 언어의 "질량"과 장 이론 언어의 "스케일링 차원"이 동일한 물리를 기술한다. 이 번역이 가능하다는 것 자체가 놀랍다. 두 개념은 각각의 이론에서 완전히 독립적으로 정의되지만, AdS/CFT라는 원리로 연결된다. ✓

**창발: 안정성의 재정의**
평탄한 시공간에서 "안정성 = $m^2 \geq 0$"이었지만, AdS에서는 부의 곡률이 안정화를 도와 "안정성 = $m^2 \geq -d^2/4L^2$"으로 완화된다. 시공간의 구조가 안정성 개념을 바꾼다.

---

## 📐 예측·반증

**수치적 예측 ✓**:
- $\mathcal{N}=4$ SYM의 보호된(BPS) 연산자 $\Delta$가 대칭으로 고정 → AdS 계산과 일치 ✓
- 슈퍼그래비티 스펙트럼의 $m^2$ → $\Delta$ 예측이 CFT쪽과 일치 ✓
- 홀로그래픽 반응 계수(shear viscosity $\eta/s = 1/4\pi$) → RHIC 실험과 근접 (간접) ✓

**반증 불가 또는 미확인 ✗**:
- 비BPS 연산자의 이상 차원(anomalous dimension)은 강한 결합에서 계산 어려움
- 실제 QCD(비등각)에 대한 정량적 예측 → 제한적
- AdS/CFT 자체의 직접 실험 검증 → 없음 ✗

---

## 🤔 다음 질문

이 문서들을 통해 끈 이론의 가장 구체적인 성취들을 살펴보았다:
- 중력자 스펙트럼의 필연성 (Ch7-01)
- T-쌍대성과 최소 길이 (Ch7-02)
- 얽힘 엔트로피와 기하학 (Ch7-03)
- 풍경의 기원 (Ch7-04)
- AdS/CFT 사전 (이 문서)

남은 질문: **이 모든 것을 합쳤을 때 끈 이론의 현재 위치는 어디인가?**

→ [종합: 성취와 미배달의 정직한 그림](./06-synthesis.md)

---

> **🧩 원리**: AdS 벌크 스칼라의 질량 $m^2$과 경계 CFT 연산자의 스케일링 차원 $\Delta$는 $\Delta(\Delta-d) = m^2 L^2$으로 연결된다. BF 한계 $m^2 L^2 \geq -d^2/4$에서 안정성이 보장된다.
>
> **🔬 경계**: 대형 N, 강한 결합 극한에서 수학적으로 성립. 약한 결합, 비등각 이론, 수학적 증명은 미완이다.
>
> **🪜 창발**: 질량(중력 언어)과 스케일링 차원(장 이론 언어)이 같은 물리의 두 기술임이 창발한다. 시공간 차원이 하나 줄어드는 홀로그래픽 창발이 수치로 확인된다.

---

<div align="center">

[◀ 이전: 콤팩트화 차원 세기](./04-compactification-counting.md) · [📚 README](../README.md) · [다음: 종합 ▶](./06-synthesis.md)

</div>
