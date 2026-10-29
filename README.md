# Chemical Engineering — Transport Phenomena, Fluid Mechanics & Separation Processes

> Reference notes transcribed and formatted from the two supplied source documents. Equations and assumptions are retained as provided; they have not been independently verified.

## Contents

- DemoCase
- [Transport Phenomena](#transport-phenomena)
- [Fluid Mechanics](#fluid-mechanics)
- [Separation Processes](#separation-processes)

# Transport and Separation — Chemical Vapor Deposition (CVD)

> **Application:** Semiconductor thin-film deposition  
> **Core subjects:** Momentum transport, mass transport, interfacial reaction, and coupled transport–reaction  
> **Related course:** MATSCI 123 — Electronic Materials Processing

<img width="766" height="485" alt="Screenshot 2026-10-28 at 2 48 16 PM" src="https://github.com/user-attachments/assets/2ec04719-27e8-4cce-bfc2-e3fd04c3c7a2" />


## Overview: How CVD connects to transport phenomena

Chemical vapor deposition (CVD) forms a solid film through chemical reactions of gaseous precursors near or on a substrate. The steps are:

1. **Bulk convection:** Carrier gas delivers reactants through the reactor.
2. **Boundary-layer transport:** Reactants cross the near-wall concentration boundary layer.
3. **Adsorption and surface reaction:** Reactants react at the substrate.
4. **Film incorporation:** Solid reaction products form a thin film.
5. **Product removal:** Volatile byproducts diffuse and convect away.

The deposition rate may be controlled by gas-phase supply, surface kinetics, or both. This example is especially relevant to **momentum and mass transfer** within a Transport and Separation course; surface chemistry provides the coupled reaction boundary condition.

| Course topic | Key equation | Application to CVD |
| --- | --- | --- |
| Momentum transport | $Re_x=\rho v_\infty x/\mu$ | Predict flow regime and boundary-layer growth |
| Mass transport | $J_A=-D_{AB}\,dC_A/dy$ | Estimate precursor diffusion toward the wafer |
| Interfacial reaction kinetics | $r_s=k_s C_s$ | Relate surface consumption to surface concentration |
| Coupled transport–reaction | $J=\dfrac{k_s h_g}{k_s+h_g}C_g$ | Estimate net deposition flux with two serial resistances |

---

## 1. Momentum Transport — Carrier-Gas Flow and Hydrodynamic Boundary Layers

### 1.1 Reynolds number

For flow past a flat substrate,

$$
\boxed{Re_x=\frac{\rho v_\infty x}{\mu}}
$$

where:

| Symbol | Meaning | SI units |
| --- | --- | --- |
| $Re_x$ | Local Reynolds number | Dimensionless |
| $\rho$ | Gas density | kg/m³ |
| $v_\infty$ | Free-stream carrier-gas velocity | m/s |
| $x$ | Distance from leading edge | m |
| $\mu$ or $\eta$ | Dynamic viscosity | Pa·s |

The Reynolds number compares inertial effects with viscous effects. The following boundary-layer relations assume **steady, approximately two-dimensional laminar external flow over a flat plate** with roughly constant properties and negligible pressure gradient. Reactor geometry can require different correlations.

### 1.2 Local hydrodynamic boundary-layer thickness

A common engineering approximation is

$$
\boxed{\delta(x)\approx\frac{5x}{\sqrt{Re_x}}}
$$

Substituting the local Reynolds number,

$$
\delta(x)=\frac{5x}{\sqrt{\rho v_\infty x/\mu}}
=\boxed{5\sqrt{\frac{\mu x}{\rho v_\infty}}}.
$$

**Interpretation:** $\delta\propto\sqrt{x}$, so the velocity boundary layer grows downstream.

### 1.3 Average boundary-layer thickness

For a substrate of length $L$,

$$
\overline{\delta}=\frac{1}{L}\int_0^L\delta(x)\,dx.
$$

Substitute the local thickness:

$$
\begin{aligned}
\overline{\delta}
&=\frac{5}{L}\sqrt{\frac{\mu}{\rho v_\infty}}\int_0^L x^{1/2}\,dx\\
&=\frac{5}{L}\sqrt{\frac{\mu}{\rho v_\infty}}\left[\frac{2}{3}x^{3/2}\right]_0^L\\
&=\boxed{\frac{10}{3}\sqrt{\frac{\mu L}{\rho v_\infty}}}.
\end{aligned}
$$

Using $Re_L=\rho v_\infty L/\mu$,

$$
\boxed{\overline{\delta}=\frac{10L}{3\sqrt{Re_L}}=\frac{2}{3}\delta(L)}.
$$

### 1.4 Effect of carrier-gas flow rate

At fixed gas properties and geometry,

$$
\overline{\delta}\propto v_\infty^{-1/2}.
$$

Because the reactor volumetric flow rate is $Q=v_\infty A$ for a fixed flow cross section $A$,

$$
\boxed{\overline{\delta}\propto Q^{-1/2}}.
$$

**Example — doubling carrier-gas flow:**

$$
\frac{\overline{\delta}_2}{\overline{\delta}_1}
=\sqrt{\frac{Q_1}{Q_2}}
=\frac{1}{\sqrt 2}\approx0.707.
$$

The average hydrodynamic boundary layer becomes about **29.3% thinner**, provided the flow remains in the assumed regime.

### 1.5 Effect of reactor pressure

For an ideal gas at fixed temperature, composition, and free-stream velocity, with viscosity approximately independent of pressure,

$$
\rho=\frac{P\overline M}{RT}\propto P,
\qquad
\boxed{\delta\propto P^{-1/2}}.
$$

Thus a lower pressure can produce a **thicker velocity boundary layer** under these particular conditions. This does not by itself imply weaker species transport; gas-phase molecular diffusivity also changes with pressure. If mass-flow rate or reactor operating conditions are held fixed instead of velocity, the scaling must be re-evaluated.

---

## 2. Mass Transport — Precursor Diffusion to the Wafer

### 2.1 Fick's first law

For one-dimensional diffusion of dilute precursor A through carrier gas B,

$$
\boxed{J_A=-D_{AB}\frac{dC_A}{dy}}
$$

where $J_A$ denotes the **diffusive molar flux relative to the molar-average gas motion** (mol/(m²·s)), $D_{AB}$ is diffusivity (m²/s), and $C_A$ is molar concentration (mol/m³). The negative sign indicates diffusion from high concentration to low concentration.

The total precursor molar flux may also include convection. Here the boundary-layer model uses an effective **gas-side mass-transfer coefficient** to summarize the species transport.

### 2.2 Concentration and partial pressure

For an ideal gas,

$$
\boxed{C_A=\frac{P_A}{RT}},
$$

with $P_A$ in Pa, $R$ in J/(mol·K), and $T$ in K.

For an approximately linear concentration profile across an effective **mass-transfer thickness** $\delta_m$,

$$
\boxed{J_A\approx\frac{D_{AB}}{RT\delta_m}(P_{A,b}-P_{A,s})}.
$$

Subscripts $b$ and $s$ refer to the bulk gas and substrate surface, respectively.

### 2.3 Gas-side mass-transfer coefficient

Define $h_g$ by

$$
\boxed{J_g=h_g(C_g-C_s)},
\qquad
\boxed{h_g\approx\frac{D_{AB}}{\delta_m}}.
$$

| Symbol | Physical meaning | SI units |
| --- | --- | --- |
| $J_g$ | Gas-side precursor transport flux | mol/(m²·s) |
| $h_g$ | Gas-side mass-transfer coefficient | m/s |
| $C_g$ | Bulk precursor concentration | mol/m³ |
| $C_s$ | Surface precursor concentration | mol/m³ |
| $\delta_m$ | Effective concentration boundary-layer thickness | m |
| $D_{AB}$ | Binary gas diffusivity | m²/s |

**Important distinction:** The velocity boundary-layer thickness $\delta$ is not necessarily equal to the concentration boundary-layer thickness $\delta_m$. Their relationship depends on fluid properties and on $Sc=\mu/(\rho D_{AB})$, the **Schmidt number**. For quantitative calculations, use appropriate Sherwood-number correlations, $Sh=h_g L/D_{AB}=f(Re,Sc)$.

### 2.4 Pressure and gas diffusivity

For ordinary binary molecular diffusion of gases, a useful approximate scaling is

$$
\boxed{D_{AB}\propto\frac{T^n}{P}},\qquad n\approx1.5\text{–}2.
$$

If, additionally, the *effective mass-transfer thickness* scales approximately like the hydrodynamic thickness under a particular model, then

$$
\frac{D_{AB}}{\delta_m}\propto\frac{P^{-1}}{P^{-1/2}}=P^{-1/2},
$$

so

$$
\boxed{J_A\propto P^{-1/2}(P_{A,b}-P_{A,s})}.
$$

This is a **conditional scaling**, not a universal LPCVD rule. It presumes fixed temperature, gas velocity, and **partial-pressure difference**. At fixed precursor mole fractions, the partial-pressure difference usually changes with total pressure. In addition, a rigorous mass-transfer correlation can give a different pressure exponent.

---

## 3. Surface Reaction Kinetics — The Interface Boundary Condition

Surface reactions consume precursors arriving at the wafer. For a simplified first-order surface reaction,

$$
\boxed{r_s=k_s C_s},
$$

where $r_s$ is mol/(m²·s), $C_s$ is mol/m³, and $k_s$ is m/s. The reaction rate constant often has an Arrhenius form:

$$
\boxed{k_s=k_0\exp\left(-\frac{E_a}{RT_s}\right)}.
$$

Here $E_a$ is activation energy (J/mol), $T_s$ is substrate temperature (K), and $k_0$ is the pre-exponential factor (m/s).

Thermodynamics determines whether a reaction is favorable, while kinetics determines its rate:

$$
\Delta_r G^\circ=\sum_i\nu_i\Delta_f G_i^\circ,
\qquad
\boxed{\Delta_r G=\Delta_r G^\circ+RT\ln Q_{\mathrm{rxn}}}.
$$

A negative $\Delta_r G$ indicates thermodynamic favorability in the forward direction under the stated conditions, **not** a guarantee of rapid deposition. $Q_{\mathrm{rxn}}$ here is the reaction quotient, not the volumetric flow rate used in Section 1.

---

## 4. Coupled Mass Transport and Surface Reaction — CVD Rate Control

### 4.1 Flux continuity at steady state

Assume steady-state transport without gas-phase loss of the precursor inside the boundary layer, and a first-order surface reaction:

$$
J_g=h_g(C_g-C_s),
\qquad
J_s=k_sC_s,
\qquad
J_g=J_s=J.
$$

Solve for the surface concentration:

$$
\begin{aligned}
h_g(C_g-C_s)&=k_sC_s\\
h_gC_g&=(h_g+k_s)C_s\\
\boxed{C_s=\frac{h_g}{h_g+k_s}C_g}.&
\end{aligned}
$$

Substitute into the reaction flux:

$$
\boxed{J=\frac{k_sh_g}{k_s+h_g}C_g}.
$$

Define the overall coefficient $k_{\mathrm{overall}}$:

$$
J=k_{\mathrm{overall}}C_g,
\qquad
\boxed{\frac{1}{k_{\mathrm{overall}}}=\frac{1}{k_s}+\frac{1}{h_g}}.
$$

This is a **resistances-in-series model**: the surface-reaction and gas-phase mass-transfer resistances add. The smaller rate coefficient produces the larger resistance.

### 4.2 Limiting regimes

| Control regime | Criterion | Approximate flux | Physical meaning |
| --- | --- | --- | --- |
| Surface-reaction-limited | $k_s\ll h_g$ | $J\approx k_sC_g$ | Reactant supply is relatively fast; surface conversion is slow |
| Mass-transfer-limited | $k_s\gg h_g$ | $J\approx h_gC_g$ | Surface conversion is fast; arrival through the gas boundary layer is slow |
| Mixed control | $k_s\sim h_g$ | Full expression required | Both resistances contribute |

A useful dimensionless competition parameter is

$$
\boxed{Da_s=\frac{k_s}{h_g}}.
$$

This is a **surface Damköhler-type ratio**. For $Da_s\ll1$, surface kinetics limits; for $Da_s\gg1$, mass transfer limits.

The normalized deposition flux is

$$
\boxed{\frac{J}{h_gC_g}=\frac{Da_s}{1+Da_s}}.
$$

At $Da_s=1$, the flux equals $0.5h_gC_g$ and the two resistances contribute equally.

### 4.3 Temperature dependence and semilog growth-rate plots

In the reaction-limited regime, if $C_g$ is approximately constant,

$$
J\approx k_0C_g\exp\left(-\frac{E_a}{RT_s}\right),
$$

so

$$
\boxed{\ln J\approx\ln(k_0C_g)-\frac{E_a}{R}\frac{1}{T_s}}.
$$

On a graph of $\ln J$ versus $1/T_s$, the slope is approximately $-E_a/R$ in the reaction-limited regime. If the vertical axis uses $\log_{10}$ instead, the slope becomes $-E_a/(2.303R)$.

At higher temperatures, surface reaction may become so fast that transport begins to control the rate, producing a weaker temperature dependence. Different precursors (for example, SiH₄ and SiCl₄) can show different kinetic behavior.

### 4.4 APCVD and LPCVD: Why uniformity can differ

- **APCVD (atmospheric-pressure CVD):** Depending on kinetics and geometry, a fast surface reaction can deplete precursor near the wafer, making deposition sensitive to gas flow and upstream consumption.
- **LPCVD (low-pressure CVD):** Lower pressure usually increases molecular diffusivity. With a suitable choice of temperature, partial pressures, and residence time, surface-reaction-limited operation can improve across-wafer and wafer-to-wafer uniformity.

**Caution:** Lower pressure alone does **not** guarantee better uniformity or reaction-limited deposition. Geometry, precursor chemistry, concentration, gas residence time, and temperature distribution all matter.

---


## 5. Worked Practice Problem — Carrier-Gas Flow and Boundary-Layer Thickness

**Problem:** For laminar flow over a flat substrate of length $L$, the local boundary-layer thickness is $\delta(x)=5x/\sqrt{Re_x}$. (a) Derive its average thickness. (b) Determine how it changes if the carrier-gas volumetric flow rate doubles while gas properties and reactor geometry remain fixed.

**(a) Average thickness**

$$
\begin{aligned}
\overline\delta
&=\frac{1}{L}\int_0^L\frac{5x}{\sqrt{\rho v_\infty x/\mu}}\,dx\\
&=\frac{5}{L}\sqrt{\frac{\mu}{\rho v_\infty}}\int_0^L\sqrt{x}\,dx\\
&=\boxed{\frac{10}{3}\sqrt{\frac{\mu L}{\rho v_\infty}}}
=\boxed{\frac{10L}{3\sqrt{Re_L}}}.
\end{aligned}
$$

**(b) Double the flow rate**

Since $Q=v_\infty A$ and $A$ is fixed,

$$
\frac{\overline\delta_2}{\overline\delta_1}
=\left(\frac{Q_2}{Q_1}\right)^{-1/2}
=2^{-1/2}=0.707.
$$

**Answer:** The mean velocity boundary-layer thickness decreases by **29.3%**.

**CVD connection:** A thinner *concentration* boundary layer often increases $h_g\approx D_{AB}/\delta_m$ and thus deposition flux under mass-transfer-limited conditions. But do not replace $\delta_m$ directly with the hydrodynamic $\delta$ without checking the mass-transfer model.

---

## 6. Worked Practice Problem 2 — Temperature Sensitivity and CVD Rate Control

**Problem:** (a) Compare surface-reaction-controlled and diffusion-controlled CVD. (b) Assuming reaction-controlled Arrhenius kinetics with activation energy $E_a=1.0\ \mathrm{eV}$ per molecule, calculate the rate ratio when temperature increases from $700$ to $800\ \mathrm{K}$. (c) Explain why the deposition rate becomes less temperature-sensitive at high temperatures. Connect your answer to the previous boundary-layer problem.

### (a) Surface-reaction-controlled versus diffusion-controlled CVD

CVD requires precursor supply through the gas boundary layer **and** incorporation through a surface reaction. For steady-state, first-order kinetics:

$$
J_g=h_g(C_g-C_s),\qquad J_s=k_sC_s,\qquad J_g=J_s=J.
$$

Eliminating the surface concentration $C_s$ gives:

$$
\boxed{J=\frac{k_sh_g}{k_s+h_g}C_g}
$$

| Quantity | Surface-reaction-controlled | Diffusion (mass-transfer)-controlled |
| --- | --- | --- |
| Rate-limiting step | Surface reaction | Precursor delivery to the surface |
| Condition | $k_s\ll h_g$ | $k_s\gg h_g$ |
| Surface concentration | $C_s\approx C_g$ | $C_s\ll C_g$ |
| Flux | $J\approx k_sC_g$ | $J\approx h_gC_g$ |
| Sensitivity to temperature | Strong when $k_s$ is Arrhenius-controlled | Usually weaker, but not zero |
| Sensitivity to flow / gas transfer | Relatively weak | Often stronger |

**Units:** $J$ in $\mathrm{mol\,m^{-2}\,s^{-1}}$; $k_s$ and $h_g$ in $\mathrm{m\,s^{-1}}$; $C_g$ and $C_s$ in $\mathrm{mol\,m^{-3}}$.

**Physical interpretation:** When surface reaction is slow, precursor arrives faster than it can react, so $C_s\approx C_g$. When surface reaction is fast, precursor is consumed almost as soon as it arrives, so transport becomes the bottleneck.

### (b) Arrhenius rate increase from 700 K to 800 K

Assume reaction-controlled deposition and constant bulk precursor concentration:

$$
R_{\mathrm{dep}}(T)=R_0\exp\!\left(-\frac{E_a}{k_BT}\right).
$$

Here $R_{\mathrm{dep}}$ is the deposition rate, **not** the universal gas constant; $k_B$ is Boltzmann's constant. Given:

$$
E_a=1.0\ \mathrm{eV},\qquad
k_B=8.617\times10^{-5}\ \mathrm{eV\,K^{-1}}.
$$

Divide the rates to eliminate the unknown prefactor $R_0$:

$$
\begin{aligned}
\frac{R_{\mathrm{dep}}(800)}{R_{\mathrm{dep}}(700)}
&=\frac{R_0e^{-E_a/(k_B\cdot800)}}{R_0e^{-E_a/(k_B\cdot700)}}\\
&=\exp\!\left[\frac{E_a}{k_B}\left(\frac{1}{700}-\frac{1}{800}\right)\right]\\
&=\exp\!\left[\frac{1.0}{8.617\times10^{-5}}
\left(\frac{1}{700}-\frac{1}{800}\right)\right]\\
&\approx\boxed{7.94}.
\end{aligned}
$$

**Answer:** Under these assumptions, increasing temperature from $700$ to $800\ \mathrm{K}$ raises the rate by approximately **7.94 times**. Higher temperature strongly increases the frequency of successful activated surface-reaction events.

**Important condition:** This ratio assumes unchanged activation energy and prefactor, constant precursor concentration, and **reaction-controlled deposition throughout** $700$–$800\ \mathrm{K}$. If the process enters mixed or mass-transfer control, the actual ratio will generally be smaller.

> **Unit convention:** $E_a/k_BT$ is dimensionless if $E_a$ is expressed per molecule (eV) and $k_B$ is in eV/K. If $E_a$ is instead in J/mol, use the molar gas constant $R=8.314\ \mathrm{J\,mol^{-1}\,K^{-1}}$.

### (c) Why the deposition rate becomes less temperature-sensitive

At relatively low temperatures, $k_s\ll h_g$:

$$
J\approx k_sC_g,\qquad k_s=k_0e^{-E_a/(RT)}.
$$

The reaction coefficient changes exponentially with temperature, producing a steep slope on an Arrhenius plot.

As temperature rises, $k_s$ may increase until $k_s\gg h_g$:

$$
J\approx h_gC_g.
$$

Now faster surface chemistry cannot substantially increase deposition because the gas cannot replenish precursor quickly enough. **Mass-transfer control is not temperature independence:** diffusivity, gas properties, and precursor concentration can still vary with temperature.

A useful dimensionless comparison is the **mass-transfer Damköhler ratio**:

$$
\boxed{Da_m=\frac{k_s}{h_g}}
$$

| $Da_m$ | Regime | Consequence |
| --- | --- | --- |
| $Da_m\ll 1$ | Reaction-controlled | Temperature strongly affects $J$ through $k_s$ |
| $Da_m\approx 1$ | Mixed control | Both resistances contribute appreciably |
| $Da_m\gg 1$ | Mass-transfer-controlled | Changes in $h_g$ and precursor supply dominate |

**Series-resistance interpretation:** Defining $k_{\mathrm{overall}}=J/C_g$ gives

$$
\frac{1}{k_{\mathrm{overall}}}=\frac{1}{k_s}+\frac{1}{h_g},
\qquad
\frac{J}{h_g C_g}=\frac{Da_m}{1+Da_m}.
$$

At $Da_m=1$, surface-reaction and gas-transfer resistances are equal, so $J/(h_g C_g)=0.5$.

**Connection to Practice Problem 1:** For fixed reactor geometry, gas properties, and laminar flow over a flat plate:

$$
\overline{\delta}_v\propto v_\infty^{-1/2}\propto Q^{-1/2}.
$$

Increasing carrier-gas flow reduces the **velocity** boundary-layer thickness. It can also increase mass transfer to the wafer, but the concentration boundary layer $\delta_m$ is not necessarily identical to the velocity boundary layer $\delta_v$; a suitable Sherwood-number correlation is needed for quantitative predictions.

| Operating regime | Often effective lever | Why |
| --- | --- | --- |
| Reaction-controlled | Raise substrate temperature | Accelerates surface-reaction kinetics |
| Mass-transfer-controlled | Improve precursor delivery, mixing, or reactor flow design | Increases available reactant supply and potentially $h_g$ |

**Key lesson:** $T\uparrow\ \Rightarrow\ k_s\uparrow$ may move the process from reaction control to mixed control and eventually mass-transfer control; deposition rate then becomes **less sensitive to further temperature increases**.

---

## 7. Worked Practice Problem 3 — CVD Equilibrium Constants and Gibbs Free Energy

**Problem:** (a) Construct the equilibrium constant for the forward CVD reaction, assuming pure solids have unit activity. (b) Use Hess's law and the supplied standard Gibbs energies at $1000\ \mathrm{K}$ to determine $\Delta_r G^\circ$. (c) Evaluate thermodynamic favorability. (d) Calculate the equilibrium constant using $R=1.99\ \mathrm{cal\,mol^{-1}\,K^{-1}}$.

> **Source-data limitation:** The actual balanced target reaction and the two underlying thermochemical equations were not included in the supplied problem text. Their stoichiometric coefficients and phases must be checked against the original assignment before writing an exact species-specific equilibrium expression. The provided relation $\mathrm{Eq.\,1=Eq.\,2+3(Eq.\,3)}$ and the reported Gibbs-energy data are sufficient to solve parts (b)–(d).

### (a) Construct the equilibrium constant correctly

For a general balanced reaction

$$
\sum_i \nu_i A_i=0,
$$

where $\nu_i$ is positive for products and negative for reactants, the dimensionless thermodynamic equilibrium constant is

$$
\boxed{K=\prod_i a_i^{\nu_i}=\frac{\prod_{\rm products}a_i^{\nu_i}}{\prod_{\rm reactants}a_i^{-\nu_i}}}.
$$

- For a **pure solid**, $a_i=1$, so it does not appear explicitly in $K$. In particular, omit $\mathrm{Y_2O_3(s)}$ if it is a pure solid.
- For an **ideal gas**, $a_i=p_i/p^\circ$; use **dimensionless pressure ratios** rather than bare dimensional concentrations. Under an ideal-gas standard-state convention, an equivalent concentration-based form uses $a_i=c_i/c^\circ$ with the appropriate standard state.
- Whether $\mathrm{YCl_3}$ appears in $K$ depends on its **phase**. Omit it too if it is a pure solid; retain it if it is gaseous (with its applicable gas activity).

**Transcription warning:** The supplied notation, `Kc = [CO]3 [Cl2]3[YCl3]2 [CO2]3`, lacks a clear fraction bar and the balanced reaction. It cannot unambiguously establish which terms belong in the numerator or denominator. Do **not** treat that text as a verified equilibrium expression; use the balanced equation to construct $K$.

### (b) Calculate $\Delta_r G^\circ$ using Hess's law

For standard reaction Gibbs energies, reversing a reaction changes the sign of $\Delta_rG^\circ$; multiplying a reaction by $n$ multiplies $\Delta_rG^\circ$ by $n$; adding reactions adds their Gibbs energies.

The supplied relationship is:

$$
\mathrm{Eq.\,1=Eq.\,2+3(Eq.\,3)}.
$$

Given at $1000\ \mathrm{K}$:

$$
\Delta_r G_2^\circ=-59.4\ \mathrm{kcal\,mol^{-1}},\qquad
\Delta_r G_3^\circ=+46.7\ \mathrm{kcal\,mol^{-1}}.
$$

Hence,

$$
\begin{aligned}
\Delta_r G_1^\circ
&=\Delta_r G_2^\circ+3\Delta_r G_3^\circ\\
&=-59.4+3(46.7)\\
&=\boxed{+80.7\ \mathrm{kcal\,mol^{-1}}}.
\end{aligned}
$$

The energy is **per mole of reaction as balanced** (often written simply $\mathrm{kcal/mol}$ in a homework solution).

### (c) Is the forward reaction favorable?

At standard-state activities,

$$
\Delta_r G=\Delta_r G^\circ+RT\ln Q,
$$

and $Q=1$ gives $\Delta_r G=\Delta_r G^\circ=+80.7\ \mathrm{kcal\,mol^{-1}}$.

Therefore, the **forward reaction is not thermodynamically favorable under standard-state conditions at $1000\ \mathrm{K}$**. The reverse reaction is favored at standard state. **Important:** $\Delta_rG^\circ>0$ does **not** mean the forward reaction can never occur. Actual direction depends on the reaction quotient $Q$: the forward direction is favorable when $\Delta_rG<0$, equivalently $Q<K$.

### (d) Calculate the numerical equilibrium constant

At equilibrium $\Delta_rG=0$ and $Q=K$, so

$$
\boxed{\Delta_rG^\circ=-RT\ln K}
$$

Rearrange (note that $RT$ is in the **denominator** of the exponent):

$$
\boxed{K=\exp\!\left(-\frac{\Delta_rG^\circ}{RT}\right)}.
$$

Convert the given energy to calories so it matches the supplied gas constant:

$$
80.7\ \mathrm{kcal\,mol^{-1}}=80{,}700\ \mathrm{cal\,mol^{-1}}.
$$

At $T=1000\ \mathrm{K}$ and $R=1.99\ \mathrm{cal\,mol^{-1}\,K^{-1}}$:

$$
\begin{aligned}
K&=\exp\!\left[-\frac{80{,}700}{(1.99)(1000)}\right]\\
&=\exp(-40.55)\\
&\approx\boxed{2.4\times10^{-18}}.
\end{aligned}
$$

**Interpretation:** The very small equilibrium constant means equilibrium strongly favors the **reactants** for the forward reaction at the standard states and temperature specified. This describes **thermodynamic equilibrium**, not the kinetic deposition rate or the rate-controlling mechanism.

### Connection to transport and reaction kinetics

| Question | Governing relation | What it tells you |
| --- | --- | --- |
| Is the reaction thermodynamically favorable? | $\Delta_rG=\Delta_rG^\circ+RT\ln Q$ | Direction of spontaneous change at specified conditions |
| Where does equilibrium lie? | $K=\exp[-\Delta_rG^\circ/(RT)]$ | Equilibrium product/reactant activities |
| How fast does surface chemistry consume precursor? | $J_s=k_sC_s$ | Kinetic rate under a first-order model |
| How fast is precursor delivered? | $J_g=h_g(C_g-C_s)$ | Gas-side transport rate |
| What is the net steady-state deposition flux? | $J=k_sh_gC_g/(k_s+h_g)$ | Combined transport/reaction limit under the simplified irreversible model |

**Model qualification:** A substantial reverse reaction or proximity to thermodynamic equilibrium requires a reversible surface-reaction model; the simplified irreversible, first-order series-resistance expression alone does not enforce the equilibrium constraint.

---

---

## 8. Worked Example 4 — Convective Heat Transfer and Transport Similarity (ME 109, Lecture 10/09)
<img width="740" height="669" alt="Screenshot 2026-10-29 at 12 06 35 PM" src="https://github.com/user-attachments/assets/dfc9b0be-073d-4440-9819-e8f33afa8b56" />


> **Source:** ME 109, *Lecture 10/09: Convective Heat Transfer Equations*, Example 6.5 (p. 5). This is a **heat-transfer example**, not a CVD reaction problem. It illustrates nondimensional similarity and connects to gas-side mass transfer in CVD.

### Given: Turbine blade under hot gas flow

| Quantity | Initial condition | SI units |
| --- | ---: | --- |
| Blade chord length, $L_1$ | $40\ \mathrm{mm}=0.040\ \mathrm{m}$ | m |
| Free-stream speed, $U_{\infty,1}$ | $160$ | m/s |
| Hot-gas temperature, $T_\infty$ | $1150$ | °C |
| Blade surface temperature, $T_{s,1}$ | $800$ | °C |
| Heat flux to blade, $q_1''$ | $95{,}000$ | W/m² |
| Kinematic viscosity, $\nu$ (Part b) | $2.06\times10^{-4}$ | m²/s |

For convection from hot gas to a cooler surface, Newton's law of cooling gives

$$
\boxed{q''=h(T_\infty-T_s)}
$$

where $h$ is the convective heat-transfer coefficient ($\mathrm{W\,m^{-2}\,K^{-1}}$). The Nusselt and Reynolds numbers are

$$
\boxed{Nu=\frac{hL}{k_f}},\qquad \boxed{Re_L=\frac{U_\infty L}{\nu}},
$$

where $k_f$ is the gas thermal conductivity ($\mathrm{W\,m^{-1}\,K^{-1}}$). For geometrically similar conditions and constant properties, the lecture models $Nu=f(Re,Pr)$; $Pr=\nu/\alpha$ is the Prandtl number.

### (a) The surface cools from 800 °C to 700 °C: new heat flux?

The free-stream conditions, blade length, and fluid properties are unchanged, so $Re_2=Re_1$, $Pr_2=Pr_1$, and $Nu_2=Nu_1$. Therefore, $h_2=h_1$.

Find the original coefficient:

$$
\begin{aligned}
h_1&=\frac{q_1''}{T_\infty-T_{s,1}}\\
&=\frac{95{,}000}{1150-800}\\
&\approx271.4\ \mathrm{W\,m^{-2}\,K^{-1}}.
\end{aligned}
$$

The new heat flux is

$$
\begin{aligned}
q_2''&=q_1''\frac{T_\infty-T_{s,2}}{T_\infty-T_{s,1}}\\
&=95{,}000\frac{1150-700}{1150-800}\\
&\approx\boxed{1.22\times10^5\ \mathrm{W/m^2}}.
\end{aligned}
$$

**Physical meaning:** A cooler blade has a larger gas-to-surface temperature difference. With the convection coefficient unchanged, the heat flux **increases** to about $122{,}000\ \mathrm{W/m^2}$.

### (b) Lower speed and longer chord: new heat flux?

The proposed operating conditions are $U_{\infty,2}=80\ \mathrm{m/s}$ and $L_2=80\ \mathrm{mm}=0.080\ \mathrm{m}$. The lecture compares these with the **original 800 °C surface condition**, not the modified 700 °C surface in part (a).

Calculate both Reynolds numbers:

$$
\begin{aligned}
Re_1&=\frac{(160)(0.040)}{2.06\times10^{-4}}\approx31{,}068,\\
Re_2&=\frac{(80)(0.080)}{2.06\times10^{-4}}\approx31{,}068.
\end{aligned}
$$

Because $Re_2=Re_1$, the fluid properties and $Pr$ are unchanged, and the blade configurations are treated as similar, the lecture assumes $Nu_2=Nu_1$.

Using $Nu=hL/k_f$ with unchanged $k_f$:

$$
\frac{h_2}{h_1}=\frac{L_1}{L_2}=\frac{0.040}{0.080}=\frac12.
$$

At the same $T_\infty$ and $T_s$ as the original case, this gives

$$
\begin{aligned}
q_2''&=q_1''\frac{L_1}{L_2}\frac{T_\infty-T_{s,2}}{T_\infty-T_{s,1}}\\
&=95{,}000\left(\frac{0.040}{0.080}\right)\left(\frac{1150-800}{1150-800}\right)\\
&=\boxed{47{,}500\ \mathrm{W/m^2}}.
\end{aligned}
$$

**Physical meaning:** Matching Reynolds number does **not** mean matching dimensional heat-transfer coefficient. Here $Nu$ is unchanged, but doubling $L$ halves $h$ and therefore halves heat flux at a fixed temperature difference.

### Connection to CVD: Heat–mass transfer analogy

Lecture 10/09 also introduces the mass-transfer counterpart of the Nusselt number:

$$
\boxed{Sh=\frac{h_mL}{D_{AB}}},\qquad
\boxed{Sc=\frac{\nu}{D_{AB}}}
$$

where $Sh$ is the Sherwood number, $Sc$ is the Schmidt number, $h_m$ is the mass-transfer coefficient (m/s), and $D_{AB}$ is binary diffusivity (m²/s). Under analogous boundary-layer assumptions,

$$
\underbrace{Nu=f(Re,Pr)}_{\text{heat transfer}}
\quad\longleftrightarrow\quad
\underbrace{Sh=f(Re,Sc)}_{\text{mass transfer}}.
$$

For CVD the associated precursor delivery flux is $J_g=h_m(C_g-C_s)$, so **flow conditions affect both heat exchange and precursor delivery**. Similarity correlations must be chosen for the actual geometry, flow regime, and fluid properties; $Nu=Sh$ is not generally implied.

**Study questions:** Why is the heat flux larger in (a) even though only the blade temperature changes? Why is $h_2=h_1/2$ in (b) despite equal Reynolds numbers? What replaces $Pr$ and $Nu$ in the analogous CVD species-transport calculation?

---

## 9. Quick Equation Sheet

| Category | Equation | Use |
| --- | --- | --- |
| Reynolds number | $Re_x=\rho v_\infty x/\mu$ | Classify and scale near-wall flow |
| Local velocity boundary layer | $\delta(x)\approx 5x/\sqrt{Re_x}$ | Thickness along a laminar flat plate |
| Average velocity boundary layer | $\overline\delta=10L/(3\sqrt{Re_L})$ | Mean thickness over a substrate |
| Carrier-gas flow scaling | $\overline\delta\propto Q^{-1/2}$ | Effect of changing flow at fixed properties |
| Fick's law | $J_A=-D_{AB}\,dC_A/dy$ | Molecular diffusive flux |
| Ideal-gas precursor concentration | $C_A=P_A/(RT)$ | Convert partial pressure to concentration |
| Gas-phase mass transfer | $J_g=h_g(C_g-C_s)$ | Gas-side supply |
| First-order surface reaction | $J_s=k_s C_s$ | Surface consumption |
| Overall deposition flux | $J=k_sh_gC_g/(k_s+h_g)$ | Combined gas transfer and reaction |
| Series resistances | $1/k_{\mathrm{overall}}=1/k_s+1/h_g$ | Identify controlling resistance |
| Surface Damköhler ratio | $Da_m=k_s/h_g$ | Distinguish limiting regimes |
| Arrhenius relation | $k_s=k_0e^{-E_a/(RT_s)}$ | Temperature-dependent surface kinetics |
| Standard Gibbs energy and equilibrium | $\Delta_rG^\circ=-RT\ln K$ | Calculate equilibrium from standard reaction Gibbs energy |
| Reaction Gibbs energy | $\Delta_rG=\Delta_rG^\circ+RT\ln Q$ | Test thermodynamic favorability at actual activities |
| Nusselt number | $Nu=hL/k_f$ | Convective heat-transfer similarity |
| Sherwood number | $Sh=h_mL/D_{AB}$ | Convective mass-transfer similarity |
| Prandtl and Schmidt numbers | $Pr=\nu/\alpha$, $Sc=\nu/D_{AB}$ | Compare thermal versus species diffusivity |
| Arrhenius two-temperature ratio | $R_{\mathrm{dep}}(T_2)/R_{\mathrm{dep}}(T_1)=\exp[(E_a/k_B)(1/T_1-1/T_2)]$ | Reaction-controlled rate comparison using $E_a$ in eV |

## 10. Transport-and-Separation Takeaways

- **Momentum transport** determines the carrier-gas flow field and velocity boundary-layer development.
- **Mass transport** determines how efficiently precursors move from the bulk gas to the substrate; diffusion and convection both matter.
- **Surface reactions** supply a boundary condition that couples mass transfer to deposition kinetics.
- **Uniform film thickness** requires considering transport, precursor depletion, reaction kinetics, reactor configuration, and operating pressure **together**.

*Model scope: These equations describe an idealized flat-plate, dilute-precursor CVD model. Actual CVD reactors can involve multicomponent diffusion, gas-phase reactions, thermal gradients, complex geometries, and non-first-order surface kinetics.*


---

# Transport Phenomena
Rate Laws For Diffusive Transport

## Rate Laws for Diffusive Transport

- **General form** — flux = -(coefficient)(driving force)

**Fourier’s law  Heat conduction**

```math
q = -k\dfrac{dT}{dy}
```

**Fick’s law  Species diffusion**

```math
J_A^* = -D_{AB} \dfrac{dc_a}{dy}
```

**Newton’s law of viscosity  Momentum transfer**

```math
\tau_{yx} = -\mu \dfrac{dv_x}{dy}
```

## Rate laws as concentration gradients

**Fourier’s law**

```math
q_{y} = -\alpha \dfrac{dc_{H}}{dy}
```

**Fick’s law**

```math
J_A^* = -D_{AB} \dfrac{dc_a}{dy}
```

**Newton’s law of viscosity**

```math
\tau_{yx} = -\nu \dfrac{dc_{p_x}}{dy}
```

**Kinematic viscosity**

```math
\nu = \dfrac{\mu}{\rho}
```

**Thermal diffusivity**

```math
\alpha = \dfrac{k}{\rho \hat{c_P}}
```

**Diffusivity of A in B**

```math
D_{AB}
```

**Prandtl number**

```math
\mathrm{Pr} = \dfrac{\nu}{\alpha} = \dfrac{\hat{C}_p \mu}{k}
```

**Schmidt number**

```math
\mathrm{Sc} = \dfrac{\nu}{D_{AB}} = \dfrac{\mu}{\rho D_{AB}}
```

## Heat transfer

**Heat flow**

```math
\dot{Q} = \dfrac{Q}{t}
```

**Heat flux**

```math
q = \dfrac{\dot{Q}}{A}
```

## Mass transfer

**Mass (species) transport**

```math
N_A = x_A (\sum N_i) + J_A^*
```

**Diffusion of A through a stagnant layer of B**

```math
N_A = -\dfrac{cD_{AB}}{1 - x_A}\dfrac{dx_A}{dy}\qquad N_A = -\dfrac{cD_{AB}}{L}\ln(1-x_A^s)
```

**Equimolar counter diffusion**

```math
N_A = -cD_{AB}\dfrac{dx_A}{dy}
```

**Reaction at catalytic surface  $\mathrm{A} \rightarrow 2\mathrm{B} \implies N_B = 2N_A$**

```math
N_A = -x_A N_A - cD_{AB}\dfrac{dx_A}{dy}
```

## Momentum transfer

- **Interpretation of $\tau_{yx}$**  
  1. viscous shear stress exerted on a $y$-plane in the $+x$-direction by the fluid of lesser $y$ on that of greater $y$  2. flux of $x$-momentum across a $y$-plane in the $+y$-direction

**Shear strain rate**

```math
\dot{\gamma} = \dfrac{dv_x}{dy}
```

**Hooke’s law  ★ Hookean solid**

```math
\tau_{yx} = -G \dfrac{dx}{dy} = -G \gamma
```

**Newton’s law of viscosity  ★ Newtonian fluid**

```math
\tau_{yx} = -\mu \dfrac{dv_x}{dy} = -\mu\dot{\gamma}
```

**General Newton’s law of viscosity**

```math
\tau_{yx} = -\eta(\dot{\gamma})\dot{\gamma}
```

**Viscosity function of power law fluid**

```math
\eta = m\dot{\gamma}^{n-1}
```

**Newton’s law of viscosity  ★ Power law fluid**

```math
\tau_{yx} = -m\dot{\gamma}^n
```

**Carreau equation  ★ Slurry**

```math
\dfrac{\eta - \eta_\infty}{\eta_o - \eta_\infty} = [1 + (\lambda\dot{\gamma})^2]^{(n-1)/2}
```

## Transport Coefficients of Fluids

*Context:* Ideal gas: Simple kinetic theory

**Average velocity**

```math
\bar{u} = \sqrt{\dfrac{8 k_B T}{\pi m}}
```

**Mean free path**

```math
\lambda = \dfrac{1}{\sqrt{2}\pi d^2 n}
```

**Number density**

```math
n = \dfrac{N}{V}
```

**Molecular flux in the y-direction**

```math
z = \frac{1}{4}n\bar{u}
```

**Average distance of molecules from ref plane when they initiate their jump**

```math
\bar{a} = \frac{2}{3}\lambda
```

**Viscosity of ideal gas**

```math
\mu = \dfrac{1}{3}\rho\bar{u}\lambda = \dfrac{2}{3\pi^{3/2}}\dfrac{\sqrt{mk_BT}}{d^2}
```

**Thermal conductivity of ideal gas**

```math
k = \dfrac{1}{3}\rho\hat{c_v}\bar{u}\lambda = \dfrac{2\hat{c_v}}{3\pi^{3/2}}\dfrac{\sqrt{mk_BT}}{d^2}
```

**Diffusivity of ideal gas A in B**

```math
D_{AB} = \dfrac{1}{3}\bar{u}_{AB}\lambda_{AB} = \dfrac{2}{\pi^{3/2}}\dfrac{\sqrt{{k_BT}^3/m_{AB}}}{d^2_{AB} P}
```

**Mean mass for diffusivity**

```math
m_{AB} = \dfrac{2m_A m_B}{m_A+m_B}
```

**Mean distance for diffusivity**

```math
d_{AB} = \frac{1}{2}(d_A + d_B)
```

**Prandtl number of monoatomic ideal gas**

```math
\mathrm{Pr}_{\text{mono}} = 1
```

**Schmidt number of general ideal gas**

```math
\mathrm{Sc} = 1
```

## Real gas: Chapman-Enskog equations

*Context:* ★ Moderate pressure

**Lenard-Jones potential**

```math
\varphi(r) = 4\varepsilon \left[\left(\dfrac{\sigma}{r}\right)^{12} - \left(\dfrac{\sigma}{r}\right)^6\right]
```

**Attractive force**

```math
F_{\text{attr}} = \dfrac{24\varepsilon}{r} \left[\left(\dfrac{\sigma}{r}\right)^{6} - 2\left(\dfrac{\sigma}{r}\right)^{12}\right]
```

**Viscosity of real gas (analytic)**

```math
\mu = \dfrac{5}{16\pi}\dfrac{\sqrt{\pi m k_BT}}{\sigma^2 \Omega_\mu}
```

**Thermal conductivity of real gas (analytic)**

```math
k = \dfrac{25}{32\pi} \dfrac{\sqrt{\pi m k_BT}}{\sigma^2 \Omega_k}\hat{c_v} = \dfrac{5}{2}\hat{c_v}\mu
```

**Viscosity of real gas**

```math
\mu\left(\mathrm{\frac{g}{cm \cdot s}}\right) = 2.6692 \times 10^{-5} \dfrac{\sqrt{\mathcal{M}T}}{\sigma^2 \Omega_\mu}
```

**Thermal conductivity of monoatomic real gas**

```math
k_{\text{mono}}\left(\mathrm{\frac{cal}{cm \cdot s \cdot K}}\right) = 1.989 \times 10^{-4} \dfrac{\sqrt{T / \mathcal{M}}}{\sigma^2 \Omega_k}
```

**Thermal conductivity of polyatomic real gas  Euken factor**

```math
k_{\text{poly}}\left(\mathrm{\frac{cal}{cm \cdot s \cdot K}}\right) = \left[ \hat{c_p} + \dfrac{5}{4}\dfrac{R}{\mathcal{M}} \right] \mu
```

**Diffusivity of real gas  $T [=] \mathrm{K} \\ P [=] \mathrm{atm} \\ \sigma_{AB} [=]$ Å**

```math
D_{AB}\left(\mathrm{\frac{cm^2}{s}}\right) = 2.63 \times 10^{-3} \dfrac{\sqrt{T^3 / \mathcal{M}_{AB}}}{P\sigma^2_{AB}\Omega_D}
```

**Mean molar mass for diffusivity**

```math
\mathcal{M}_{AB} = \dfrac{2\mathcal{M}_A \mathcal{M}_B}{\mathcal{M}_A + \mathcal{M}_B}
```

**Mean distance for diffusivity**

```math
\omega_{AB} = \frac{1}{2}(\omega_A + \omega_B)
```

**Viscosity at different temperatures**

```math
\mu(T_2) = \mu(T_1)\sqrt{\dfrac{T_2}{T_1}}\dfrac{\Omega_{\mu_1}}{\Omega_{\mu_2}}
```

**Diffusivity at different temperatures**

```math
D_{AB}(T_2) = D_{AB}(T_1)\left(\dfrac{T_2}{T_1}\right)^{3/2}\dfrac{\Omega_{D_1}}{\Omega_{D_2}}
```

**$T$ and $P$ dependence of transport coefficients of gases at moderate pressure**

```math
\begin{aligned}\mu &\propto\sqrt{T} \\ k_{\text{mono}} &\propto\sqrt{T} \\ k_{\text{poly}} &= f(T, \hat{c_p}(T)) \\ D_{AB} &\propto T^{3/2}P^{-1} \\ D_{AB} &= D_{BA}\end{aligned}
```

## Ideal gas mixtures

**Wilke equation  Viscosity of gas mixture**

```math
\mu_{\text{mix}} = \displaystyle\sum_{i=1}^{N}\dfrac{x_i \mu_i}{\sum_{j=1}^N x_j \Phi_{ij}}
```

**Wilke equation  Thermal conductivity of gas mixture**

```math
k_{\text{mix}} = \displaystyle\sum_{i=1}^{N}\dfrac{x_i k_i}{\sum_{j=1}^N x_j \Phi_{ij}}
```

**Wilke equation parameter**

```math
\Phi_{ij} = \frac{1}{\sqrt{8}} \left[ 1 + \frac{\mathcal{M}_i}{\mathcal{M}_j} \right]^{-1/2} \left[ 1 + \left[\frac{\mu_i}{\mu_j}\right]^{1/2} + \left[\frac{\mathcal{M}_i}{\mathcal{M}_j}\right]^{-1/4} \right]^2
```

**Blanc’s equation  Diffusivity of gas mixture**

```math
D_{i, \text{mix}} = \left[ \displaystyle\sum_{j \neq 1}^{N} \dfrac{x_j}{D_{ij}} \right]^{-1}
```

## Liquids

**Eyring model  Viscosity of liquid**

```math
\mu = \dfrac{N_A h}{\tilde{V}}\exp\left[ 0.408 \dfrac{\Delta U_{\text{vap}}}{RT} \right]
```

**Bridgeman equation  Thermal conductivity of liquid**

```math
k = 2.8 \left( \dfrac{N_A}{\tilde{V}}^{2/3} k_B v_s \right)
```

**Einstein equation**

```math
D_{AB} \approx \dfrac{k_BT}{f}
```

**Hydrodynamic friction factor**

```math
f = \begin{cases} 6\pi\mu_BR_A & \text{no slip} \\ 4\pi\mu_BR_A & \text{free slip} \end{cases}
```

**Stoke-Einstein Equation  Diffusivity of dilute liquid A**

```math
D_{AB} = \dfrac{k_BT}{4\pi\mu_BR_A}
```

**Wilke-Chang correlation  Diffusivity of dilute liquid A  $\tilde{V} [=] \mathrm{cm^3/mol} \\ \mu_B [=] \mathrm{cP} \\ T [=] \mathrm{K}$**

```math
D_{AB}\left(\mathrm{\frac{cm^2}{s}}\right) = 7.4 \times 10^{-8} \dfrac{(\psi_B \mathcal{M}_B)^{1/2} T}{\mu \tilde{V}_A^{0.6}}
```

**Vigne’s equation  Diffusivity of liquid mixture**

```math
D_{AB} = (D_{AB}^0)^{x_B} (D_{BA}^0)^{x_A}
```

**$T$ dependence of transport coefficients of liquids  (no $P$ dependence)**

```math
\begin{aligned} \mu &= Ae^{B/T} \\ D_{AB}\mu_B &\propto T \\ D_{AB} &\neq D_{BA} \end{aligned}
```

## Shell Balance (Bottom-Up)

*Context:* Boundary conditions and shell volume

**Rectilinear shell volume**

```math
\Delta V = LW\Delta y
```

**Cylindrical shell volume**

```math
\Delta V = 2\pi r L \Delta r
```

**Spherical shell volume**

```math
\Delta V = 4 \pi r^2 \Delta r
```

**Newton’s law of cooling**

```math
q = h(T_{\text{solid}} - T_{\text{fluid}})
```

**Relationship between $N_A$ and $c_A$ at boundary**

```math
N_A = k_m (c_{A, \text{solid}} - c_{A, \text{fluid}})
```

**Reynolds number**

```math
\mathrm{Re} = \dfrac{L_{\text{char}}v_{\text{char}}\rho}{\mu}
```

**No slip condition**

```math
v_1 = v_2
```

**Free slip condition**

```math
-\mu_1\left(\dfrac{dv_x}{dy}\right)_1 = 0
```

**Continuity of stress**

```math
\begin{aligned}\tau_{y, 1} &= \tau_{y, 2} \\ -\mu_1\left(\dfrac{dv_x}{dy}\right)_1 &= -\mu_2\left(\dfrac{dv_x}{dy}\right)_2 \end{aligned}
```

- **Shell balance method**  
  Sketch the system with coordinate system  Sketch the shell that is thin in the direction of transport (change)  Write shell volume $\Delta V$  Write shell balance OIGA of transported quantity  $\mathrm{out - in = generation - accumulation}$

- **Take limit as shell thickness approach 0** — Differential equation of flux distribution

- **Separate variable and integrate**  
  Flux distribution, $c_1$

- **Substitute rate law**  
  Separate variable and integrate  Profile, $c_1, c_2$

## Evaluate $c_1, c_2$ using boundary conditions

*Context:* Axial transport in rectilinear systems; Rectilinear coordinates; No generation; No driving force; Steady state

**Differential equation of flux distribution**

```math
\dfrac{dq}{dy} = 0
```

**Temperature profile (linear)**

```math
T(y) = T_1 - \dfrac{q}{k} y
```

**Flux distribution (inverse)**

```math
q(y) = \dfrac{k(T_1 - T)}{y}
```

**Flux across the whole layer**

```math
q = \dfrac{k(T_1 - T_2)}{H}
```

## Radial transport in cylindrical systems

*Context:* Cylindrical coordinates; No generation; No driving force; Steady state

**Differential equation of flux distribution**

```math
\dfrac{d(rq)}{dr} = 0
```

**Flux distribution (inverse)**

```math
q(r) = \dfrac{k(T_i - T_0)}{r \ln(\frac{R_0}{R_i})}
```

**Temperature profile (logarithmic)**

```math
T(r) = T_i - \dfrac{T_i - T_0}{\ln(\frac{R_0}{R_i})} \ln\left(\dfrac{r}{R_i}\right)
```

## Radial transport in spherical systems

*Context:* Spherical coordinates; No generation; No driving force; Steady state

**Differential equation of flux distribution**

```math
\dfrac{d(r^2 q)}{dr} = 0
```

**Flux distribution (inverse squared)**

```math
q(r) = \dfrac{k(T_i - T_0)}{r^2 (\frac{1}{R_i} - \frac{1}{R_0})}
```

**Temperature profile (inverse)**

```math
T(r) = T_i - \dfrac{T_i - T_0}{(\frac{1}{R_i} - \frac{1}{R_0})} \left(\dfrac{1}{r} - \dfrac{1}{R_i}\right)
```

## Axial transport in rectilinear systems (with generation)

*Context:* Rectilinear coordinates; With generation; No driving force; Steady state

**Differential equation of flux distribution**

```math
\dfrac{dq}{dy} = S
```

**Flux distribution (linear)**

```math
q(y) = Sy + \dfrac{k}{H}(T_2 - T_1) - \dfrac{SH}{2}
```

**Temperature profile (quadratic)**

```math
T(y) = T_1 - \dfrac{S}{2k} y^2 + \left[ \dfrac{SH}{2k} - \dfrac{T_2 - T_1}{H} \right] y
```

## Flow down inclined plane (falling film)

*Context:* Rectilinear coordinates; Gravity driving force, but no pressure gradient; Steady state

**Differential equation of flux distribution**

```math
\dfrac{d\tau_{yx}}{dy} = \rho g \cos\beta
```

**Flux distribution (linear)**

```math
\tau_{yx}(y) = -\rho g \cos\beta (\delta - y)
```

**Velocity profile (quadratic)**

```math
v_x(y) = \dfrac{g \cos\beta}{2\nu}(2\delta y - y^2)
```

**★ No entry length effect**

```math
L \gg \delta
```

**★ No edge effect**

```math
W \gg \delta
```

**★ Incompressible Newtonian fluid**

```math
\Delta\mu = 0, \Delta\rho = 0
```

**★ No end effect, no ripple**

```math
\mathrm{Re}_{\text{rippling}} \lesssim 20
```

**Reynolds number for falling film**

```math
\mathrm{Re} = \dfrac{4\delta \langle v_x \rangle\rho}{\mu}
```

## Flow descriptors

**Skin friction**

```math
\tau^0 = \rho g \cos(\beta)\delta
```

**Free surface velocity**

```math
v_x^{\text{surf}} = \dfrac{g \cos\beta}{2\nu}\delta^2
```

**Volumetric flow rate**

```math
Q = \int v_\perp \ dA
```

**Volumetric flow rate per unit area**

```math
\dfrac{Q}{W} = \dfrac{g \cos(\beta) \delta^3}{3\nu}
```

**Average velocity**

```math
\langle v_x \rangle = \dfrac{g\cos(\beta)\delta^2}{3\nu}
```

**Mass flow rate**

```math
\dot{m} = \rho Q
```

**Mass flow rate per unit width**

```math
\Gamma = \dfrac{\rho Q}{W} = \dfrac{\rho g \cos(\beta) \delta^3}{3\nu}
```

**Film thickness given $\Gamma$**

```math
\delta = \sqrt[3]{\dfrac{3\nu \Gamma}{\rho g \cos\beta}}
```

## Flow in round tube (Hagen-Poiseuille flow)

*Context:* Cylindrical coordinates; Pressure-gravity driving force; Steady state; No tube bents, constant cross section; Negligible P dependence with r

**Modified pressure**

```math
\mathcal{P} = P + \rho gh
```

**Pressure-gravity driving force**

```math
-\dfrac{dP}{dz} + \rho g \cos\beta = \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L}
```

**Differential equation of flux distribution**

```math
\dfrac{d (r\tau_{rz})}{dr} = \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) r
```

**Flux distribution (linear)**

```math
\tau_{rz}(r) = \dfrac{1}{2} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) r
```

**Velocity profile (quadratic)**

```math
v_z(r) = \dfrac{R^2}{4\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) \left[ 1 - \left( \dfrac{r}{R} \right)^2 \right]
```

**★ Incompressible Newtonian fluid**

```math
\Delta\mu = 0, \Delta\rho = 0
```

**★ Laminar flow**

```math
\mathrm{Re}_{\text{laminar}} \le 2100
```

**★ Fully developed flow (no entry length effect)**

```math
L_e \approx 0.035 D \mathrm{Re}
```

**Reynolds number for pipe flow**

```math
\mathrm{Re}_{\text{pipe}} = \dfrac{D \langle v_z \rangle\rho}{\mu}
```

## Flow descriptors

**Skin friction**

```math
\tau_{rz}^0 = \dfrac{1}{2} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) R
```

**Volumetric flow**

```math
Q = \dfrac{R^4 \pi}{8 \mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)
```

**Average velocity**

```math
\langle v_z \rangle = \dfrac{R^2}{8\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)
```

**Mass flow rate**

```math
\dot{m} = \dfrac{R^4 \pi\rho}{8\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)
```

## Laminar flow through porous media

**Darcy’s law - average velocity  $\kappa$ - bed permeability**

```math
\langle v \rangle = \dfrac{\kappa}{\mu L}(\mathcal{P}_1 - \mathcal{P}_2)
```

**Darcy’s law - volumetric flow rate  $A$ - empty bed cross section  $\varepsilon$ - porosity, void fraction**

```math
Q = \dfrac{\kappa A \varepsilon}{\mu L}(\mathcal{P}_1 - \mathcal{P}_2)
```

**Blake-Kozeny model  Bed permeability**

```math
\kappa = \dfrac{D_p^2}{150} \left( \dfrac{\varepsilon}{1 - \varepsilon} \right)^2
```

**Effective packing particle diameter**

```math
\begin{gathered}
D_p = \dfrac{6}{a_v} = \dfrac{6 V}{A} \\
D_{p, \text{spheres}} = D
\end{gathered}
```

**Bed Reynolds number**

```math
\mathrm{Re}_{\text{bed}} = \dfrac{D_p Q \rho}{\mu A (1-\varepsilon)}
```

**★ Laminar flow**

```math
\mathrm{Re}_{\text{laminar}} < 10
```

## Fluid pressure, hydrostatic, manometer

**Equation of hydrostatic**

```math
P_1 - P_2 = \rho g(h_2 - h_1)
```

**Manometer equation**

```math
P_1 - P_2 = (\rho_m - \rho) gH + \rho g(h_2 - h_1)
```

**Manometer equation**

```math
\mathcal{P}_1 - \mathcal{P}_2 = (\rho_m - \rho) gH
```

## Unsteady state transport

**Unsteady state conduction in rectilinear system**

```math
\left(\dfrac{\partial T}{\partial t}\right)_y = \alpha \dfrac{\partial^2 T}{\partial y^2} + \dfrac{S}{\rho \hat{c_p}}
```

**Unsteady state diffusion in rectilinear system**

```math
\left(\dfrac{\partial c_A}{\partial t}\right)_y = D_{AB} \dfrac{\partial^2 c_A}{\partial y^2} + R_A
```

**Unsteady state Couette flow (1D rectilinear shear flow)**

```math
\left(\dfrac{\partial v_x}{\partial t}\right)_y = \nu \left(\dfrac{\partial^2 v_x}{\partial y^2}\right)_t
```

**Unsteady state flow in cylindrical system**

```math
\left(\dfrac{\partial v_z}{\partial t}\right)_r = \nu \left[ \dfrac{\partial^2 v_z}{\partial r^2} + \dfrac{1}{r} \dfrac{\partial v_z}{\partial r} \right] + \dfrac{1}{\rho} \left[\dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L}\right]
```

## Rate Laws in 3D

**Fourier’s law in 3D**

```math
\boldsymbol{q} = -k \nabla T
```

**Fick’s law in 3D**

```math
\boldsymbol{J}_A^* = -D_{AB} \nabla c_A
```

**Newton’s law of viscosity in 3D**

```math
\boldsymbol{\tau} = -\mu (\boldsymbol{\Delta} + \boldsymbol{\Delta}^{\dagger})
```

**Viscous stress tensor**

```math
\boldsymbol{\tau} = \begin{bmatrix} \tau_{xx} & \tau_{xy} & \tau_{xz} \\ \tau_{yx} & \tau_{yy} & \tau_{yz} \\ \tau_{zx} & \tau_{zy} & \tau_{zz} \end{bmatrix}
```

**Rate of strain tensor**

```math
\boldsymbol{\Delta} = \begin{bmatrix} \dfrac{\partial v_x}{\partial x} & \dfrac{\partial v_x}{\partial y} & \dfrac{\partial v_x}{\partial z} \\ \\ \dfrac{\partial v_y}{\partial x} & \dfrac{\partial v_y}{\partial y} & \dfrac{\partial v_y}{\partial z} \\ \\ \dfrac{\partial v_z}{\partial x} & \dfrac{\partial v_z}{\partial y} & \dfrac{\partial v_z}{\partial z} \end{bmatrix}
```

## Conservation Laws in 3D

**Conservation of thermal energy**

```math
\nabla\cdot\boldsymbol{q} = S - \rho \hat{c_p} \dfrac{\partial T}{\partial t}
```

**Conduction equation  ★ No convection**

```math
\dfrac{\partial T}{\partial t} = \alpha \nabla^2 T + \dfrac{S}{\rho \hat{c_p}}
```

**Molecular diffusion equation  ★ No convection**

```math
\dfrac{\partial c_A}{\partial t} = D_{AB} \nabla^2 c_A + R_A
```

# Fluid Mechanics
Navier-Stokes Equation

## Navier-Stokes Equation

**Continuity equation**

```math
\dfrac{\partial \rho}{\partial t} + \nabla\cdot(\rho\boldsymbol{v}) = 0
```

**Continuity equation of incompressible liquid  ★ Constant $\rho$**

```math
\nabla\cdot\boldsymbol{v} = 0
```

**Equation of motion ($v$-form)**

```math
\rho\dfrac{D\boldsymbol{v}}{Dt} = -\nabla p + \mu\nabla^2\boldsymbol{v} + \rho g
```

**Equation of motion ($\tau$-form)**

```math
\rho\dfrac{D\boldsymbol{v}}{Dt} = -\nabla p - \nabla\cdot\boldsymbol{\tau} + \rho g
```

**Equation of motion ($x$-component)**

```math
\begin{aligned} &\rho \left[ \dfrac{\partial v_x}{\partial t} + \boldsymbol{v}\cdot\nabla v_x \right] \\ =& -\dfrac{\partial p}{\partial x} - \left[ \dfrac{\partial \tau_{xx}}{\partial x} + \dfrac{\partial \tau_{yx}}{\partial y} + \dfrac{\partial \tau_{zx}}{\partial z} \right] + \rho g_x \end{aligned}
```

## Operators

Gradient operator $\nabla$ Operates on scalar to give a vector, whose magnitude is the maximum rate of change of the scalar with position, and whose direction points in the direction of that change

Divergence operator $(\nabla\cdot)$ Operates on a vector to give a scalar

Divergence of a flux vector $(\nabla\cdot\boldsymbol{f})$ Rate of efflux (outflow) of the transported quantity per unit volume

**Laplacian operator**

```math
\nabla^2 = \nabla\cdot\nabla
```

**Substantial derivative operator**

```math
\dfrac{D}{Dt} = \dfrac{\partial}{\partial t} + \boldsymbol{v}\cdot\nabla
```

## Generalization to convection

**Thermal energy equation**

```math
\dfrac{DT}{Dt} = \alpha \nabla^2 T + \dfrac{S}{\rho \hat{c_p}}
```

**Convective diffusion equation**

```math
\dfrac{D c_A}{Dt} = D_{AB} \nabla^2 c_A + R_A
```

## Flow in conduit

**Mach number**

```math
\mathrm{Ma} = \dfrac{v_{\text{char}}}{v_{\text{sound}}}
```

**Conduit flow**

```math
\begin{aligned} \dot{m}_1 &= \dot{m}_2 \\ \rho_1 Q_1 &= \rho_2 Q_2 \end{aligned}
```

**Incompressible conduit flow  ★ Constant $\rho$**

```math
\begin{aligned} Q_1 &= Q_2 \\ A_1 \langle v \rangle_1 &= A_2 \langle v \rangle_2 \end{aligned}
```

## Apply N-S Equations (Top-Down) Flow between parallel plates

**Rectilinear coordinates**

```math
f(x, y, z)
```

**Constant $\rho, \mu$**

```math
\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0
```

**Laminar flow**

```math
\mathrm{Re} < \mathrm{Re}_{\text{cr}}
```

**Steady state**

```math
\frac{\partial}{\partial t} = 0
```

**$v_x$ component only**

```math
v_y = v_z = 0
```

**No edge effect**

```math
\frac{\partial}{\partial z} = 0
```

**No end effect**

```math
\frac{\partial v_x}{\partial x} = 0
```

## No hydrostatic pressure diff between plates

*Context:* $b \ll W, L \implies -\frac{\partial p}{\partial y} + \rho g_y = 0$

**$x$-momentum equation**

```math
\dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} + \mu\dfrac{\partial^2 v_x}{\partial y^2} = 0
```

**Velocity profile (quadratic)**

```math
v_x(y) = \dfrac{1}{2\mu}\left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)(-y^2 + by)
```

**Average velocity**

```math
\langle v_x \rangle = \dfrac{b^2}{12\mu}\left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)
```

**Skin friction at bottom plate**

```math
\tau^0 = \dfrac{b}{2} \left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)
```

## Couette flow between concentric rotating cylinders

**Cylindrical coordinates**

```math
f(r, \theta, z)
```

**Constant $\rho, \mu$**

```math
\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0
```

**Laminar flow**

```math
\mathrm{Re} < \mathrm{Re}_{\text{cr}}
```

**Steady state**

```math
\frac{\partial}{\partial t} = 0
```

**$v_\theta$ component only**

```math
v_r = v_z = 0
```

**Axial symmetry**

```math
\frac{\partial}{\partial \theta} = 0
```

**No end effect**

```math
\frac{\partial v_\theta}{\partial z} = 0
```

## Vertical orientation

*Context:* $g_z = -g, g_\theta = g_r = 0$

**$r$-momentum equation**

```math
-\rho\dfrac{v_\theta^2}{r} = -\dfrac{\partial p}{\partial r}
```

**$\theta$-momentum equation**

```math
\mu\dfrac{\partial}{\partial r} \left( \dfrac{1}{r}\dfrac{\partial}{\partial r} (rv_\theta) \right) = 0
```

**$z$-momentum equation**

```math
-\dfrac{\partial p}{\partial z} - \rho g = 0
```

**Velocity profile (general form)**

```math
v_\theta(r) = c_1\dfrac{r}{2} + \dfrac{c_2}{r}
```

**Velocity profile**

```math
v_\theta(r) = \dfrac{\Omega_0}{1 - \kappa^2}\left[r - \dfrac{(\kappa R)^2}{r}\right]
```

**Pressure profile**

```math
P - P_{\kappa R} = \dfrac{1}{2}\rho \left(\dfrac{\Omega_0\kappa R}{1-\kappa^2}\right)^2 \left[\left(\dfrac{r}{\kappa R}\right)^2 - \left(\dfrac{\kappa R}{r}\right)^2 - 4\ln\left(\dfrac{r}{\kappa R}\right) \right]
```

**Shear stress distribution**

```math
\tau_{r\theta} = -2\mu\kappa^2\left(\dfrac{\Omega_0}{1-\kappa^2}\right)\left(\dfrac{R}{r}\right)^2
```

**Torque**

```math
\mathcal{T} = 4\pi\mu L \Omega_0 R^2\dfrac{\kappa^2}{1 - \kappa^2}
```

**Couette viscometer**

```math
\mu = \dfrac{\mathcal{T}}{4\pi L \Omega_0 R^2}\dfrac{1 - \kappa^2}{\kappa^2}
```

## Stoke’s law: Flow around a sphere

**Spherical coordinates**

```math
f(r, \theta, \phi)
```

**Constant $\rho, \mu$**

```math
\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0
```

**Laminar flow**

```math
\mathrm{Re} < \mathrm{Re}_{\text{cr}}
```

**Steady state**

```math
\frac{\partial}{\partial t} = 0
```

**Axial symmetry**

```math
\frac{\partial}{\partial \phi} = 0
```

**No spinning**

```math
v_\phi = 0
```

**Vertical orientation**

```math
g_r = -g \cos\theta, g_\theta = g \sin\theta, g_\phi = 0
```

## $v_\theta$ component only

*Context:* $v_r = v_z = 0$

**$r$ velocity profile**

```math
v_r = v_\infty \left[ 1 - \dfrac{3}{2}\left(\dfrac{R}{r}\right) + \dfrac{1}{2}\left(\dfrac{R}{r}\right)^2 \right] \cos\theta
```

**$\theta$ velocity profile**

```math
v_\theta = -v_\infty \left[ 1 - \dfrac{3}{4}\left(\dfrac{R}{r}\right) - \dfrac{1}{4}\left(\dfrac{R}{r}\right)^3 \right] \sin\theta
```

**Pressure profile**

```math
p = p_0 - \rho gz - \dfrac{3}{2}\dfrac{\mu v_\infty}{R}\left(\dfrac{R}{r}\right)^2 \cos\theta
```

**Viscous drag**

```math
4\pi\mu v_\infty R
```

**Pressure force (buoyancy + form frag)**

```math
\frac{4}{3}\pi R^3 \rho g + 2\pi R \mu v_\infty
```

**Stoke’s law**

```math
v_\infty = \dfrac{2R^2 (\rho_s - \rho)g}{9\mu}
```

**Falling ball viscometer**

```math
\mu = \dfrac{2R^2 (\rho_s - \rho)g}{9 v_\infty}
```

## Centrifuge viscometer

**Terminal velocity**

```math
v_\infty = \dfrac{2R^2 (\rho_s - \rho) \omega ^2r}{9\mu}
```

**Centrifuge viscometer**

```math
\mu = \dfrac{2R^2 (\rho_s - \rho)\omega^2}{9 \ln\left(\frac{R_2}{R_1}\right)} \Delta t
```

- **Turbulence** — Transition to turbulence

- **Geometry** — Reynolds Number; Critical Reynolds Number

**Circular tube flow**

```math
\mathrm{Re} = \dfrac{D \langle v \rangle \rho}{\mu}\qquad \mathrm{Re_c} \approx 2100
```

**Falling film**

```math
\mathrm{Re} = \dfrac{4 \delta \langle v \rangle \rho}{\mu}\qquad \mathrm{Re_c} \approx 1500
```

**Flow between parallel plates**

```math
\mathrm{Re} = \dfrac{2b \langle v \rangle \rho}{\mu}\qquad \mathrm{Re_c} \approx 1780
```

**Tangential flow in an annulus (Couette flow between rotating cylinders)**

```math
\mathrm{Re} = \dfrac{\Omega_0 R^2 \langle v \rangle \rho}{\mu}\qquad \mathrm{Re_c} \approx 50000
```

Laminar vs. turbulent

- **Property**  
  Laminar Flow $(\mathrm{Re} < 2100)$  Turbulent Flow $(\mathrm{Re} \in [10^4, 10^5])$

**Velocity profile**

```math
\dfrac{v_z}{v_{z, \max}} = 1 - \left(\dfrac{r}{R}\right)^2\qquad \dfrac{v_z}{v_{z, \max}} \approx \left(1 - \dfrac{r}{R}\right)^{1/7}
```

**Average velocity**

```math
\langle v_z \rangle = \frac{1}{2}v_{z, \max}\qquad \langle v_z \rangle \approx \frac{4}{5}\bar{v}_{z, \max}
```

**Volumetric flow rate**

```math
Q = \dfrac{\pi R^4}{8\mu} \left(\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right)\qquad Q \propto \left(\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right)^{4/7}
```

**Entry length**

```math
L_e = 0.035 D \mathrm{Re}\qquad L_e \approx 40D
```

## Derivation

*Context:* From theory; From experiment

**Velocity decomposition**

```math
v_z = \bar{v}_z + v_z'
```

**Velocity profile in turbulent flow**

```math
\bar{v}_z = \bar{v}_{z, \max}\left(1 - \dfrac{r}{R}\right)^{1/n}\qquad n = \begin{cases} 6 & \mathrm{Re} \in [2\times 10^3, 10^4] \\ 7 & \mathrm{Re} \in [10^4, 10^5] \\ 8 & \mathrm{Re} \in [10^5, 10^6] \end{cases}
```

## Time-smoothed N-S equation

**Time-smoothed continuity equation**

```math
\begin{gathered}
\nabla\cdot\boldsymbol{\bar{v}} = 0 \\
\nabla\cdot\boldsymbol{v}' = 0
\end{gathered}
```

**Time-smoothed equation of motion ($\tau$-form)**

```math
\rho\dfrac{D\boldsymbol{\bar{v}}}{Dt} = -\nabla \bar{p} - \nabla\cdot\boldsymbol{\bar{\tau}}^{\text{total}} + \rho g
```

**Time-smoothed equation of motion ($x$-component)**

```math
\begin{aligned} &\rho \left[ \dfrac{\partial \bar{v}_x}{\partial t} + \boldsymbol{\bar{v}}\cdot\nabla \bar{v}_x \right] \\ =& -\dfrac{\partial \bar{p}}{\partial x} - \left[ \dfrac{\partial \bar{\tau}^{\text{total}}_{xx}}{\partial x} + \dfrac{\partial \bar{\tau}^{\text{total}}_{yx}}{\partial y} + \dfrac{\partial \bar{\tau}^{\text{total}}_{zx}}{\partial z} \right] + \rho g_x \end{aligned}
```

**Total shear stress (viscous + turbulent)**

```math
\begin{aligned} \bar{\tau}^{\text{total}}_{yx} &= \bar{\tau}_{yx}^{(v)} + \bar{\tau}_{yx}^{(t)} \\ &= \bar{\tau}_{yx} + \rho \overline{v_y' v_x'} \end{aligned}
```

## Shear stress distribution

**Shear stress distribution in round tube**

```math
\tau_{r\theta} = \dfrac{1}{2}\left[\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right]r
```

**Shear stress distribution in general conduit**

```math
\tau_{r\theta} = \left[\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right] R_H
```

**Hydraulic radius**

```math
R_H = \mathrm{\dfrac{cross \ sectional \ area}{wetted \ perimeter}}
```

**Characteristic length**

```math
l_{\text{char}} = 4R_H
```

**Characteristic velocity**

```math
v_{\text{char}} = \langle v_z \rangle
```

Universal velocity profile

- **Layer** — Normalized velocity; Normalized length range

**Laminar sublayer**

```math
v^+ = y^+\qquad y^+ \in (0, 5)
```

**Buffer layer**

```math
v^+ = 5 \ln(y^+ + 0.205) - 3.27\qquad y^+ \in (5, 30)
```

## Turbulent core

*Context:* $v^+ = 2.5 \ln(y^+) + 5.5$; $y^+ \in (30, \infty)$

**Characteristic length**

```math
y_* = \dfrac{\mu}{v_* \rho}
```

**Characteristic velocity**

```math
v_* = \sqrt{\dfrac{\tau^0}{\rho}}
```

**Normalized length**

```math
y^+ = \dfrac{y}{y_*}
```

**Normalized velocity**

```math
v^+ = \dfrac{v}{v_*}
```

**Eddie viscosity**

```math
\mu^{(t)} = - \dfrac{\bar{\tau}_{yz}^{\text{total}}}{\left(\frac{dv_z}{dy}\right)} - \mu = - \dfrac{\left[\frac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right] \frac{r}{2}}{\left(\frac{dv_z}{dy}\right)} - \mu
```

## Dynamic Similarity and Dimensional Analysis

*Context:* Flow around a sphere outside of Stoke’s law

**★ Non-Stoke’s law condition**

```math
\mathrm{Re} \ge 0.1
```

**Nondimensionalized continuity equation**

```math
\breve{\nabla}\cdot\boldsymbol{\breve{v}} = 0
```

**x-component of momentum equation**

```math
\dfrac{D\breve{v}_x}{D\breve{t}} = -\dfrac{\partial\breve{p}}{\partial\breve{x}} + \dfrac{1}{\mathrm{Re}}\breve{\nabla}^2 \breve{v}_x + \dfrac{1}{\mathrm{Fr}}\breve{g}_x
```

**Drag coefficient  Friction factor**

```math
c_D = f = \dfrac{F_D}{\frac{1}{2}\rho v_\infty^2 A_{\text{approach}}}
```

**Drag coefficient in Stoke’s law region**

```math
c_D = \dfrac{24}{\mathrm{Re}}
```

**Drag coefficient in non-Stoke’s law region**

```math
c_D = \left(\sqrt{\dfrac{24}{\mathrm{Re}}} + 0.5407\right)^2
```

## Dimensionless groups

**Reynolds number**

```math
\mathrm{Re} = \dfrac{l_0 v_0 \rho}{\mu} = \mathrm{\dfrac{inertial \ forces}{viscous \ forces}}
```

**Froude number**

```math
\mathrm{Fr} = \dfrac{v_0^2}{gl_0} = \mathrm{\dfrac{inertial \ forces}{gravitational \ forces}}
```

**Capillary number**

```math
\mathrm{Ca} = \dfrac{\mu v_0}{\sigma} = \mathrm{\dfrac{viscous \ forces}{surface \ tension \ forces}}
```

**Weber number**

```math
\mathrm{Fr} = \dfrac{l_0 \rho v_0^2}{\sigma} = \mathrm{\dfrac{inertial \ forces}{surface \ tension \ forces}}
```

**Euler’s number**

```math
\mathrm{Eu} = \dfrac{(\Delta p)D^4}{\rho Q^2}
```

- **Dimensional analysis**  
  Buckingham $\pi$ theorem - A function $f(X_1, X_2, \dots, X_k)$ with dimensional variables $X_i$ can be rewritten in a function $\Phi(\Pi_1, \Pi_2, \dots, \Pi_{k-n})$ with dimensionless variables $\Pi_j$ by enforcing dimensional consistency using $n$ fundamental dimensions.  Define fundamental dimensions  Choose stand-in variables for fundamental dimensions  Rewrite other variables in terms of stand-in variables to get dimensionless groups

## Bernoulli Analysis and Applications N-S equation for steady flow in stream tubes

**Constant density fluid**

```math
\Delta \rho = 0
```

**1D flow in $z$ direction**

```math
v_r = v_\theta = 0
```

**Plug flow - uniform velocity across cross section**

```math
\begin{gathered}
\langle v \rangle = v = \mathrm{constant} \\
v_z = v_z(z)
\end{gathered}
```

**Inviscid flow**

```math
\mu \approx 0, \mathrm{Re} \ge 10000
```

## No sharp bends

*Context:* Straight stream lines

**Continuity equation**

```math
\begin{aligned} Q_1 &= Q_2 \\ A_1 \langle v \rangle_1 &= A_2 \langle v \rangle_2 \end{aligned}
```

**Equation of motion**

```math
\rho v \dfrac{dv}{dz} = -\dfrac{dp}{dz} - \rho g \dfrac{dh}{dz}
```

## Bernoulli equation

**Bernoulli equation (energy form)**

```math
p_1 + \frac{1}{2}\rho v_1^2 + \rho gh_1 = p_2 + \frac{1}{2}\rho v_2^2 + \rho gh_2
```

**Bernoulli equation (head form)**

```math
\dfrac{v_1^2}{2g} + \dfrac{p_1}{\rho g} + h_1 = \dfrac{v_2^2}{2g} + \dfrac{p_2}{\rho g} + h_2
```

**Bernoulli head**

```math
\mathcal{B} = \dfrac{v^2}{2g} + \dfrac{p}{\rho g} + h = \mathrm{constant}
```

**Drag coefficient**

```math
c_D = \dfrac{F_D}{\frac{1}{2}\rho v_\infty^2 A_{\text{approach}}}
```

**Lift coefficient**

```math
c_L = \dfrac{F_L}{\frac{1}{2}\rho v_\infty^2 A_{\text{planform}}}
```

**Pressure change in contracting conduit  $\Delta p \equiv p_1 - p_2$**

```math
\Delta p = \dfrac{8\rho Q^2}{\pi^2 D_1^4}\left[\left(\dfrac{D_1}{D_2}\right)^4 - 1\right] + \rho g (h_2 - h_1)
```

**Torricelli’s law**

```math
\langle v \rangle = \sqrt{2g\Delta h}
```

**Pressure at stagnation point**

```math
\begin{aligned} p &= p_{\text{static}} + p_{\text{dynamic}} \\ &= p_{\text{static}} + \textstyle\frac{1}{2}\rho v_\infty^2 \end{aligned}
```

## Flow-metering devices

**Manometer equation**

```math
\Delta p = (\rho_\mathrm{m} - \rho)gH
```

**Local velocity  Pitot tube**

```math
v = \sqrt{\dfrac{2\Delta p}{\rho}}
```

**Volumetric flow rate  Venturi meter $c_0 \in [0.96, 0.98]$  Orfice meter $c_0 \in [0.40, 0.80]$  Nozzle meter $c_0 \in [0.96, 0.98]$**

```math
Q = c_0\pi D_0^2 \sqrt{\dfrac{\Delta p}{8\rho [1 - (\frac{D_0}{D})^4]}}
```

- **Rotameter** — Calibrated specifically to the fluid with falling sphere

## Full Bernoulli analysis

**Full Bernoulli equation**

```math
\dfrac{v_1^2}{2g} + \dfrac{p_1}{\rho g} + h_1 = \dfrac{v_2^2}{2g} + \dfrac{p_2}{\rho g} + h_2 + H_{L12}
```

**Head loss**

```math
H_{L12} = H_{L12f} + H_{L12c}
```

Skin friction loss $H_{L12f}$ Viscous work done per unit weight by fluid on walls of conduit in moving from 1 to 2

**Skin friction loss (general)**

```math
H_{L12f} = \dfrac{\tau^0 L}{\rho g R_H}
```

**Skin friction loss for circular tube**

```math
H_{L12f} = \dfrac{4\tau^0 L}{\rho g D}
```

**Fanning friction factor**

```math
f = \dfrac{\tau^0}{\frac{1}{2}\rho \langle v \rangle^2}
```

**Skin friction loss for circular tube**

```math
H_{L12f} = \dfrac{2\langle v \rangle^2 L}{g D}f = \dfrac{32Q^2 L}{\pi^2 D^5 g}f
```

**Skin friction loss for non-circular tube**

```math
H_{L12f} = \dfrac{\langle v \rangle^2 L}{2 g R_H}f = \dfrac{Q^2 L}{2g A_c^2 R_H}f
```

**Reynolds number for noncircular pipes**

```math
\mathrm{Re} = \dfrac{4R_H \langle v \rangle \rho}{\mu}
```

**Configurational loss of one fitting in circular tube**

```math
H_{Lc} = e_v\dfrac{\langle v \rangle^2_{\text{downstream}}}{2g}
```

**Configurational loss of all fittings in circular tube**

```math
H_{L12c} = \dfrac{\langle v \rangle^2_{\text{down}}}{2g} (\sum\limits_i e_{v, i}) = \dfrac{8Q^2}{\pi^2 D^4 g} (\sum\limits_i e_{v, i})
```

**Total head loss for circular tube**

```math
H_{L12} = \begin{cases} \dfrac{2 \langle v \rangle^2}{Dg} [(\sum\limits_i L_i)f + \frac{D}{4} (\sum\limits_i e_{v, i})] \\ \dfrac{32 Q^2}{\pi^2 D^5 g} [(\sum\limits_i L_i)f + \frac{D}{4} (\sum\limits_i e_{v, i})] \end{cases}
```

**Kinetic head correction factor**

```math
\alpha = \dfrac{\langle v^3 \rangle}{\langle v \rangle^3}
```

**Brake horse power**

```math
\mathrm{bhp} = \dfrac{P}{\eta} = \dfrac{H_p \rho g Q}{\eta}
```

## Fanning friction factor correlations

- **Description** — Equations; Conditions

**Hydraulically smooth pipes (Blasius)**

```math
f = \dfrac{0.0791}{\mathrm{Re}^1/4}\qquad \mathrm{Re} \in [2100, 10^5]
```

**Hydraulically smooth pipes (Koo)**

```math
f = 0.0014 + \dfrac{0.125}{\mathrm{Re}^{0.32}}\qquad \mathrm{Re} \in [10^4, 10^7]
```

**Pipes of general roughness (Haaland)**

```math
\begin{gathered}
\dfrac{1}{\sqrt{f}} = -3.6\log_{10} \left[\dfrac{6.9}{\mathrm{Re}} + \left(\dfrac{k/D}{3.7}\right)^{10/9}\right]\qquad \mathrm{Re} \in [4\times 10^4, 10^7] \\
k/D < 0.05
\end{gathered}
```

**Commercial standard piping (Drew)**

```math
\begin{gathered}
f = 0.0014 + \dfrac{0.090}{\mathrm{Re}^{0.27}}\qquad \mathrm{Re} \in [10^4, 10^7] \\
k/D \approx 0.00015
\end{gathered}
```

**Full rough conduit**

```math
\begin{gathered}
\dfrac{1}{\sqrt{f}} = 2.28 - 4.0 \log_{10} \left(\dfrac{k}{D}\right)\qquad \mathrm{Re} > 10^4 \\
k/D > 0.01
\end{gathered}
```

Kinetic head correction factor

**$\mathrm{Re}$**

```math
n\qquad \alpha
```

**$2 \times 10^3 \sim 10^4$**

```math
6\qquad 1.08
```

**$10^4 \sim 10^5$**

```math
7\qquad 1.06
```

**$10^5 \sim 10^7$**

```math
8\qquad 1.05
```

## Flow through packed bed

**Specific area of packing element**

```math
a_v = \dfrac{\text{area of packing element}}{\text{volume of packing element}}
```

**Effective diameter of packing element (particle)**

```math
D_p = \dfrac{6}{a_v}
```

**Darcy’s law  ★ $\mathrm{Re_{bed}} \lesssim 10$**

```math
\langle v \rangle = \dfrac{\kappa}{\mu} \left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right]
```

**Volumetric flow rate**

```math
Q = \langle v \rangle \varepsilon A = v_0 A
```

**Superficial velocity**

```math
v_0 = \langle v \rangle \varepsilon
```

**Bed Reynolds number**

```math
\begin{aligned}\mathrm{Re_{bed}} &= \dfrac{D_p v_0 \rho}{\mu}\dfrac{1}{1 - \varepsilon} \\ &= \dfrac{D_p \langle v \rangle \rho}{\mu}\dfrac{\varepsilon}{1 - \varepsilon} \\ &= \dfrac{D_p Q \rho}{\mu A}\dfrac{1}{1 - \varepsilon}\end{aligned}
```

**Tube Reynolds number**

```math
\mathrm{Re_{tube}} = \dfrac{2}{3}\mathrm{Re_{bed}}
```

**Hydrolic radius**

```math
R_H = \dfrac{D_p\varepsilon}{6(1-\varepsilon)}
```

**Friction factor of tube  ★ $\mathrm{Re_{bed}} \le 10$**

```math
f_{\text{tube}} = \dfrac{24(1-\varepsilon)\mu}{D_p v_0 \rho}
```

**Friction factor of tube  ★ $\mathrm{Re_{bed}} > 1000$**

```math
f_{\text{tube}} = \dfrac{7}{12}
```

**Bed permeability**

```math
\kappa = \dfrac{D_p^2}{150} \left(\dfrac{\varepsilon}{1-\varepsilon}\right)^2
```

**Blake-Kozeny equation  ★ $\mathrm{Re_{bed}} \le 10$**

```math
\left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right] = 150 \dfrac{\mu v_0}{D_p^2}\dfrac{(1-\varepsilon)^2}{\varepsilon^3}
```

**Burke-Plummer equation  ★ $\mathrm{Re_{bed}} > 1000$**

```math
\left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right] = \dfrac{7}{4}\dfrac{\rho v_0^2}{D_p}\dfrac{1-\varepsilon}{\varepsilon^2}
```

**Superficial mass flux**

```math
G_0 = \rho v_0 = \dfrac{\dot{m}}{A}
```

**Ergun equation  ★ $\mathrm{Re_{bed}} \in [10, 1000]$**

```math
\begin{gathered}
\left[ \dfrac{(\mathcal{P}_0 - \mathcal{P}_L)\rho}{G_0^2} \right] \dfrac{D_p}{L}\dfrac{\varepsilon^3}{1-\varepsilon} = 150 \left[ \dfrac{1-\varepsilon}{\frac{D_p G_0}{\mu}} \right] + \dfrac{7}{4} \\
\left[ \dfrac{(\mathcal{P}_0 - \mathcal{P}_L)\rho}{G_0^2} \right] \dfrac{D_p}{L}\dfrac{\varepsilon^3}{1-\varepsilon} = 150 \dfrac{1}{\mathrm{Re_{bed}}} + \dfrac{7}{4}
\end{gathered}
```

## Cavitation and vortex motion

**Cavitation number**

```math
\sigma = \dfrac{p_A - p_C}{\frac{1}{2}\rho v_\infty^2}
```

## Forced vortex flow in rotating cylinder

**Velocity profile**

```math
v_\theta = r\Omega
```

**Pressure difference  ★ 1 defined arbitrarily, 2 defined at center**

```math
p_2 - p_1 = \dfrac{1}{2}\rho\Omega^2 (r_2^2 - r_1^2) + \rho g (z_1 - z_2)
```

**Height**

```math
h = \dfrac{\Omega^2}{2g} r^2
```

## Free vortex flow during drainage

**Pressure difference   ★ 1 defined arbitrarily, 2 defined at $r \to\infty$**

```math
p_2 - p_1 = \dfrac{1}{2}\rho C^2 \left(\dfrac{1}{r_1^2} - \dfrac{1}{r_2^2}\right) + \rho g (z_1 - z_2)
```

**Depth**

```math
h = \dfrac{C^2}{2g} \dfrac{1}{r^2}
```

## Microfluidics*

*Context:* Validity of continuum description

**Mean free path**

```math
\begin{gathered}
\lambda = \dfrac{1}{\sqrt{2}\pi d^2 n} \\
\lambda(\mathrm{\mu m}) \approx 3.1\times 10^{-3} \dfrac{T(\mathrm{K})}{\sigma^2(\mathrm{\mathring{A}^2}) p(\mathrm{atm})}
\end{gathered}
```

**Knudsen number**

```math
\mathrm{Kn} = \dfrac{\lambda}{L_c}
```

- **Characteristics** — Range

**Molecular flow**

```math
\mathrm{Kn} \in (10, \infty)
```

**Transition flow**

```math
\mathrm{Kn} \in (0.1, 10)
```

**N-S equations hold, but no-slip condition fails**

```math
\mathrm{Kn} \in (0.001, 0.1)
```

**N-S equations hold, and no-slip condition holds**

```math
\mathrm{Kn} \in (0, 0.001)
```

Forces in microfluidic flows Viscous force dominate over inertial forces and gravity forces Driving force Pressure Capillary (surface tension) forces Electro-kinetic forces Magnetic forces

## Resisting forces: viscous force, dominated by wall effects

**Reynolds number  ★ Creeping flow**

```math
\mathrm{Re} = \dfrac{\text{inertial forces}}{\text{viscous forces}} = \dfrac{Lv\rho}{\mu} \to 0
```

**Froude number**

```math
\mathrm{Fr} = \dfrac{\text{inertial forces}}{\text{gravity forces}} = \dfrac{v^2}{gL}
```

**Viscous force dominates gravity force**

```math
\mathrm{\dfrac{Re}{Fr}} = \dfrac{\text{gravity forces}}{\text{viscous forces}} = \dfrac{gL^2}{\mu v} \to 0
```

## Generalized Hagen-Poiseuille flow

**Differential equation of generalized H-P flow**

```math
0 = \dfrac{\Delta p}{L} + \mu \left(\dfrac{\partial^2 v_z}{\partial x^2} + \dfrac{\partial^2 v_z}{\partial y^2}\right)
```

**No-slip condition  $F(x, y)$ is equation of conduit perimeter**

```math
v_z(x, y) = 0 for F(x, y) = 0
```

**Velocity profile**

```math
v_z(x, y) = \dfrac{\Delta p}{\mu L} F(x, y)
```

**Volumetric flow rate**

```math
Q = \dfrac{\Delta p}{\mu L} \displaystyle\iint F(x, y) \ dy\ dx
```

## Hydraulic resistance in micro-channels

**Flow equation**

```math
\Delta p = \mathcal{R}_{\text{hyd}}Q
```

**Volumetric flow rate**

```math
Q = \dfrac{\Delta p}{\mathcal{R}_{\text{hyd}}}
```

## Capillary driving force and wicking phenomena

**Pressure difference**

```math
\Delta p = \sigma\kappa = \dfrac{2\sigma}{R}
```

**Wicking velocity**

```math
v = \dfrac{r^2}{8\mu}\dfrac{\Delta P}{x} = \dfrac{r\sigma \cos\theta}{4\mu x}
```

**Washburn equation**

```math
x = \sqrt{\dfrac{r\sigma\cos\theta}{2\mu} t} \propto \sqrt{t}
```

**Wicking into porous media**

```math
h = \sqrt{\dfrac{r_e\sigma\cos\theta}{2\mu} t} \propto \sqrt{t}
```

# Separation Processes

## Separation Processes

*Context:* Types of Separations; Separations by phase creation

- **Partial condensation/vaporization** — V and/or L; L or V; Heat transfer (ESA)

- **Flash vaporization** — L; V; Pressure reduction

- **Distillation** — V and/or L; V and L; Heat transfer (ESA) and sometimes shaft work (ESA)

## Separations by phase addition

- **Absorption** — V; L; Liquid absorbent (MSA)

- **Stripping** — L; V; Stripping vapor (MSA)

- **Liquid-liquid extraction** — L; L; Liquid solvent (MSA)

- **Adsorption** — V or L; S; Solid adsorbent (MSA)

## Separations by barrier

- **Dialysis** — L; Microporous membrane; Pressure (ESA)

- **Reverse osmosis** — L; Microporous membrane; Pressure (ESA)

- **Gas permeation** — Vapor; Nonporous membrane; Pressure (ESA)

- **Pervaporation** — L; Nonporous membrane; Pressure and heat transfer (ESA)

## Separations by external field/gradient

*Context:* Centrifugation - pressure gradient; Thermal diffusion - temperature gradient; Electrolysis; Electrodialysis - permeable membrane with fixed charge; Electrophoresis - electric field; Magnetophoresis - magnetic field; Crystallization - solubility; Thermodynamics Review

**Equilibrium conditions**

```math
\begin{aligned}T_1 &= T_2 \\ P_1 &= P_2 \\ \bar{f}_2 &= \bar{f}_2 \\ a_1 &= a_2\end{aligned}
```

**Fugacity**

```math
\bar{f}_i = \bar{f}_i^\circ \exp\left(\dfrac{\mu_i}{RT}\right)
```

**Fugacity coefficient**

```math
\phi_i = \dfrac{f_i}{P}
```

**Partial fugacity coefficient**

```math
\phi_i = \dfrac{f_i}{x_iP}
```

**Activity**

```math
a_i = \dfrac{\bar{f}_i}{f_i^\circ}
```

**Activity coefficient**

```math
\gamma_i = \dfrac{a_i}{x_i}
```

## $K$-values

**$K$-value (vapor-liquid equilibrium ratio)**

```math
K_i = \dfrac{y_i}{x_i}
```

**Distribution ratio (partition coefficient, liquid-liquid equilibrium ratio**

```math
K_{D_i} = \dfrac{x_i^\alpha}{x_i^\beta}
```

**Relative volatility**

```math
\alpha_{i, j} = \dfrac{K_i}{K_j}
```

**Relative selectivity**

```math
\beta{i, j} = \dfrac{K_{D_i}}{K_{D_j}}
```

**Raoult’s law  ★ Ideal solution**

```math
K_i = \dfrac{P_i^*}{P}
```

**Modified Raoult’s law  ★ Low pressure**

```math
K_i = \gamma_{i, L}\dfrac{P_i^*}{P}
```

**Poynting correction  ★ Moderate pressure**

```math
K_i = \gamma_{i, L}\phi_{i, V}^\mathrm{sat}\left(\dfrac{P_i^\mathrm{sat}}{P}\right) \exp\left[\dfrac{1}{RT}\displaystyle\int^P_{P_i^{\mathrm{sat}}} v_{i, L} dP \right]
```

**Henry’s law  ★ Dilute species**

```math
K_i = \dfrac{H_i}{P}
```

## Mass Transfer and Diffusion

*Context:* Steady-state ordinary molecular diffusion (OMD)

**Fick’s first law  Molecular diffusion flux of species A**

```math
\begin{gathered}
\begin{aligned} J_{A} &= -cD_{AB}\dfrac{dx_A}{dx} \\ &= -D_{AB} \dfrac{dc_A}{dz} \end{aligned} \\
j_{A} = -\rho D_{AB}\dfrac{dw_A}{dz}
\end{gathered}
```

**Bulk flow flux**

```math
N = N_A + N_B
```

**Bulk flow flux of species A**

```math
x_A N
```

**Molar flux of species A (definition)**

```math
N_A = \dfrac{\dot{n}_A}{A}
```

**Molar flux of species A  ★ No eddie diffusion flux**

```math
\begin{aligned} N_A &= \text{bulk flow flux} + \text{molecular diffusion flux}\\ N_A &= x_A N - cD_{AB} \dfrac{dx_A}{dz} \end{aligned}
```

**Total velocity of species A**

```math
v_A = \dfrac{N_A}{c_A}
```

**Molar-average mixture velocity**

```math
v_M = v_Ax_A + v_Bx_B
```

**Diffusion velocity of species A**

```math
v_{D, A} = \dfrac{J_A}{c_A}
```

**Velocity relations**

```math
v_A = v_M + v_{D, A}
```

## Equimolar counter diffusion (EMD)

**Equimolar counter diffusion**

```math
N_A = - N_B
```

**No bulk flow**

```math
N = 0
```

**Molar flux of species A  Molecular diffusion flux of species A**

```math
N_A = J_A = -cD_{AB} \dfrac{\Delta x_A}{\Delta z}
```

**Concentration profile of species A**

```math
c_A = c_{A0} - \dfrac{J_A z}{D_{AB}}
```

**Concentration profile of species B**

```math
c_B = c_{B0} + \dfrac{J_A (z-L)}{D_{AB}}
```

## Unimolecular diffusion (UMD)

**Stagnant B**

```math
N_B = 0
```

**Molar flux of species A  Bulk flow flux**

```math
N = N_A
```

**Molar flux of species A**

```math
N_A = \dfrac{cD_{AB}}{z - z_1} \ln\left(\dfrac{1 - x_A}{1 - x_{A, 1}}\right)
```

**Molar flux of species A**

```math
N_A = -\dfrac{cD_{AB}}{(1 - x_A)_{\mathrm{LM}}} \dfrac{\Delta x_A}{\Delta z}
```

**Dilute A reduces UMD to EMD (no bulk flow)**

```math
(1 - x_A)_{\mathrm{LM}} \approx 1 \quad \text{if } x_A \to 0
```

**Log-mean**

```math
x_{\mathrm{LM}} = \dfrac{x_2 - x_1}{\ln(x_2/x_1)}
```

**Composition profile**

```math
x_A(z) = 1 - (1 - x_A) \exp\left[\dfrac{N_A (z - z_1)}{cD_{AB}}\right]
```

**Molecular diffusion and bulk flow flux of species**

```math
J_A = x_B N = - J_B
```

**Changing liquid level of A with stagnant B**

```math
N_A = -\dfrac{cD_{AB}}{(1 - x_A)_{\mathrm{LM}}} \dfrac{\Delta x_A}{z} = \dfrac{\rho_A}{\mathcal{M}_A}\dfrac{dz}{dt}
```

---

## Diffusivity of gas mixtures

**Fuller-Schettler-Giddings correlation  * Low pressure (0 - 10 atm) *  $D_{AB} \ [\mathrm{cm^2/s}]$ *  $P \ [\mathrm{atm}], T \ [\mathrm{K}]$  * $\mathcal{M}_{AB} \ [\mathrm{g/mol}]$**

```math
D_{AB} = D_{BA} = \dfrac{0.00143 T^{1.75}}{P \mathcal{M}_{AB}^{1/2} \left[(\sum_V)_A^{1/3} + (\sum_V)_B^{1/3}\right]^2}
```

**Effective molecular mass**

```math
\mathcal{M}_{AB} = \dfrac{2}{\dfrac{1}{\mathcal{M}_A} + \dfrac{1}{\mathcal{M}_B}}
```

**Summation of atomic and structural diffusion volumes (Table 3.1)**

```math
\sum_V
```

**Takahashi correlation  * High pressure (Figure 3.3)**

```math
\dfrac{D_{AB} P}{(D_{AB}P)_{\text{low }P}} = \mathrm{const}
```

**Molar averaged reduced properties**

```math
\begin{gathered}
T_r = x_A T_{r, A} + x_B T_{r, B} \\
P_r = x_A P_{r, A} + x_B P_{r, B}
\end{gathered}
```

## Diffusivity of nonelectrolyte liquid mixtures

**Stokes-Einstein equation  * Infinite dilution**

```math
(D_{AB})_\infty = \dfrac{RT}{6\pi \mu_B R_A N_A} \propto \dfrac{T}{\mu_B R_A}
```

**Wilke-Chang equation  * Low pressure (0 - 10 atm)  * $D_{AB} \ [\mathrm{cm^2/s}]$  * $\mu_B \ [\mathrm{cP}], T \ [\mathrm{K}]$  * $\mathcal{M}_{AB} \ [\mathrm{g/mol}]$  * $v_A \ [\mathrm{cm^3/mol}]$**

```math
(D_{AB})_\infty = 7.4\times 10^{-8} \dfrac{(\phi_B \mathcal{M}_B)^{1/2}T}{\mu_B v_A^{0.6}}
```

**Hayduk-Minhas correlation  (Modified Wilke-Chang equation)**

```math
\begin{gathered}
(D_{AB})_\infty = 13.3\times 10^{-8} \dfrac{T^{1.47}\mu_B^\varepsilon}{v_A^{0.71}} \\
\varepsilon = \dfrac{10.2}{v_A} - 0.791
\end{gathered}
```

## Film theory for mass transfer at fluid-fluid interface

*Context:* Single film theory

**Concentration and mole fraction**

```math
c_A = x_Ac
```

**Mass transfer coefficient (no bulk flow)**

```math
k_c = \dfrac{D_{AB}}{\delta}
```

**Mass transfer coefficient (with bulk flow)**

```math
k'_c = \dfrac{D_{AB}}{\delta (1 - x_A)_{\mathrm{LM}}}
```

**Molar flux of species A — interface (i), bulk (b)**

```math
\begin{gathered}
N_A = \pm k_c (c_{A, i} - c_{A, b}) \\
N_A = \pm k'_c (c_{A, i} - c_{A, b})
\end{gathered}
```

**Film thickness**

```math
\delta = \dfrac{D_{AB}}{k_c} = \dfrac{D_{AB}}{k'_c (1 - x_A)_{\mathrm{LM}}}
```

### Mass-transfer coefficients and driving forces

**Concentration (liquid)**

```math
k_c \ [\mathrm{m/s}]\qquad N_A = \pm k_c (c_{A, i} - c_{A, b})
```

**Pressure (vapor)**

```math
k_p \ [\mathrm{mol/m^2 \cdot s \cdot Pa}]\qquad N_A = \pm k_p (P_{A, i} - P_{A, b})
```

**Mole fraction (liquid)**

```math
k_x \ [\mathrm{mol/m^2 \cdot s}]\qquad N_A = \pm k_x (x_{A, i} - x_{A, b})
```

### Mole fraction (vapor)

*Context:* $k_y \ [\mathrm{mol/m^2 \cdot s}]$; $N_A = \pm k_y (y_{A, i} - y_{A, b})$

**Liquid phase coefficient conversion**

```math
k_x = k_c c = k_c \dfrac{\rho_L}{\mathcal{M}_L}
```

**Vapor phase coefficient conversion**

```math
k_y = k_p P = (k_c)_g c = (k_c)_g \dfrac{P}{RT} = (k_c)_g \dfrac{\rho_G}{\mathcal{M}_G}
```

**Liquid phase bulk flow correction**

```math
k' = \dfrac{k}{(1 - x_A)_{\mathrm{LM}}}
```

**Gas phase bulk flow correction**

```math
k' = \dfrac{k}{(1 - y_A)_{\mathrm{LM}}}
```

### Two-film theory

- **Based on** — Overall Mass Transfer Coefficient; Equations; Fictitious properties

**Liquid phase**

```math
\dfrac{1}{K_L} = \dfrac{H_A}{k_p} + \dfrac{1}{k_c}\qquad N_A = \pm K_L (c_A^* - c_{A, b})\qquad c_A^* = P_{A, b} H_A
```

**Gas phase**

```math
\dfrac{1}{K_G} = \dfrac{1}{k_p} + \dfrac{1}{H_A k_c}\qquad N_A = \pm K_G (P_{A, b} - P_A^*)\qquad P_A^* = \dfrac{c_{A, b}}{H_A}
```

**Liquid phase mole fraction**

```math
\dfrac{1}{K_x} = \dfrac{1}{K_a k_y} + \dfrac{1}{k_x}\qquad N_A = \pm K_y (y_{A, b} - y_{A}^*)\qquad y_A^* = x_{A, b}K_A
```

**Gas phase mole fraction**

```math
\dfrac{1}{K_y} = \dfrac{1}{k_y} + \dfrac{K_A}{k_x}\qquad N_A = \pm K_x (x_{A}^* - x_{A, b})\qquad x_A^* = \dfrac{y_{A, b}}{K_A}
```

## Single Equilibrium Stages

*Context:* Degrees of freedom

**Gibbs' phase rule**

```math
\mathrm{DOF = component - phase + 2}
```

**Degree of freedom**

```math
\text{DOF = \# intensive variables} - \text{\# independent eqns}
```

**Azeotrope**

```math
x_i = y_i
```

**$q$-line**

```math
y_H = \left[\dfrac{(V/F) - 1}{(V/F)}\right] x_H + \left[\dfrac{1}{(V/F)}\right] z_H
```

### Rachford–Rice algorithm for isothermal flash calculation

**Symbol conventions**

- **Molar flow rates**  
  $F$ - Feed  $V$ - Output vapor  $L$ - Output liquid

### Mole fractions of component i

*Context:* $x_i$ - In the liquid; $y_i$ - In the vapor; $z_i$ - Overall

- **Road map**  
  Known -  $K_i, z_i, F$  Solve - $\Psi \to V \to L \to x_i, y_i \to Q$

**Vapor-to feed ratio**

```math
\Psi \equiv \dfrac{V}{F}
```

**Objective function  ★ Derived from $\sum y_i - \sum x_i = 0$**

```math
f(\Psi) = \displaystyle\sum_i \dfrac{z_i (1 - K_i)}{[1 + \Psi(K_i - 1)]} = 0
```

**Derivative of objective function**

```math
f'(\Psi) = \displaystyle\sum_i \dfrac{z_i (K_i - 1)^2}{[1 + \Psi(K_i - 1)]^2}
```

**Newton’s method for root finding**

```math
\Psi_{n+1} = \Psi_n - \dfrac{f(\Psi_n)}{f'(\Psi_n)}
```

**Vapor molar flow rate**

```math
V = \Psi F
```

**Liquid molar flow rate**

```math
L = F - V
```

**Liquid mole fraction**

```math
x_i = \dfrac{z_i}{1 + \Psi(K_i - 1)}
```

**Vapor mole fraction**

```math
y_i = \dfrac{z_i K_i}{1 + \Psi(K_i - 1)}
```

**Heat**

```math
Q = h_V V + h_L L - h_F F
```

## Bubble and dew point calculations

*Context:* Flash operations of flash vaporization and partial condensation. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p93, Figures 4.8, 4.9.)

**Bubble point (ideal mixture, Raoult’s law)**

```math
\begin{gathered}
\Psi = 0 \\
\sum z_i K_i = 1 \\
\sum_i x_i P_i^*(T) = P
\end{gathered}
```

**Dew point (ideal mixture, Raoult’s law)**

```math
\begin{gathered}
\Psi = 1 \\
\sum \dfrac{z_i}{K_i} = 1 \\
\sum_i \dfrac{y_i}{P_i^*(T)} = \dfrac{1}{P}
\end{gathered}
```

## Ternary liquid–liquid extraction

**Symbol conventions**

- **Components**  
  $A$ - Carrier (feed solvent)  $B$ - Solute  $C$ - Solvent

- **Mass flow rates**  
  $F$ - Feed  $S$ - Solvent  $E$ - Extract (Majority of solvent $C$ carrier extracted solute $B$)  $R$ - Raffinate

- **Mass fraction of component i**  
  $x_i$ - In the liquid  $y_i$ - In the vapor  $z_i$ - Overall

### Mass ratio of component i

*Context:* $X_i$ - In the liquid; $Y_i$ - In the vapor

**Mass fraction**

```math
x_i = \dfrac{m_i}{m}
```

**Mass ratio**

```math
X_i = \dfrac{m_i}{m - m_i}
```

**Conversion between mass fraction and ratio**

```math
\begin{gathered}
X_i = \dfrac{x_i}{1 - x_i} \\
x_i = \dfrac{X_i}{1 + X_i}
\end{gathered}
```

**Solute balance  ★ Solvent A, Solute B  ★ Feed F, Solvent S, Extract E, Raffinate R**

```math
\begin{aligned} F_B &= E_B + R_B & \\ X_{F, B} F_A &= Y_{E, B} S + X_{R, B}F_A & Y_{E, B} = K'_{D_B} X_{R, B} \\ X_{F, B}F_A &= K'_{D_B} X_{R, B}S + X_{R, B}F_A & \\ X_{R, B} &= \dfrac{X_{F, B} F_A}{F_A + K'_{D_B} S} \end{aligned}
```

**Extraction factor of solute B**

```math
\mathcal{E} = \dfrac{K'_{D_B} S}{F_A}
```

**Fraction of solute B unextracted**

```math
\dfrac{X_{R, B}}{X_{F, B}} = \dfrac{1}{1 + \mathcal{E}}
```

Liquid-liquid extraction of ternary mixture. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p98, Figure 4.12.) Ternary phase diagram General principles are the same for different types of ternary phase diagrams. Here, algorithm for using equilateral ternary phase diagrams is presented. Identify chemical species at the apexes: feed solvent (A), feed solute (B), and pure solvent (S) Apexes are pure components Lines parallel to the apex are used to read values Label each side of the triangle according to the apex

- **Identify compositions of entering streams: feed (F) and solvent (S)**  
  Assume feed only contains A and B, and solvent is pure S  Calculate composition of mixture (M) with component balances  $x_{M, A} = \dfrac{x_{F, A} F}{F + S}, \quad x_{M, B} = \dfrac{x_{F, B} F}{F + S}, \quad x_{M, C} = \dfrac{S}{F + S}$

- **Interpolate tie line on the ternary phase diagram** — Identify compositions of exiting streams: extract (E) and raffinate (R); E and R lies on the intersection of tie line and miscibility boundary (binodal) curve; E has a larger S component than R (extracted component is dissolved in solvent), being closer to point S

- **Identify plait point (P)** — P lies between E and R on the miscibility boundary curve; P the the point where E and R merge together and tie line collapses to a point

**Determine flow rate ratio with inverse level rule**

```math
\dfrac{E}{F + S} = \dfrac{E}{E + R} = \dfrac{\overline{MR}}{\overline{ER}}, \quad \dfrac{E}{R} = \dfrac{\overline{MR}}{\overline{ME}}
```

- **Sample equilateral ternary phase diagram. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p101, Figure 4.14.)** — Multistage Cascades

**Single stage**

```math
\dfrac{X_{R, B}}{X_{F, B}} = \dfrac{1}{1 + \mathcal{E}}
```

**Cocurrent cascade ($N$ stages)**

```math
\dfrac{X_{N, B}}{X_{F, B}} = \dfrac{1}{1 + \mathcal{E}}
```

**Crosscurrent cascade ($N$ stages)**

```math
\dfrac{X_{N, B}}{X_{F, B}} = \dfrac{1}{(1 + \mathcal{E}/N)^N}
```

**Crosscurrent cascade ($\infty$ stages)**

```math
\dfrac{X_{\infty, B}}{X_{F, B}} = \dfrac{1}{\exp(\mathcal{E})}
```

**Countercurrent cascade ($N$ stages)**

```math
\dfrac{X_{R, B}}{X_{F, B}} = \left[\displaystyle\sum_{n = 0}^N \mathcal{E}^n\right]^{-1} = \dfrac{\mathcal{E} - 1}{\mathcal{E}^{N+1} - 1}
```

**Countercurrent cascade ($\infty$ stages)**

```math
\begin{cases} \dfrac{X_{\infty, B}}{X_{F, B}} = 0, & \mathcal{E} \in [1, \infty) \\ \dfrac{X_{\infty, B}}{X_{F, B}} = 1 - \mathcal{E}, & \mathcal{E} \in (-\infty, 1) \end{cases}
```

## Absorption and stripping — graphical design

Multistage arrangements: cocurrent, crosscurrent and countercurrent (Seader, 4th ed., Fig. 5.4).

**Symbol conventions**

- **Molar flow rates**  
  $L$ - Total liquid feed  $V$ - Total gas feed  $L'$ - solute-free absorbent - constant at each stage  $V'$ - solute-free gas (carrier gas) - constant at each stage

- **Mole ratio of solute to solute-free absorbent**  
  $X$ - In the liquid  $Y$ - In the vapor

Equilibrium curve and operating lines of absorber and stripper. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p144, 146, Figures 6.9, 6.12.)

**Construct the equilibrium curve from thermodynamics**

```math
K_n = \dfrac{y_n}{x_n} = \dfrac{Y_n}{X_n}\dfrac{1 + X_n}{1 + Y_n} \implies Y_n = \dfrac{K_n X_n}{1 + X_n - K_n X_n}
```

- **Identify absorption and stripping process** — Absorption - Use liquid to remove components from gas mixture; Stripping - Use gas to remove components from liquid mixture

- **Construct operating line for $\infty$ stages for $L'_{\min}$ or $V'_{\min}$**  
  Absorption ($L'_{\min}$)  Identify (liquid in, gas out) = $(X_0, Y_1)$  Identify (liquid out, gas in) = $(X_N, Y_{N+1})$ with minimum operating line intersects and ends at the equilibrium curve

- **Stripping ($V'_{\min}$)**  
  Identify (gas in, liquid out) = $(X_1, Y_0)$  Identify (liquid out, gas in) = $(X_{N+1}, Y_N)$ with minimum  operating line intersects and ends at the equilibrium curve

Slope of operating line = $\dfrac{L'}{V'}$

- **Determine number of equilibrium stages for $L'$ and $V'$**  
  Absorption ($L'$)  Construct operating line with point (liquid in, gas out) = $(X_0, Y_1)$ and slope = $\dfrac{L'}{V'}$  From $(X_0, Y_1)$, draw horizontal line toward the equilibrium curve and vertical lines back to the operating line until it reaches $(X_N, Y_{N+1})$

- **Stripping ($V'$)**  
  Construct operating line with point (gas in, liquid out) = $(X_1, Y_0)$ and slope = $\dfrac{L'}{V'}$  From $(X_1, Y_0)$, draw horizontal line toward the equilibrium curve and vertical lines back to the operating line until it reaches $(X_{N+1}, Y_N)$

- **The number of equilibrium stages is the number of intersections on the equilibrium curve** — Interpolate number of stages if not exact

## Absorption

**Absorption operating line**

```math
Y_{n+1} = X_n \dfrac{L'}{V'} + Y_1 - X_0 \dfrac{L'}{V'}
```

**Absorbent flow rate**

```math
L' = V' \dfrac{Y_{N+1} - Y_1}{X_N - X_0}
```

**Minimum absorbent flow rate ($\infty$ stages)**

```math
L'_{\min} = V' K_N \cdot (\text{fraction solute absorbed})
```

**Absorption factor**

```math
\mathcal{A} = \dfrac{L}{K V}
```

## Stripping

**Stripping operating line**

```math
Y_{n} = X_n \dfrac{L'}{V'} + Y_0 - X_1 \dfrac{L'}{V'}
```

**Stripping agent flow rate**

```math
V' = L'\dfrac{X_{N} - X_1}{Y_N - Y_0}
```

**Minimum stripping agent flow rate ($\infty$ stages)**

```math
V'_{\min} = \dfrac{L'}{K_N} \cdot (\text{fraction solute stripped})
```

**Stripping factor**

```math
\mathcal{S} = \dfrac{V}{L}K
```

**Relating stripping factor and adsorption factor**

```math
\mathcal{S} = \dfrac{1}{\mathcal{A}}
```

## Stage efficiency and packed columns

**Overall stage efficiency**

```math
E_o = \dfrac{\text{\# theoretical stages}}{\text{\# actual stages}}
```

**Drickamer and Bradford correlation  ★ Hydrocarbons, $\mu_L \in (0.2, 1.6) \ \mathrm{cP}$**

```math
E_o [\%] = 19.2 - 57.8 \log(\mu_L)
```

**Height equivalent to a theoretical plate (HETP)**

```math
\mathrm{HETP} = \dfrac{l_T}{N_t} = \dfrac{\text{packed height}}{\text{\# equiv eqm stages}}
```

**Packed height**

```math
l_T = H_{OG}N_{OG}
```

**Overall height of a transfer unit (HTU)**

```math
H_{OG} = \dfrac{V}{K_y a A_c}
```

**Overall number of transfer unit (NTU)**

```math
N_{OG} = \displaystyle\int_{y_{\text{out}}}^{y_{\text{in}}}\dfrac{dy}{y - y^*}
```

**Overall volumetric mass transfer coefficient**

```math
K_y a
```

## Distillation of binary mixtures

McCabe–Thiele graphical method for trayed towers.

**Symbol conventions**

- **Molar flow rates**  
  $F$ - Feed  $D$ - Distillate  $B$ - Bottoms  $L$ - Liquid in the rectifying section, Reflux  $V$ - Vapor in the rectifying section  $\overline{L}$ - Liquid in the stripping section  $\overline{V}$ - Vapor in the stripping section, Boilup

- **Mole fraction of the light key component**  
  $x$ - In the liquid  $y$ - In the vapor  $x_D$ - In the distillate  $x_B$ - In the bottoms

### Ratios and assumptions

*Context:* $\alpha_{1, 2}$ - Relative volatility; $R$ - Reflux ratio; $V_B$ - Boilup ratio

- **McCabe-Thiele assumptions**  
  1. Equal and constant $\Delta H_{\text{vap}}$  2. Negligible $C_P \Delta T$ and $\Delta H_{\text{mix}}$  3. Insulated column $q = 0$  4. No pressure drop $\Delta P = 0$

**Constant molar overflow in rectifying section**

```math
\begin{gathered}
L_1 = L_i = L \\
V_1 = V_i = V
\end{gathered}
```

**Constant molar overflow in stripping section**

```math
\begin{gathered}
\overline{L}_1 = \overline{L}_i = \overline{L} \\
\overline{V}_1 = \overline{V}_i = \overline{V}
\end{gathered}
```

**Non-equal flow rate in rectifying and stripping sections**

```math
\begin{gathered}
L \neq \overline{L} \\
V \neq \overline{V}
\end{gathered}
```

**Reflux ratio**

```math
R = \dfrac{L}{D}
```

**Boilup ratio**

```math
V_B = \dfrac{\overline{V}}{B}
```

**Equilibrium curve**

```math
y_1 = \dfrac{\alpha_{1, 2}x_1}{1 + x_1(\alpha_{1, 2} - 1)}
```

**Rectifying section operating line**

```math
y = \left(\dfrac{R}{R + 1}\right)x + \left(\dfrac{x_D}{R + 1}\right)
```

**Stripping section operating line**

```math
y = \left(\dfrac{V_B + 1}{V_B}\right)x - \left(\dfrac{x_B}{V_B}\right)
```

**$q$-parameter**

```math
\begin{cases} q > 1 & \text{subcooled liq} \\ q = 1 & \text{saturated liq (bubble pt)} \\ q \in (0, 1) & \text{liq + vap} \\ q = 0 & \text{saturated vap (dew pt)} \\ q < 0 & \text{superheated vap} \end{cases}
```

**$q$-parameter**

```math
q = \dfrac{\overline{L} - L}{F} = 1 + \dfrac{\overline{V} - V}{F}
```

**$q$-line**

```math
y = \left(\dfrac{q}{q - 1}\right)x - \left(\dfrac{z_F}{q - 1}\right)
```

## Limiting conditions

**Total reflux — theoretical limiting case**

```math
\begin{gathered}
R_\infty = \infty \\
N_{\min} = \text{finite minimum theoretical stage count} \\
L = V \\
D = B = 0
\end{gathered}
```

**Minimum reflux**

```math
\begin{gathered}
R_{\min} = \dfrac{(L/V)_{\min}}{1 - (L/V)_{\min}} \\
N_\infty = \infty \\
V_{B, \min} = \dfrac{1}{(\overline{L}/\overline{V})_{\min} - 1}
\end{gathered}
```

**Perfect separation**

```math
\begin{gathered}
x_D = 1, \quad x_B = 0 \\
R \ge R_{\min}  \begin{cases} R_{\min} = \dfrac{1}{z_F (\alpha_{1, 2} - 1)} & q = 1 \\ R_{\min} = \dfrac{\alpha_{1, 2}}{z_F (\alpha_{1, 2} - 1)} - 1 & q = 0 \end{cases}
\end{gathered}
```

## Membrane Separations

*Context:* Equilibrium curve and operating lines of rectifying and stripping sections of distillation column. Optimal feed stage is indicated by the transition between operating lines on the equilibrium curve. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p195, 196, 197, 200, Figures 7.5, 7.6, 7.7, 7.10.)

**Transmembrane molar flux**

```math
\begin{aligned}N_i &= \dfrac{P_{M, i}}{l_M} \cdot (\text{driving force}) \\ &= \bar{P}_{M, i} \cdot (\text{driving force}) \end{aligned}
```

**Permeance**

```math
\bar{P}_{M, i} = \dfrac{P_{M, i}}{l_M}
```

**Permeability**

```math
P_{M, i} = \bar{P}_{M, i} l_M
```

**Selectivity**

```math
S_{i, j} = \dfrac{P_{M, i}}{P_{M, j}}
```

**Gas permeability unit**

```math
\begin{aligned}&1 \ \mathrm{barrer} \\ &= 10^{-10} \ \mathrm{cm^3_{STP} \cdot cm/(cm^2 \cdot s \cdot cmHg)} \\ &= 3.35 \times 10^{-16} \ \mathrm{mol \cdot m / (m^2 \cdot s \cdot Pa)} \\ &= 5.58 \times 10^{-12} \ \mathrm{lbmol \cdot ft / (ft^2 \cdot h \cdot psi)}\end{aligned}
```

**Mole of gas in standard temperature and pressure (STP)**

```math
1 \ \mathrm{mol} \sim 22.4 \ \mathrm{L_{STP}}
```

## Transport through porous membranes

*Context:* Bulk flow

**Hagen-Poiseuille flow  ★ Laminar flow $\mathrm{Re} < 2100$**

```math
v = \dfrac{D^2}{32\mu L}(P_0 - P_L)
```

**Pore number density**

```math
n = \dfrac{n_\text{total}}{A_c} = \dfrac{\text{total \# of pores}}{\text{membrane cross sectional area}}
```

**Porosity (void fraction)  ★ Straight cylindrical pore**

```math
\varepsilon = \frac{1}{4}n\pi D^2
```

**Bulk flow flux  ★ Straight cylindrical pore**

```math
\begin{aligned}N &= v\rho\varepsilon \\ &= \dfrac{\varepsilon\rho D^2}{32 \mu l_M} (P_0 - P_L) \\ &= \dfrac{n\pi\rho D^4}{128 \mu l_M}(P_0 - P_L)\end{aligned}
```

**Empirical hydraulic diameter**

```math
d_H = \dfrac{4\varepsilon}{a_v}
```

**Specific surface area**

```math
a_v = \dfrac{a}{1 - \varepsilon}
```

**Total pore surface area**

```math
a = a_v (1 - \varepsilon)
```

**Tortuosity correction of membrane width**

```math
\tau l_M
```

**Bulk flow flux  ★ General pore**

```math
N = \dfrac{\rho\varepsilon^2}{2(1-\varepsilon)^2 \tau a_v^2 \mu l_M}(P_0 - P_L)
```

**Ergun equation**

```math
\dfrac{P_0 - P_L}{l_M} = \dfrac{150 \mu v_0 (1-\varepsilon)^2}{D_P^2 \varepsilon^3} + \dfrac{1.75 \rho v_0^2 (1 - \varepsilon)}{D_P \varepsilon^3}
```

**Mean spherical particle diameter**

```math
D_P = \dfrac{6}{a_v}
```

## Liquid diffusion

**Concentration driving force**

```math
\begin{gathered}
\Delta c \neq 0 \\
\Delta P = 0
\end{gathered}
```

**Transmembrane mass flux**

```math
N_i = \dfrac{D_{e, i}}{l_M}(c_{i, 0} - c_{i, L})
```

**Effective diffusivity**

```math
D_{e, i} = \dfrac{\varepsilon D_i}{\tau} K_{r, i}
```

**Restrictive factor of solute**

```math
K_r = \left[ 1 - \dfrac{d_m}{d_p}\right]^4
```

**Selectivity**

```math
S_{i, j} = \dfrac{D_i K_{r, i}}{D_j K_{r, j}}
```

## Gas diffusion

**Transmembrane molar flux  ★ Ideal gas, uniform transmembrane T, P**

```math
\begin{aligned} N_i &= \dfrac{c_M}{P}\dfrac{D_{e, i}}{l_M}(P_{i, 0} - P_{i, L}) \\ &= \dfrac{1}{RT}\dfrac{D_{e, i}}{l_M}(P_{i, 0} - P_{i, L}) \end{aligned}
```

**Effective diffusivity**

```math
D_{e, i} = \dfrac{\varepsilon}{\tau} \left[\dfrac{1}{(1/D_i) + (1/D_{K, i})}\right]
```

**Knudsen diffusivity of straight cylindrical pore  ★ Kinetic theory of gas**

```math
D_{K, i} \ [\mathrm{cm^2/s}] = 4850 d_p \ [\mathrm{cm}] \sqrt{\dfrac{T}{\mathcal{M}_i}\dfrac{[\mathrm{K}]}{[\mathrm{g/mol}]}}
```

**Selectivity of Knudsen diffusion  ★ $D_i \gg D_{K, i}$  ★ $D_{e, i} \sim D_{K, i}$**

```math
S_{i, j} = \dfrac{P_{M, i}}{P_{M, j}} = \sqrt{\dfrac{\mathcal{M}_j}{\mathcal{M}_i}}
```

## Transport through nonporous (dense) membranes

*Context:* Solution-diffusion of liquid mixtures

**Thermodynamic equilibrium partition coefficient**

```math
K_i = \dfrac{c_i}{c_i'}
```

**Transmembrane mass flux  ★ Fick’s law**

```math
N_i = \dfrac{D_i}{l_M}(c_{i, 0} - c_{i, L})
```

**Transmembrane mass flux  ★ $K_{i, 0} = K_{i, L} = K_{i}$**

```math
N_i = \dfrac{K_i D_i}{l_M}(c'_{i, 0} - c'_{i, L})
```

**Transmembrane mass flux  ★ No mass transfer resistance in fluid boundary layers  ★ $c'_{i, 0} = c_{i, F}$ and $c'_{i, L} = c_{i, P}$**

```math
N_i = \dfrac{K_i D_i}{l_M}(c_{i, F} - c_{i, P})
```

## Solution-diffusion of gas mixtures

**Henry’s constant**

```math
H_i = \dfrac{c_i}{P_i}
```

**Transmembrane mass flux  ★ Fick’s law**

```math
N_i = \dfrac{D_i}{l_M}(c_{i, 0} - c_{i, L})
```

**Transmembrane mass flux  ★ $H_{i, 0} = H_{i, L} = H_{i}$**

```math
N_i = \dfrac{H_i D_i}{l_M}(P_{i, 0} - P_{i, L})
```

**Transmembrane mass flux  ★ No mass transfer resistance in external boundary layers  ★ $P_{i, 0} = P_{i, F}$ and $P_{i, L} = P_{i, P}$**

```math
N_i = \dfrac{H_i D_i}{l_M}(P_{i, F} - P_{i, P})
```

## Separation factor

**Ideal separation factor  ★ Downstream permeate pressure negligible compared to upstream feed pressure  ★ $x_{i, P} P_P \ll x_{i, F} P_F$ and $x_{j, P} P_P \ll x_{j, F} P_F$**

```math
\alpha^*_{i, j} = \dfrac{H_i D_i}{H_j D_j} = \dfrac{P_{M, i}}{P_{M, j}}
```

**Separation factor**

```math
\alpha_{i, j} = \alpha^*_{i, j} \left[\dfrac{(x_{j, F} / x_{j, P}) - r\alpha_{i, j}}{(x_{j, F} / x_{j, P}) - r}\right]
```

**Cut (fraction of feed permeated)**

```math
\theta = \dfrac{\dot{n}_P}{\dot{n}_F}
```

### Summary of transport through membranes

- **Type of transport** — Permselective; Membrane Type; Driving Force; Permeability

- **(L) Bulk flow**  
  No  Macroporous  $\Delta P\qquad \begin{aligned}P_M = \dfrac{\rho\varepsilon^3}{2(1 - \varepsilon)^2 \tau a_v^2 \mu}\end{aligned}$

- **(L) Molecular diffusion**  
  Yes  Microporous  $\Delta c\qquad P_M = D_{e, i} = \dfrac{\varepsilon D_i K_{r, i}}{\tau}$

- **(G) Molecular diffusion  ★ high P  ★ $d_p > d_m$**  
  Yes  Microporous  $\Delta P_i \\ \Delta P = 0\qquad P_{M, i} = \dfrac{D_{e, i}}{RT}$

- **(G) Knudsen diffusion  ★ low P  ★ $d_p \sim d_m$**  
  Yes  Microporous  $\Delta P_i \\ \Delta P = 0\qquad P_{M, i} = \dfrac{D_{e, i}}{RT}$

- **(L) Solution diffusion**  
  Yes  Nonporous (dense)  $\Delta c\qquad P_{M, i} = K_i D_i$

- **(G) Solution diffusion**  
  Yes  Nonporous (dense)  $\Delta P_i \\ \Delta P = 0\qquad P_{M, i} = H_i D_i$

## Reverse osmosis

**Osmotic pressure  ★ Equilibrium**

```math
\Pi \equiv P_1 - P_{\mathrm{H_2O}}
```

**Osmotic pressure of water**

```math
\Pi_{\mathrm{H_2O}} = 0
```

**Osmotic process**

```math
P_1 - P_{\mathrm{H_2O}} < \Pi
```

**Reverse osmotic process**

```math
P_1 - P_{\mathrm{H_2O}} > \Pi
```

**Osmotic pressure’s thermodynamic derivation  ★ Between pure water and solution  ★ Solvent $A$, solute $B$**

```math
\Pi = -\dfrac{RT}{v_{A}} \ln(x_A \gamma_A)
```

**Osmotic pressure  ★ Ideal solution, dilute $B$**

```math
\Pi = \dfrac{RT n_B}{v_A} = \dfrac{RTc_B}{\mathcal{M}_B}
```

## Seawater reverse osmosis

**Seawater as solution 1; salt as solute B**

```math
\begin{gathered}
\mathrm{A} = \text{water} = \mathrm{H_2O} \\
\mathrm{B} = \text{salt} = \mathrm{S}
\end{gathered}
```

**Molar mass**

```math
\mathcal{M} = \dfrac{m}{n}
```

**Molarity (molar concentration)**

```math
M = \dfrac{n}{V} = \dfrac{\mathrm{wt \% \ S}}{100 \% - \mathrm{wt \% \ S}}\dfrac{\rho_{\mathrm{H_2O}}}{\mathcal{M}_S}
```

**Seawater osmotic pressure correlation**

```math
\Pi \ [\mathrm{psia}] = 1.12 T \ [\mathrm{K}] \sum M_i \ [\mathrm{mol/L}]
```

**Transmembrane molar flux of water (solvent A)**

```math
N_{\mathrm{H_2O}} = \dfrac{P_{M, \mathrm{H_2O}}}{l_M} (\Delta P - \Delta \pi)
```

**Salt passage**

```math
\mathrm{SP} = \dfrac{c_{S, P}}{c_{S, F}}
```

**Salt rejection**

```math
\mathrm{SR} = 1 - \mathrm{SP}
```

**Concentration polarization factor**

```math
\Gamma \equiv \dfrac{c_{S, i} - c_{S, F}}{c_{S, F}} = \dfrac{N_{\mathrm{H_2O}} (\mathrm{SR})}{k_S}
```

**Significant concentration polarization**

```math
\Gamma > 0.2
```

