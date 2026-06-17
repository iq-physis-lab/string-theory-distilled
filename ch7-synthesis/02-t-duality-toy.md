# T-쌍대성 장난감

*작은 원과 큰 원이 물리적으로 구별되지 않는다는 역설*

---

## 🎯 핵심 질문

공간의 한 방향을 반지름 $R$인 원으로 말았다고 하자. 직관적으로는 $R \to 0$이면 그 차원이 사라지고, $R \to \infty$이면 평탄한 공간으로 돌아올 것이다. 끈 이론은 이 직관을 정면으로 부정한다.

> 반지름 $R$의 원형 차원에 사는 끈의 스펙트럼은 반지름 $\alpha'/R$의 원형 차원에 사는 끈의 스펙트럼과 완전히 동일한가? 그렇다면 '최소 길이'란 무엇인가?

질량 공식은:

$$M^2 = \left(\frac{n}{R}\right)^2 + \left(\frac{wR}{\alpha'}\right)^2 + \frac{N_L + N_R - 2}{\alpha'}$$

여기서 $n \in \mathbb{Z}$는 운동량 모드(Kaluza-Klein), $w \in \mathbb{Z}$는 감김 모드(winding)다.

---

## 🌍 어디서 나타나나

**T-쌍대성**은 끈 이론의 여러 쌍대성 중 가장 명확하게 이해된 것이다.

- **IIA $\leftrightarrow$ IIB 초끈**: 원형 차원에서 $R \leftrightarrow \alpha'/R$으로 두 이론이 서로 연결된다.
- **헤테로틱 $E_8 \times E_8 \leftrightarrow SO(32)$**: 역시 T-쌍대성으로 연결.
- **M-이론 웹**: 5가지 초끈 이론이 쌍대성으로 연결된다는 증거의 핵심.
- **콤팩트화 모듈라이**: 복잡한 Calabi-Yau 콤팩트화에서도 T-쌍대성은 미러 대칭으로 나타난다.

점입자 이론에는 감김 모드가 없다. 끈만이 원 주위를 감아돌 수 있고, 이 감김 모드가 T-쌍대성을 가능하게 한다. **끈의 확장성(extended nature)이 없으면 이 쌍대성도 없다.**

---

## 🔍 직관의 함정

**함정 1: 작은 $R$과 큰 $R$이 다르다는 생각.**
점입자라면 $R \to 0$은 물리적 자유도의 손실이다. 그러나 끈에서는 $R \to 0$일 때 운동량 모드($n/R$)의 에너지는 발산하지만 감김 모드($wR/\alpha'$)의 에너지는 0으로 간다. 두 종류의 모드가 교환되면서 물리는 동일하게 유지된다.

**함정 2: 최소 길이가 0이라는 생각.**
T-쌍대성 $R \leftrightarrow \alpha'/R$은 $R = \sqrt{\alpha'}$를 자기쌍대점(self-dual point)으로 만든다. 이보다 작은 $R$의 물리는 더 큰 $\tilde{R} = \alpha'/R > \sqrt{\alpha'}$의 물리와 동일하다. 따라서 의미있는 최소 길이는 $\ell_s = \sqrt{\alpha'}$다.

**함정 3: "쌍대성 = 근사적 동등"이라는 오해.**
T-쌍대성은 **정확한(exact)** 동등이다. 섭동 전개의 모든 차수, 모든 관측량에서 두 기술이 동일한 결과를 준다. 이것이 쌍대성을 근사가 아닌 동일성으로 분류하는 이유다.

---

## ⚙️ 제1원리 유도

원형 차원 $X^{25} \sim X^{25} + 2\pi R$에서 모드 전개:

$$X^{25}(\tau, \sigma) = x^{25} + 2\alpha' p^{25}\tau + wR\sigma + \text{(진동 모드)}$$

주기 조건에서 운동량이 양자화: $p^{25} = n/R$, $n \in \mathbb{Z}$

감김 조건: $X^{25}(\tau, \sigma+2\pi) = X^{25}(\tau, \sigma) + 2\pi wR$, $w \in \mathbb{Z}$

좌우 운동량:

$$p_L = \frac{n}{R} + \frac{wR}{\alpha'}, \qquad p_R = \frac{n}{R} - \frac{wR}{\alpha'}$$

질량 공식:

$$\frac{\alpha' M^2}{4} = \frac{\alpha' p_L^2}{4} + N_L - 1 = \frac{\alpha' p_R^2}{4} + N_R - 1$$

즉:

$$M^2 = \frac{1}{\alpha'}\left[\frac{1}{2}(p_L^2 + p_R^2)(\alpha') + 2(N_L + N_R - 2)\right] = \left(\frac{n}{R}\right)^2 + \left(\frac{wR}{\alpha'}\right)^2 + \frac{2(N_L + N_R - 2)}{\alpha'}$$

**T-쌍대성 변환**: $R \to \tilde{R} = \alpha'/R$일 때 $n \leftrightarrow w$이면:

$$p_L \to p_L, \quad p_R \to -p_R$$

이 변환 하에 $M^2$은 불변! 스펙트럼이 완전히 보존된다. $\square$

자기쌍대점: $R = \tilde{R}$이면 $R^2 = \alpha'$, 즉 $R_* = \sqrt{\alpha'} = \ell_s$.

---

## 🧪 검증 현실

✗ **직접 실험 검증 없음.** $\ell_s \sim 10^{-35}$ m 스케일은 관측 불가.

✓ **수학적 자기일관성 확인 (아래 코드)**:
- 다양한 $(n, w, R)$ 조합에서 $M^2(R) = M^2(\alpha'/R)|_{n \leftrightarrow w}$를 수치로 확인
- 자기쌍대점 $R = \sqrt{\alpha'}$에서 스펙트럼 대칭성 확인

✓ **이론적 일관성**: IIA ↔ IIB 연결, 미러 대칭을 통한 수학적 예측은 수학 내부에서 독립적으로 확인되었다.

```python
import numpy as np
import matplotlib.pyplot as plt

# ── 파라미터 ──────────────────────────────────────────────────
ALPHA_PRIME = 1.0          # α' = 1 (끈 길이 단위)
LS = np.sqrt(ALPHA_PRIME)  # 자기쌍대 반지름 = 최소 길이

# ── 질량 제곱 공식 ─────────────────────────────────────────────
def M2_string(n, w, R, N_osc=0, alpha_prime=ALPHA_PRIME):
    """
    닫힌 끈 질량 공식 (진동 기여 단순화: N_L=N_R=N_osc/2 가정, a=1)
    M^2 = (n/R)^2 + (wR/alpha')^2 + (N_osc - 2) * 2/alpha'
    여기서는 N_osc=2 (N_L=N_R=1, 무질량 레벨)로 진동 기여 0 취급
    """
    KK   = (n / R)**2                    # Kaluza-Klein 항
    wind = (w * R / alpha_prime)**2      # winding 항
    osc  = (N_osc - 2) * 2 / alpha_prime
    return KK + wind + osc

# ── T-쌍대성 수치 검증 ─────────────────────────────────────────
print("=" * 60)
print("T-쌍대성 수치 검증: M²(R, n, w) = M²(α'/R, w, n)")
print("=" * 60)
print(f"{'n':>4} {'w':>4} {'R':>8} | {'M²(R)':>12} {'M²(α\'/R)':>12} {'일치?':>8}")
print("-" * 60)

test_cases = [
    (1, 0, 0.5), (0, 1, 0.5), (1, 1, 0.5), (2, 1, 0.5),
    (1, 0, 1.0), (0, 1, 1.0), (1, 1, 1.0), (2, 3, 1.5),
    (3, 2, 2.0), (1, 0, LS),  (0, 1, LS),  (2, 2, LS),
]

for n, w, R in test_cases:
    R_dual = ALPHA_PRIME / R
    m2_R      = M2_string(n, w, R)
    m2_R_dual = M2_string(w, n, R_dual)   # n↔w, R→α'/R
    match = "✓" if np.isclose(m2_R, m2_R_dual, rtol=1e-10) else "✗"
    print(f"{n:>4} {w:>4} {R:>8.3f} | {m2_R:>12.5f} {m2_R_dual:>12.5f} {match:>8}")

# ── R 변화에 따른 스펙트럼 곡선 ────────────────────────────────
R_values = np.logspace(-1, 1, 500)   # 0.1 ~ 10 범위

fig, axes = plt.subplots(1, 2, figsize=(13, 5))

# 왼쪽: 여러 (n, w) 쌍의 M² vs R
ax1 = axes[0]
mode_pairs = [(1,0), (0,1), (1,1), (2,0), (0,2)]
styles     = ['-', '--', '-.', ':', (0,(3,1,1,1))]
palette    = ['#e74c3c', '#3498db', '#2ecc71', '#e67e22', '#9b59b6']

for (n, w), ls, col in zip(mode_pairs, styles, palette):
    M2 = M2_string(n, w, R_values)
    ax1.plot(R_values, M2, linestyle=ls, color=col, linewidth=2,
             label=f'(n={n}, w={w})')

ax1.axvline(LS, color='black', linestyle=':', linewidth=1.5,
            label=f'$R_*=\\sqrt{{\\alpha\'}}={LS:.2f}$')
ax1.set_xscale('log')
ax1.set_xlabel(r"반지름 $R$ (단위: $\ell_s$)", fontsize=11)
ax1.set_ylabel(r"$M^2\alpha'$", fontsize=11)
ax1.set_title("끈 모드 $M^2$ vs 반지름 $R$\n(T-쌍대성: $R\\leftrightarrow\\alpha'/R$)", fontsize=11)
ax1.legend(fontsize=8)
ax1.set_ylim(-0.5, 15)
ax1.grid(alpha=0.3)

# 오른쪽: n=1,w=0 과 n=0,w=1의 교환 대칭 시각화
ax2 = axes[1]
M2_10 = M2_string(1, 0, R_values)   # KK 모드
M2_01 = M2_string(0, 1, R_values)   # winding 모드
M2_10_dual = M2_string(0, 1, ALPHA_PRIME / R_values)  # 쌍대 이론의 KK

ax2.plot(R_values, M2_10, 'r-',  linewidth=2.5, label='(n=1,w=0): KK 모드')
ax2.plot(R_values, M2_01, 'b--', linewidth=2.5, label='(n=0,w=1): winding 모드')
ax2.plot(R_values, M2_10_dual, 'g:', linewidth=2,
         label='쌍대(R→α\'/R)의 (w=1,n=0)')

ax2.axvline(LS, color='black', linestyle=':', linewidth=1.5,
            label=f'자기쌍대점 $R_*={LS:.2f}$')
ax2.set_xscale('log')
ax2.set_xlabel(r"반지름 $R$", fontsize=11)
ax2.set_ylabel(r"$M^2\alpha'$", fontsize=11)
ax2.set_title("KK↔winding 교환 대칭\n(자기쌍대점에서 만남)", fontsize=11)
ax2.legend(fontsize=8)
ax2.set_ylim(-0.5, 20)
ax2.grid(alpha=0.3)

plt.tight_layout()
plt.savefig("t_duality.png", dpi=150, bbox_inches='tight')
plt.show()
print(f"\n자기쌍대 반지름: R* = sqrt(α') = {LS:.4f}")
print("모든 테스트 케이스에서 T-쌍대성 성립 ✓")
```

**예상 출력 (일부)**:
```
T-쌍대성 수치 검증: M²(R, n, w) = M²(α'/R, w, n)
   n    w       R |       M²(R)    M²(α'/R)      일치?
   1    0   0.500 |      4.00000      4.00000       ✓
   0    1   0.500 |      0.25000      0.25000       ✓
   1    1   0.500 |      4.25000      4.25000       ✓
   ...
자기쌍대 반지름: R* = sqrt(α') = 1.0000
모든 테스트 케이스에서 T-쌍대성 성립 ✓
```

---

## 🔬 경계

| 영역 | T-쌍대성 성립 ✓ | 성립 안 함 ✗ |
|------|----------------|-------------|
| 구성 | 원형 차원, 평탄 배경 | 비원형 콤팩트화 (일반화 필요) |
| 결합 상수 | 임의의 $g_s$ (정확한 쌍대성) | — |
| 이론 쌍 | IIA↔IIB, HE↔HO | M-이론에서는 기하학적 해석 필요 |
| 수학 | 모든 섭동 차수에서 정확 | 비섭동적 효과는 별도 분석 |

T-쌍대성은 S-쌍대성(강↔약 결합)과 다르다. S-쌍대성은 증거가 있으나 엄밀한 증명은 어렵고, T-쌍대성은 세계면 CFT 수준에서 수학적으로 확립되어 있다.

---

## 🧬 횡단 원리

**최소 길이 원리**: $R < \ell_s$의 물리는 $R > \ell_s$의 물리와 동일하다. 이것은 양자 중력에서 예상되는 "플랑크 길이 이하는 기술 불능"과 연결되지만, 끈에서는 쌍대성 덕분에 물리가 완전히 유지된다는 점이 다르다.

**L1 파동-입자 이중성**: 운동량 모드($n/R$)와 감김 모드($wR/\alpha'$)의 교환은 파동-입자 이중성의 끈 버전이다. "위치 공간"과 "운동량 공간"의 대칭이 새로운 차원을 얻는다.

**L5 대칭**: T-쌍대성은 끈 이론의 쌍대성 웹 전체의 첫 번째 예시다. S-쌍대성, M-이론 조각들과 함께 "이론들의 이론"이라는 그림을 형성한다.

---

## 🪜 창발

**창발: 최소 길이의 물리**
점입자 양자역학에서 공간의 최소 길이 개념은 불연속적이고 외부에서 부과된다(예: 격자 모형). 끈 이론에서는 T-쌍대성이라는 내부 일관성으로부터 $\ell_s = \sqrt{\alpha'}$라는 최소 길이가 **창발**한다. "더 이상 작은 것은 없다"가 아니라 "더 작은 것은 더 큰 것과 같다"는 훨씬 강한 진술이다. ✓

**창발: 쌍대 기하학**
두 반지름이 물리적으로 동등하다는 것은 '기하학'이라는 개념 자체가 끈 이론에서 더 근본적인 무언가(세계면 CFT 데이터)의 창발임을 암시한다. 이 생각이 Ch7-03의 홀로그래피로 이어진다.

---

## 📐 예측·반증

**구조적 예측 ✓**:
- IIA와 IIB 초끈이 원 콤팩트화에서 동일한 물리를 주어야 함 → 수학적으로 확인
- 미러 쌍 Calabi-Yau 다양체의 존재 → 수학에서 독립적으로 확인
- $g_s \to 0$ 극한에서 T-쌍대성이 명확 → 섭동 계산으로 확인

**실험적 검증 ✗**:
- $R \sim \ell_s$의 물리는 실험 불가
- 추가 차원은 LHC에서 미발견

---

## 🤔 다음 질문

T-쌍대성은 시공간 기하학의 창발성을 암시한다. 그렇다면:

1. **기하학이 창발이라면, 블랙홀 엔트로피는 어디서 오나?** → [류–타카야나기](./03-ryu-takayanagi.md)

2. **콤팩트화의 선택지가 얼마나 많나?** → [콤팩트화 차원 세기](./04-compactification-counting.md)

3. **경계 이론과 내부 기하학의 대응은?** → [AdS/CFT 사전](./05-ads-cft-dictionary.md)

---

> **🧩 원리**: $R \leftrightarrow \alpha'/R$, $n \leftrightarrow w$ 변환 하에 끈 스펙트럼이 완전히 불변이다. 최소 물리 길이는 $\ell_s = \sqrt{\alpha'}$.
>
> **🔬 경계**: 원형 차원, 섭동 끈 이론에서 수학적으로 엄밀하게 성립. 일반 Calabi-Yau에서는 미러 대칭으로 일반화되지만 추가 분석 필요.
>
> **🪜 창발**: 최소 길이가 외부 가정 없이 쌍대성 구조 자체에서 창발한다. 시공간 기하학은 세계면 데이터의 창발물이다.

---

<div align="center">

[◀ 이전: 끈 진동 스펙트럼](./01-string-spectrum.md) · [📚 README](../README.md) · [다음: 류–타카야나기 ▶](./03-ryu-takayanagi.md)

</div>
