
### 配管系の諸計算　
以下の問題に取り組んでください。解答はWebClassにお願いします。数値を入力する際、例えば$1.20 \times 10^{-2}$の場合、0.0120, 1.20*10^(-2), 1.20e-2いずれでもいいです。
### 課題1　
**[配管1]** 内径50.0  mmの配管を用いて, 水 (ρ=1000  kg  m$^{-3}$，μ=1.25×10$^{-3}$ Pa s) を平均流速2.50 m s$^{-1}$でタンク１から20.0 mの高さにあるタンク２に汲み上げる配管がある。直管部の総長さは30.0  m、管路に90°エルボが４個，仕切弁2個が配置されている。

 **問1.**. 配管内のRe数を求め、WebClassの所定解答欄に数値のみ記入しなさい。
 **問2.**. エネルギー得失のある拡張ベルヌーイ式を次に示す。
 $$ 
 \frac{1}{2}u_1^2 + gh_1 + \frac{P_1}{\rho} + w =\frac{1}{2}u_2^2 + gh_2 + \frac{P_2}{\rho} +E_\mathrm{total}   \quad \text{(1)}
 $$
 - $u$ :線流速 [m/s]
 - $h$:基準面からの高さ[m]
 - $P$: 圧力 [Pa]
 - $\rho$ :流体密度 [kg/m$^3$]
 - $w$:ポンプから得るエネルギー
 - $E_\mathrm{total}$: エネルギー損失の総和
 
$w$と$E_\mathrm{total}$の単位として適切なものを選びなさい。Eq. (1)から判断してください。
　　　(1)  J/s
 　　　(2) J/kg
 　　　(3) J/m$^3$




**問3.** **配管1**においてタンク１とタンク２の水面を断面①、断面②とする。
 - 線流速は①、②ともゼロとする。
 - 圧力はいずれも大気開放

とした場合、Eq. (1)は簡略化でき、$w$は最終的に
$$w=\boxed{式　A}$$

となる。$\boxed{式A}$をテキスト入力で回答しなさい。(記入例）w= (P1-P2)/ rho + (u1-u2)^2

 
**問4**  全損失エネルギー$E_\mathrm{total}$を計算し、数値のみ解答欄に入力しなさい。ただし、各部位のエネルギー損失の求め方は以下のとおりとする。
　
>各部位のエネルギー損失$E$の算出につかう式の基本形は
$$ E = e_v \frac{1}{2} u^2$$
である。損失係数$e_v$は各部位によって以下のとおりとする。
> - 直管部：$e_v=4 \frac{L}{D} f$
		  層流のとき$f=\frac{16}{Re}$
	     乱流のとき$f=0.0791Re^{-\frac{1}{4}}$
> - エルボー: $e_v$=0.5
> - 仕切り弁: $e_v$=0.2
> 
>なお、タンクと配管の接続箇所における急拡大と急縮小による損失は無視できるものとする。

**問5**.ポンプ効率を55%としたときのポンプ所要動力[W]を求め,解答欄に数値のみ記入しなさい。 

---
### 課題2
**[配管2]** 長さ $L$、内径$D$の水平におかれた直円管に、密度を $\rho$の流体が線流速$u$一定で流れている。円管の上流断面①の圧力を $p_1$、下流断面②の圧力を $p_2$とし、流れ方向に摩擦損失が生じている。

この場合は、まずポンプ仕事$w$がなくなるので
 $$ \frac{1}{2}u_1^2 + gh_1 + \frac{P_1}{\rho}  =\frac{1}{2}u_2^2 + gh_2 + \frac{P_2}{\rho} +E    \quad \text{(2)}$$
 
**問6**  この**配管2**の場合、さらに$u$=一定および配管の水平配置からEq. (2)はさらに簡単になる。それを変形すると、下流における圧力$P_2$が

$$P_2=\boxed{式 　B}  $$
で求めることができる。$\boxed{式　B}$を解答欄にテキスト入力しなさい。

---
以上問1から問6は全員解答してください。以下は配管系の最適化に関する問題です、必須ではありませんが、提出した場合は加点します。

## 問題設定

あるプラントで、水をポンプで高さの異なる地点へ送る。  ポンプ動力が最小となるような配管の内径  D  を求めたい。

条件
| 項目    | 記号  | 値  |
| ----- | ------ | -- |
| 流量  |  $Q$  |  0.02  $\mathrm{m^3/s}$ |
| 配管長   |  $L$         |  200  $\mathrm{m}$  |
| 高低差   |  $\Delta z$  |  5  $\mathrm{m}$  |
| 粗さ    |  $\epsilon$  |  4.5$\times10^{-5}$ $\mathrm{m}$  |
| 水の密度  |  $\rho$  |  $1000$  $\mathrm{kg/m^3}$|
| 動粘度   |  $\nu$  |  $1.0\times10^{-6}$ $\mathrm{m^2/s}$   |
| 重力加速度 |  $g$         |  9.81  $\mathrm{m/s^2}$ |
| ポンプ効率 |  $\eta$         |  0.7   |
ポンプ動力 $P$ は：
$$ P= \rho gQ( \Delta z + h_f)/\eta　 \quad \text{(3)}$$

**ベルヌーイの定理（摩擦損失込み）からEq. (3)の導出**
ポンプによるエネルギー付加を$$\rho g h_p$$
また摩擦によるエネルギー損失を
$$\rho g h_f$$
とすると、ベルヌーイの定理より


$$p_1 + \frac{ \rho u_1^2}{2}+ \rho g z_1 + \rho gh_\mathrm{p} 
= p_2 + \frac{ \rho u_2^2}{2}+ \rho g z_2 +
\rho gh_\mathrm{f}$$ 
両辺を$\rho g$で除すると
$$\frac{p_1}{\rho g} + \frac{  u_1^2}{2g}+ z_1 + h_\mathrm{p} 
=\frac{p_2}{\rho g} + \frac{ u_2^2}{2g}+  z_2 +h_\mathrm{f}$$ 
となり、長さの次元を持つ式となる。$h$をhead（頭）と呼んでいる。ポンプ動力頭で整理すると

$$h_\mathrm{p} =\frac{p_2-p_1}{\rho g} + \frac{ u_2^2-u_1^2}{2g}+  (z_2 -z_1) +h_\mathrm{f}$$  

 - 大気開放より圧力項=0
 - 線流速は一定
 - $\Delta z = z_2- z_1$

とすると
$$h_\mathrm{p} =  \Delta z +h_\mathrm{f}$$ 

となる。

ポンプが1秒間に供給する**エネルギー量（仕事率）**＝**出力**  $P$ は

$P$ =（単位時間に流れる質量）×（単位質量あたりのエネルギー）
 $$P=(\rho Q) \times (gh_p)$$

従ってポンプ動力 $P$ は：
$$ P= \rho gQ( \Delta z + h_f) $$ で与えられる。実際にはポンプ効率$\eta$で除した値を用いる。
ここで、摩擦損失水頭 $h_\mathrm{f}$​ は **Darcy-Weisbach式**

$$h_f = f \frac{L}{D} \frac{u^2}{2g}$$

摩擦係数$f$は乱流の場合、

$$f=0.25 \left[ \log_{10} \left( \frac{\epsilon }{3.7 D} + \frac{5.74}{Re^{0.9}} \right) \right]^{-2}$$
で求めることにする。
(講義で使用したものと異なる式です）

---
**式のまとめ**

ここで$u$は平均線速度で 、あえて体積流量$Q$で表すと
$$u=\frac{4Q}{\pi D^2}$$
Re数を$u$の代わりに$Q$を使うと
$$Re = \frac{4Q \rho }{\pi D \mu }$$

したがって $h_f$は$D$の関数として
$$h_f(D)　＝ f(D) \left(\frac{L}{D} \right) \left( \frac{16 Q^2}{2 \pi^2 g D^4 }\right) $$


---
**結論**：ポンプ動力は
$$
\begin{aligned}
P &= \rho gQ( \Delta z + h_f(D)) / \eta\\
h_f(D)&＝ f(D) \left(\frac{L}{D} \right) \left( \frac{16 Q^2}{2 \pi^2 g D^4 }\right) \\
f(D) &=0.25 \left[ \log_{10} \left( \frac{\epsilon }{3.7 D} + \frac{5.74}{Re^{0.9}} \right) \right]^{-2}\\
Re &= \frac{4Q \rho }{\pi D \mu }
\end{aligned}
$$




エネルギー面からは、$P(D)$と$D$の曲線が得られるので、$P(D)$が最小となる$D$を求めることができる。

>**演習1**: 結論の一連の式を使って、**Excel**で　$P(D)$と$D$の曲線を計算し、**グラフ**にしてみましょう。$P(D)$が最小となる$D$があれば、その値を記載してください。もちろん、曲線の形によっては最小値が見つからない場合もありますので、その場合は戸惑わないでください。
>作成したExcelファイルは演習２と合わせて、WebClassの所定の場所に提出してください。

---
## コスト面も加味した最適化 

配管径 $D$ に対する 総コスト を
$$C_\mathrm{total}(D) =C_\mathrm{pipe}(D) + C_\mathrm{energy}(D)$$
とする。

**(1) 材料コスト**
鋼管などの材料費は、ざっくりと**体積に比例**するものとし（実際はもっと厳密に計算されますが、簡略化しました）、

$$C_\mathrm{pipe}(D) = k_P D^2 L$$
 $k_P$：材料単価　(JPY/m$^3$)

**(2) エネルギーコスト**
1年間の運転に要する電力料金は、
 
$$C_\mathrm{energy}(D) = k_e P(D) t$$
$k_e$: 電力単価[JPY/kWh]
$t$ : 運転時間　[h/year]

したがって、
$$C(D)=k_PD^2L + k_e \frac{\rho gQ( \Delta z + h_f(D)) }{ \eta}t$$

この$C(D)$を最小化する$D$を求めることになります。

> **演習2** 下表の値を使って$C(D)$ vs $D$のグラフを作成してください。今度は最小値がもとまりましたか？

| パラメータ   | 記号           | 値        | 単位      |
| ------- | ------------ | -------- | ------- |
| 密度      |  $\rho$      | 1000     | kg/m³   |
| 重力加速度   |  g         | 9.81     | m/s²    |
| 動粘度     |  $\nu$       | 1×10⁻⁶   | m²/s    |
| 流量      |  $Q$         | 0.02     | m³/s    |
| 長さ      |  $L$         | 200      | m       |
| 高低差     |  $\Delta z$  | 5        | m       |
| 粗さ      |  $\epsilon$  | 4.5×10⁻⁵ | m       |
| 効率      |  $\eta$      | 0.7      | －       |
| 電力単価    |  $k_e$       | 30       | 円/kWh   |
| 運転時間    |  $t$         | 4000     | 時間/年    |
| 材料コスト係数 |  $k_p$       | 2×10⁶    | 円/m³（例） |

演習１、２のPythonコードを貼り付けておきますので　Google Colabにコピペして、実行してみてください。解答が表示されます。

演習１のコード
```Python:Enshu1.py
import numpy as np
from scipy.optimize import minimize_scalar
import matplotlib.pyplot as plt

# --- 定数設定 ---
rho = 1000       # kg/m^3 (水)
g = 9.81         # m/s^2
Q = 0.02         # m^3/s
L = 200          # m
dz = 5           # m (高低差)
eps = 4.5e-5     # m (鋼管粗さ)
nu = 1.0e-6      # m^2/s (動粘度)

# --- 摩擦係数 Swamee-Jain式 ---
def friction_factor(D):
    v = 4 * Q / (np.pi * D**2)
    Re = v * D / nu
    f = 0.25 / (np.log10((eps/D)/3.7 + 5.74/Re**0.9))**2
    return f

# --- 摩擦損失水頭 ---
def hf(D):
    v = 4 * Q / (np.pi * D**2)
    f = friction_factor(D)
    return f * (L/D) * (v**2 / (2*g))

# --- ポンプ動力 ---
def P(D):
    return rho * g * Q * (dz + hf(D))  # W（ワット）

# --- 最適化 ---
res = minimize_scalar(P, bounds=(0.03, 0.3), method='bounded')

D_opt = res.x
P_min = res.fun

print(f"optimum D D_opt = {D_opt*1000:.1f} mm")
print(f"min pomp power P_min = {P_min/1000:.2f} kW")

# --- プロット ---
D_vals = np.linspace(0.05, 0.3, 100)
#D_vals = np.linspace(0.1, 0.3, 100)
P_vals = [P(D)/1000 for D in D_vals]

plt.figure(figsize=(7,4))
plt.plot(D_vals*1000, P_vals, label="P(D)")
plt.axvline(D_opt*1000, color='r', linestyle='--', label=f"Opt = {D_opt*1000:.1f} mm")
plt.xlabel("diameter D [mm]")
plt.ylabel("power P [kW]")
plt.title("P vs D")
plt.legend()
plt.grid(True)
plt.show()
```
演習２のpythonコード

```Python:Enshu2.py
import numpy as np
from scipy.optimize import minimize_scalar
import matplotlib.pyplot as plt

# --- 定数設定 ---
rho = 1000       # kg/m^3 (水)
g = 9.81         # m/s^2
Q = 0.02         # m^3/s
L = 200          # m
dz = 5           # m (高低差)
eps = 4.5e-5     # m (鋼管粗さ)
nu = 1.0e-6      # m^2/s (動粘度)

# --- 摩擦係数 Swamee-Jain式 ---
def friction_factor(D):
    v = 4 * Q / (np.pi * D**2)
    Re = v * D / nu
    f = 0.25 / (np.log10((eps/D)/3.7 + 5.74/Re**0.9))**2
    return f

# --- 摩擦損失水頭 ---
def hf(D):
    v = 4 * Q / (np.pi * D**2)
    f = friction_factor(D)
    return f * (L/D) * (v**2 / (2*g))

# --- ポンプ動力 ---
def P(D):
    return rho * g * Q * (dz + hf(D))  # W（ワット）

# --- 最適化 ---
res = minimize_scalar(P, bounds=(0.03, 0.3), method='bounded')

D_opt = res.x
P_min = res.fun

print(f"optimum D D_opt = {D_opt*1000:.1f} mm")
print(f"min pomp power P_min = {P_min/1000:.2f} kW")

# --- プロット ---
D_vals = np.linspace(0.05, 0.3, 100)
#D_vals = np.linspace(0.1, 0.3, 100)
P_vals = [P(D)/1000 for D in D_vals]

plt.figure(figsize=(7,4))
plt.plot(D_vals*1000, P_vals, label="P(D)")
plt.axvline(D_opt*1000, color='r', linestyle='--', label=f"Opt = {D_opt*1000:.1f} mm")
plt.xlabel("diameter D [mm]")
plt.ylabel("power P [kW]")
plt.title("P vs D")
plt.legend()
plt.grid(True)
plt.show()




