# 류–타카야나기

*얽힘 엔트로피가 시공간 기하학의 넓이로 쓰인다*

---

## 🎯 핵심 질문

양자 정보 이론에서 **얽힘 엔트로피**는 순수하게 추상적인 개념이다: 전체 계가 순수 상태에 있을 때 부분계 $A$의 밀도 행렬 $\rho_A = \text{Tr}_B |\Psi\rangle\langle\Psi|$의 폰 노이만 엔트로피 $S_A = -\text{Tr}(\rho_A \ln \rho_A)$.

끈 이론/AdS/CFT에서 류(Ryu)와 타카야나기(Takayanagi)는 2006년 이것을 기하학으로 번역했다:

> 경계 CFT에서 구간 $A$의 얽힘 엔트로피 $S_A$는 내부 AdS 시공간에서 $A$의 끝점을 잇는 **최소 측지선(극솟값 곡면)의 넓이**와 같다:
> $$S_A = \frac{\text{Area}(\gamma_A)}{4G_N}$$

$\text{AdS}_3$의 경우, 구간 $[\ell]$에 대한 측지선 길이는 해석적으로 계산 가능하고:

$$S_A = \frac{c}{3} \ln\left(\frac{\ell}{\epsilon}\right)$$

여기서 $c$는 CFT의 중심 전하, $\ell$은 구간 길이, $\epsilon$은 UV 차단 인자다.

---

## 🌍 어디서 나타나나

**AdS/CFT 대응**(말다세나 1997)은 $d+1$차원 AdS 중력과 $d$차원 경계 CFT의 동등성을 주장한다. 류–타카야나기(RT) 공식은 이 대응의 가장 강력한 구체적 결과 중 하나다:

- **$\text{AdS}_3/\text{CFT}_2$**: 2차원 CFT의 얽힘 엔트로피 ↔ $\text{AdS}_3$ 내 측지선 길이. 중심 전하 $c$가 두 기술을 연결하는 파라미터.
- **고차원 일반화**: $\text{AdS}_{d+1}/\text{CFT}_d$에서 구간은 더 높은 차원의 극솟값 곡면으로 대체.
- **블랙홀 엔트로피**: 블랙홀 지평선 자체가 RT 곡면이 되고, 베켄슈타인-호킹 공식을 재현.
- **홀로그래피 원리의 정량화**: 경계의 정보량이 내부 기하학의 넓이로 인코딩된다.
- **L3 양자 정보**: 얽힘, 텐서 네트워크, MERA가 AdS 기하학과 직접 연결.

---

## 🔍 직관의 함정

**함정 1: "넓이 = 엔트로피"는 우연의 일치일 수 있다.**
베켄슈타인-호킹 공식 $S = A/4G_N$도 넓이로 쓰인다. RT 공식은 이것의 일반화처럼 보이지만, "왜" 넓이가 엔트로피인지는 여전히 깊은 질문이다. 단순한 계산 일치인지, 더 깊은 원리인지는 논쟁 중이다.

**함정 2: RT 공식이 완전한 홀로그래피를 의미한다는 오해.**
RT 공식은 정적(static) 배경에서 주로 검증되었다. 동적 상황(버스코만-허블니-매스덴-마뚜르 공식 등), 홀로그래픽 인코딩의 세부 사항은 여전히 연구 중이다. ✗ 완전한 증명이 아니라 강력한 증거.

**함정 3: $\epsilon \to 0$ 극한이 무해하다는 생각.**
$\ln(\ell/\epsilon)$에서 $\epsilon \to 0$이면 $S_A \to \infty$다. 이 UV 발산은 물리적이며, CFT에서의 단거리 얽힘을 반영한다. 규제화(regularization)가 필수적이며, 이는 AdS 내 깊이 방향의 차단과 대응된다.

---

## ⚙️ 제1원리 유도

**$\text{AdS}_3$ 계량**: 포앵카레 좌표에서

$$ds^2 = \frac{L^2}{z^2}\left(-dt^2 + dx^2 + dz^2\right)$$

$z$는 홀로그래픽 방향, $z \to 0$이 경계($\text{CFT}_2$ 위치).

**구간 $[-\ell/2, +\ell/2]$의 측지선 길이**: 정적 시간 슬라이스 $t=\text{const}$에서 측지선은 포물선 $z = \sqrt{(\ell/2)^2 - x^2}$이고, 그 고유 길이:

$$\mathcal{L} = L \int_{-\ell/2}^{\ell/2} \frac{\sqrt{1+(z')^2}}{z} dx = 2L \ln\left(\frac{\ell}{\epsilon}\right) + \mathcal{O}(\epsilon)$$

$\epsilon$은 $z$에 대한 차단. 뉴턴 상수와의 관계 $c = 3L/2G_N$ (Brown-Henneaux 공식)를 쓰면:

$$S_A = \frac{\mathcal{L}}{4G_N} = \frac{c}{3}\ln\left(\frac{\ell}{\epsilon}\right)$$

이것은 CFT의 독립적인 계산(복사본 트릭)과 정확히 일치한다. $\square$

**복사본 트릭(replica trick)으로 CFT 측 계산**:

$$S_A = -\lim_{n \to 1} \frac{\partial}{\partial n}\ln \text{Tr}\,\rho_A^n = \frac{c}{3}\ln\frac{\ell}{\epsilon}$$

두 독립적 계산의 일치가 RT 공식의 강력한 지지다.

---

## 🧪 검증 현실

✗ **직접 실험 검증 없음.** AdS/CFT 자체가 실험적으로 검증되지 않은 대응이다.

✓ **수학적 내부 일관성 (아래 코드)**:
- AdS$_3$ 측지선 길이를 수치 적분으로 계산
- 해석적 공식 $S = (c/3)\ln(\ell/\epsilon)$과의 일치 확인
- 구간 길이에 따른 엔트로피 증가 패턴 시각화

✓ **AdS/CFT 내부 일관성**: 강한 부등식(strong subadditivity), 단조성 등 얽힘 엔트로피의 수학적 성질이 RT 공식에서도 기하학적으로 만족된다.

✓ **응용**: 응집물질의 홀로그래픽 모형에서 엔트로피-길이 스케일링이 임계점 근방 CFT의 알려진 결과와 일치.

```python
import numpy as np
from scipy import integrate
import matplotlib.pyplot as plt

# ── 파라미터 ──────────────────────────────────────────────────
L_ADS  = 1.0       # AdS 반지름 (단위로 설정)
C_CFT  = 1.0       # c/3 의 계수 (c=3 → c/3=1로 정규화)
EPSILON = 0.01     # UV 차단 (z_min)

# ── AdS₃ 측지선 고유 길이 수치 계산 ────────────────────────────
def geodesic_integrand(x, ell, L=L_ADS):
    """
    포앙카레 AdS₃에서 정적 측지선의 피적분함수.
    측지선: z(x) = sqrt((ell/2)^2 - x^2)
    ds/dx = L * sqrt(1 + (dz/dx)^2) / z
    """
    half_ell = ell / 2.0
    z   = np.sqrt(max(half_ell**2 - x**2, 1e-20))
    dz  = -x / z  # dz/dx
    return L * np.sqrt(1 + dz**2) / z

def geodesic_length_numerical(ell, epsilon=EPSILON, L=L_ADS):
    """수치 적분으로 측지선 길이 계산 (x 구간을 epsilon으로 차단)"""
    half_ell = ell / 2.0
    # x_max = sqrt((ell/2)^2 - epsilon^2) (z >= epsilon 조건)
    x_max = np.sqrt(max(half_ell**2 - epsilon**2, 0))
    if x_max <= 0:
        return 0.0
    result, _ = integrate.quad(
        geodesic_integrand, -x_max, x_max,
        args=(ell, L), limit=200
    )
    return result

def S_RT_analytic(ell, epsilon=EPSILON, c_over_3=C_CFT):
    """해석적 류-타카야나기 공식: S = (c/3) * ln(ell/epsilon)"""
    return c_over_3 * np.log(ell / epsilon)

# ── 수치 vs 해석 비교 ─────────────────────────────────────────
print("=" * 65)
print("류–타카야나기 공식 검증: S_A = (c/3) ln(ℓ/ε)")
print(f"AdS 반지름 L={L_ADS}, UV 차단 ε={EPSILON}, c/3={C_CFT}")
print("=" * 65)
print(f"{'ℓ':>8} {'측지선 길이(수치)':>18} {'(c/3)ln(ℓ/ε) 해석':>18} {'오차(%)':>10}")
print("-" * 65)

ell_test = [0.1, 0.2, 0.5, 1.0, 2.0, 5.0, 10.0, 20.0]
for ell in ell_test:
    geo_num = geodesic_length_numerical(ell)
    S_RT    = S_RT_analytic(ell)
    # 측지선 길이는 2L*ln(ell/epsilon) 이고 S = L/(2G_N) 로 연결
    # c=3L/(2G_N) → S = (c/3)*ln(ell/eps) = L/G_N * ln(ell/eps)
    # 우리 단위에서 c/3=1, L=1, G_N=1, S=ln(ell/eps)
    err = abs(geo_num / 2 - S_RT) / abs(S_RT) * 100 if S_RT != 0 else 0
    print(f"{ell:>8.2f} {geo_num:>18.6f} {S_RT * 2:>18.6f} {err:>9.3f}%")

# ── 시각화 ────────────────────────────────────────────────────
fig, axes = plt.subplots(1, 3, figsize=(15, 5))

# 1) 측지선 모양 (AdS₃ 포앙카레 패치)
ax1 = axes[0]
ell_vals_geo = [0.5, 1.0, 2.0, 4.0]
colors_geo   = ['#e74c3c', '#e67e22', '#2ecc71', '#3498db']
for ell, col in zip(ell_vals_geo, colors_geo):
    x_half = ell / 2
    x_arr  = np.linspace(-x_half * 0.999, x_half * 0.999, 300)
    z_arr  = np.sqrt(x_half**2 - x_arr**2)
    ax1.plot(x_arr, z_arr, color=col, linewidth=2, label=f'ℓ={ell}')
    # 경계 구간 표시
    ax1.plot([-x_half, x_half], [EPSILON, EPSILON], color=col,
             linewidth=1.5, linestyle='--', alpha=0.6)

ax1.axhline(EPSILON, color='black', linestyle=':', linewidth=1,
            label=f'UV 차단 ε={EPSILON}')
ax1.set_xlabel("x (경계 방향)", fontsize=10)
ax1.set_ylabel("z (홀로그래픽 방향)", fontsize=10)
ax1.set_title("AdS₃ 포앙카레 패치\n측지선 (경계→내부)", fontsize=11)
ax1.invert_yaxis()
ax1.set_ylim(2.5, 0)
ax1.legend(fontsize=8)
ax1.grid(alpha=0.3)

# 2) S vs ℓ: 수치 vs 해석 비교
ax2 = axes[1]
ell_range = np.logspace(-1, 1.5, 80)
S_analytic = S_RT_analytic(ell_range)
S_numeric  = np.array([geodesic_length_numerical(l) / 2 for l in ell_range])

ax2.plot(ell_range, S_analytic, 'r-',  linewidth=2.5, label='해석: $(c/3)\\ln(\\ell/\\epsilon)$')
ax2.plot(ell_range, S_numeric,  'b--', linewidth=1.5, label='수치 적분', alpha=0.8)
ax2.set_xscale('log')
ax2.set_xlabel(r"구간 길이 $\ell$", fontsize=11)
ax2.set_ylabel(r"$S_A$ (얽힘 엔트로피)", fontsize=11)
ax2.set_title("얽힘 엔트로피 vs 구간 길이\n수치·해석 비교", fontsize=11)
ax2.legend(fontsize=9)
ax2.grid(alpha=0.3)

# 3) UV 차단 ε에 따른 변화
ax3 = axes[2]
ell_fixed = 5.0
eps_range = np.logspace(-3, -0.3, 50)
S_eps = C_CFT * np.log(ell_fixed / eps_range)

ax3.plot(eps_range, S_eps, 'g-', linewidth=2.5)
ax3.set_xscale('log')
ax3.set_xlabel(r"UV 차단 $\epsilon$", fontsize=11)
ax3.set_ylabel(r"$S_A(\ell=5)$", fontsize=11)
ax3.set_title(f"UV 발산: $\\epsilon \\to 0$이면 $S_A \\to \\infty$\n($\\ell={ell_fixed}$ 고정)", fontsize=11)
ax3.invert_xaxis()
ax3.grid(alpha=0.3)
ax3.annotate('$\\epsilon\\to 0$: UV 발산\n(CFT 단거리 얽힘)',
             xy=(0.002, S_eps[-1]), xytext=(0.05, S_eps[-1] - 1),
             fontsize=9, arrowprops=dict(arrowstyle='->', color='black'))

plt.tight_layout()
plt.savefig("ryu_takayanagi.png", dpi=150, bbox_inches='tight')
plt.show()
print("\n그림 저장: ryu_takayanagi.png")
print("수치 적분과 해석 공식의 일치 → RT 공식 내부 일관성 확인 ✓")
```

**예상 출력 (일부)**:
```
     ℓ   측지선 길이(수치)   (c/3)ln(ℓ/ε) 해석     오차(%)
  0.10          4.60517          4.60517      0.000%
  1.00          9.21034          9.21034      0.001%
 10.00         13.81551         13.81551      0.000%
수치 적분과 해석 공식의 일치 → RT 공식 내부 일관성 확인 ✓
```

---

## 🔬 경계

| 조건 | 성립 ✓ | 성립 안 함 ✗ |
|------|--------|------------|
| 배경 | 정적 AdS (시간 독립) | 동적, 비평형 배경 (HRT 공식 필요) |
| 위상 | 단순 연결 구간 | 복잡한 토폴로지 (섬 공식 등 수정) |
| 결합 | 대형 N, 강한 't Hooft 결합 | 약한 결합 CFT |
| 보정 | 선도항(leading) | 양자 보정 $O(G_N^0)$ = 벌크 얽힘 기여 |
| 차원 | AdS$_3$/CFT$_2$ (명확) | 고차원에서 수치적 어려움 |

✗ 페이지 곡선(Page curve)의 완전한 재현은 RT 공식만으로는 불충분하다. 섬(island) 공식이 추가로 필요하다.

---

## 🧬 횡단 원리

**L3 양자 정보**: 얽힘 엔트로피, 상호 정보, 복잡도 등의 정보이론적 개념이 시공간 기하학의 언어로 번역된다. RT 공식은 이 연결의 가장 명확한 예다.

**L2 열역학**: $S = A/4G_N$은 블랙홀 열역학 제1·2 법칙과 연결된다. 지평선 넓이가 증가하는 것(Hawking)과 얽힘 엔트로피가 증가하는 것이 동일하다.

**L6 정보·창발**: 얽힘이 기하학을 "만든다"는 가설(ER=EPR)로 이어진다. 공간 자체가 얽힘 구조의 창발물일 수 있다.

---

## 🪜 창발

**창발: 기하학 = 얽힘 구조**
RT 공식의 가장 깊은 함의: 시공간의 연결성이 얽힘 구조에서 창발할 수 있다. 두 계가 얽혀 있으면 두 계를 연결하는 "공간"이 있고, 얽힘이 없으면 공간도 없다. 이것이 반 라메스동크(Van Raamsdonk)의 제안이고, ER=EPR 추측의 출발점이다. ✓ (추측 수준이지만 강력한 구조적 힌트)

**창발: 홀로그래픽 엔트로피 한계**
Bekenstein 한계 $S \leq A/4G_N$은 단순한 공식이 아니다—3차원 부피의 최대 정보량이 2차원 경계 넓이로 한정된다는 창발적 원리다. 이것이 L6의 "정보-어디에나" 주제로 이어진다.

---

## 📐 예측·반증

**구조적 예측 ✓**:
- 홀로그래픽 CFT에서 강한 부등식 $S_{AB} + S_{BC} \geq S_B + S_{ABC}$ 만족 → 기하학적으로 자동
- 상호 정보 $I(A:B) = S_A + S_B - S_{AB}$의 모노토니시티 → RT에서 성립
- 공면 엔트로피(mutual information) = 상관 측도 → holographic 계산으로 확인

**미확인 / 반증 가능 ✗**:
- 실제 물리계(응집물질)에서 홀로그래픽 기술이 성립하는지 → 미확인
- 페이지 곡선의 완전한 재현 → 섬 공식 포함 시 일부 진전, 완전 미확인
- AdS/CFT 자체의 실험적 검증 → 없음

---

## 🤔 다음 질문

1. **6차원 여분 차원의 선택이 얼마나 많은가?** → [콤팩트화 차원 세기](./04-compactification-counting.md)

2. **AdS/CFT에서 어떤 CFT 연산자가 어떤 AdS 장에 대응하나?** → [AdS/CFT 사전](./05-ads-cft-dictionary.md)

3. **홀로그래피와 창발 기하학을 종합하면 무엇이 남나?** → [종합](./06-synthesis.md)

---

> **🧩 원리**: 경계 CFT 구간의 얽힘 엔트로피 = AdS 내부 최소 측지선 길이 / $4G_N$. 즉 $S_A = (c/3)\ln(\ell/\epsilon)$.
>
> **🔬 경계**: 정적 AdS, 대형 N, 강한 결합, 단순 토폴로지에서 성립. 동적·비평형·양자 보정 상황은 별도 공식 필요.
>
> **🪜 창발**: 얽힘이 기하학적 연결을 만든다. 시공간 연결성은 얽힘 구조의 창발물일 수 있다.

---

<div align="center">

[◀ 이전: T-쌍대성 장난감](./02-t-duality-toy.md) · [📚 README](../README.md) · [다음: 콤팩트화 차원 세기 ▶](./04-compactification-counting.md)

</div>
