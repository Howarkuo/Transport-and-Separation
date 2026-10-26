# Transport-and-Seperation
# Chemical Engineering — Transport Phenomena, Fluid Mechanics & Separation Processes


## Contents

- [Transport Phenomena](#transport-phenomena)
- [Fluid Mechanics](#fluid-mechanics)
- [Separation Processes](#separation-processes)

---

# Transport Phenomena
Rate Laws For Diffusive Transport

## Rate Laws for Diffusive Transport

- **General form** — flux = -(coefficient)(driving force)

- **Fourier’s law  Heat conduction**  
  $q = -k\dfrac{dT}{dy}$

- **Fick’s law  Species diffusion**  
  $J_A^* = -D_{AB} \dfrac{dc_a}{dy}$

- **Newton’s law of viscosity  Momentum transfer**  
  $\tau_{yx} = -\mu \dfrac{dv_x}{dy}$

## Rate laws as concentration gradients

- **Fourier’s law**  
  $q_{y} = -\alpha \dfrac{dc_{H}}{dy}$

- **Fick’s law**  
  $J_A^* = -D_{AB} \dfrac{dc_a}{dy}$

- **Newton’s law of viscosity**  
  $\tau_{yx} = -\nu \dfrac{dc_{p_x}}{dy}$

- **Kinematic viscosity**  
  $\nu = \dfrac{\mu}{\rho}$

- **Thermal diffusivity**  
  $\alpha = \dfrac{k}{\rho \hat{c_P}}$

- **Diffusivity of A in B**  
  $D_{AB}$

- **Prandtl number**  
  $\mathrm{Pr} = \dfrac{\nu}{\alpha} = \dfrac{\hat{C}_p \mu}{k}$

- **Schmidt number**  
  $\mathrm{Sc} = \dfrac{\nu}{D_{AB}} = \dfrac{\mu}{\rho D_{AB}}$

## Heat transfer

- **Heat flow**  
  $\dot{Q} = \dfrac{Q}{t}$

- **Heat flux**  
  $q = \dfrac{\dot{Q}}{A}$

## Mass transfer

- **Mass (species) transport**  
  $N_A = x_A (\sum N_i) + J_A^*$

- **Diffusion of A through a stagnant layer of B**  
  $N_A = -\dfrac{cD_{AB}}{1 - x_A}\dfrac{dx_A}{dy}$  $N_A = -\dfrac{cD_{AB}}{L}\ln(1-x_A^s)$

- **Equimolar counter diffusion**  
  $N_A = -cD_{AB}\dfrac{dx_A}{dy}$

- **Reaction at catalytic surface  $\ce{A = 2B} \implies N_B = 2N_A$**  
  $N_A = -x_A N_A - cD_{AB}\dfrac{dx_A}{dy}$

## Momentum transfer

- **Interpretation of $\tau_{yx}$**  
  1. viscous shear stress exerted on a $y$-plane in the $+x$-direction by the fluid of lesser $y$ on that of greater $y$  2. flux of $x$-momentum across a $y$-plane in the $+y$-direction

- **Shear strain rate**  
  $\dot{\gamma} = \dfrac{dv_x}{dy}$

- **Hooke’s law  ★ Hookean solid**  
  $\tau_{yx} = -G \dfrac{dx}{dy} = -G \gamma$

- **Newton’s law of viscosity  ★ Newtonian fluid**  
  $\tau_{yx} = -\mu \dfrac{dv_x}{dy} = -\mu\dot{\gamma}$

- **General Newton’s law of viscosity**  
  $\tau_{yx} = -\eta(\dot{\gamma})\dot{\gamma}$

- **Viscosity function of power law fluid**  
  $\eta = m\dot{\gamma}^{n-1}$

- **Newton’s law of viscosity  ★ Power law fluid**  
  $\tau_{yx} = -m\dot{\gamma}^n$

- **Carreau equation  ★ Slurry**  
  $\dfrac{\eta - \eta_\infty}{\eta_o - \eta_\infty} = [1 + (\lambda\dot{\gamma})^2]^{(n-1)/2}$

## Transport Coefficients of Fluids

*Context:* Ideal gas: Simple kinetic theory

- **Average velocity**  
  $\bar{u} = \sqrt{\dfrac{8 k_B T}{\pi m}}$

- **Mean free path**  
  $\lambda = \dfrac{1}{\sqrt{2}\pi d^2 n}$

- **Number density**  
  $n = \dfrac{N}{V}$

- **Molecular flux in the y-direction**  
  $z = \frac{1}{4}n\bar{u}$

- **Average distance of molecules from ref plane when they initiate their jump**  
  $\bar{a} = \frac{2}{3}\lambda$

- **Viscosity of ideal gas**  
  $\mu = \dfrac{1}{3}\rho\bar{u}\lambda = \dfrac{2}{3\pi^{3/2}}\dfrac{\sqrt{mk_BT}}{d^2}$

- **Thermal conductivity of ideal gas**  
  $k = \dfrac{1}{3}\rho\hat{c_v}\bar{u}\lambda = \dfrac{2\hat{c_v}}{3\pi^{3/2}}\dfrac{\sqrt{mk_BT}}{d^2}$

- **Diffusivity of ideal gas A in B**  
  $D_{AB} = \dfrac{1}{3}\bar{u}_{AB}\lambda_{AB} = \dfrac{2}{\pi^{3/2}}\dfrac{\sqrt{{k_BT}^3/m_{AB}}}{d^2_{AB} P}$

- **Mean mass for diffusivity**  
  $m_{AB} = \dfrac{2m_A m_B}{m_A+m_B}$

- **Mean distance for diffusivity**  
  $d_{AB} = \frac{1}{2}(d_A + d_B)$

- **Prandtl number of monoatomic ideal gas**  
  $\mathrm{Pr}_{\text{mono}} = 1$

- **Schmidt number of general ideal gas**  
  $\mathrm{Sc} = 1$

## Real gas: Chapman-Enskog equations

*Context:* ★ Moderate pressure

- **Lenard-Jones potential**  
  $\varphi(r) = 4\varepsilon \left[\left(\dfrac{\sigma}{r}\right)^{12} - \left(\dfrac{\sigma}{r}\right)^6\right]$

- **Attractive force**  
  $F_{\text{attr}} = \dfrac{24\varepsilon}{r} \left[\left(\dfrac{\sigma}{r}\right)^{6} - 2\left(\dfrac{\sigma}{r}\right)^{12}\right]$

- **Viscosity of real gas (analytic)**  
  $\mu = \dfrac{5}{16\pi}\dfrac{\sqrt{\pi m k_BT}}{\sigma^2 \Omega_\mu}$

- **Thermal conductivity of real gas (analytic)**  
  $k = \dfrac{25}{32\pi} \dfrac{\sqrt{\pi m k_BT}}{\sigma^2 \Omega_k}\hat{c_v} = \dfrac{5}{2}\hat{c_v}\mu $

- **Viscosity of real gas**  
  $\mu\left(\mathrm{\frac{g}{cm \cdot s}}\right) = 2.6692 \times 10^{-5} \dfrac{\sqrt{\mathcal{M}T}}{\sigma^2 \Omega_\mu}$

- **Thermal conductivity of monoatomic real gas**  
  $k_{\text{mono}}\left(\mathrm{\frac{cal}{cm \cdot s \cdot K}}\right) = 1.989 \times 10^{-4} \dfrac{\sqrt{T / \mathcal{M}}}{\sigma^2 \Omega_k}$

- **Thermal conductivity of polyatomic real gas  Euken factor**  
  $k_{\text{poly}}\left(\mathrm{\frac{cal}{cm \cdot s \cdot K}}\right) = \left[ \hat{c_p} + \dfrac{5}{4}\dfrac{R}{\mathcal{M}} \right] \mu$

- **Diffusivity of real gas  $T [=] \mathrm{K} \\ P [=] \mathrm{atm} \\ \sigma_{AB} [=]$ Å**  
  $D_{AB}\left(\mathrm{\frac{cm^2}{s}}\right) = 2.63 \times 10^{-3} \dfrac{\sqrt{T^3 / \mathcal{M}_{AB}}}{P\sigma^2_{AB}\Omega_D}$

- **Mean molar mass for diffusivity**  
  $\mathcal{M}_{AB} = \dfrac{2\mathcal{M}_A \mathcal{M}_B}{\mathcal{M}_A + \mathcal{M}_B}$

- **Mean distance for diffusivity**  
  $\omega_{AB} = \frac{1}{2}(\omega_A + \omega_B)$

- **Viscosity at different temperatures**  
  $\mu(T_2) = \mu(T_1)\sqrt{\dfrac{T_2}{T_1}}\dfrac{\Omega_{\mu_1}}{\Omega_{\mu_2}}$

- **Diffusivity at different temperatures**  
  $D_{AB}(T_2) = D_{AB}(T_1)\left(\dfrac{T_2}{T_1}\right)^{3/2}\dfrac{\Omega_{D_1}}{\Omega_{D_2}}$

- **$T$ and $P$ dependence of transport coefficients of gases at moderate pressure**  
  $\begin{aligned}\mu &\propto\sqrt{T} \\ k_{\text{mono}} &\propto\sqrt{T} \\ k_{\text{poly}} &= f(T, \hat{c_p}(T)) \\ D_{AB} &\propto T^{3/2}P^{-1} \\ D_{AB} &= D_{BA}\end{aligned}$

## Ideal gas mixtures

- **Wilke equation  Viscosity of gas mixture**  
  $\mu_{\text{mix}} = \displaystyle\sum_{i=1}^{N}\dfrac{x_i \mu_i}{\sum_{j=1}^N x_j \Phi_{ij}}$

- **Wilke equation  Thermal conductivity of gas mixture**  
  $k_{\text{mix}} = \displaystyle\sum_{i=1}^{N}\dfrac{x_i k_i}{\sum_{j=1}^N x_j \Phi_{ij}}$

- **Wilke equation parameter**  
  $\Phi_{ij} = \frac{1}{\sqrt{8}} \left[ 1 + \frac{\mathcal{M}_i}{\mathcal{M}_j} \right]^{-1/2} \left[ 1 + \left[\frac{\mu_i}{\mu_j}\right]^{1/2} + \left[\frac{\mathcal{M}_i}{\mathcal{M}_j}\right]^{-1/4} \right]^2$

- **Blanc’s equation  Diffusivity of gas mixture**  
  $D_{i, \text{mix}} = \left[ \displaystyle\sum_{j \not= 1}^{N} \dfrac{x_j}{D_{ij}} \right]^{-1}$

## Liquids

- **Eyring model  Viscosity of liquid**  
  $\mu = \dfrac{N_A h}{\tilde{V}}\exp\left[ 0.408 \dfrac{\Delta U_{\text{vap}}}{RT} \right]$

- **Bridgeman equation  Thermal conductivity of liquid**  
  $k = 2.8 \left( \dfrac{N_A}{\tilde{V}}^{2/3} k_B v_s \right)$

- **Einstein equation**  
  $D_{AB} \approx \dfrac{k_BT}{f}$

- **Hydrodynamic friction factor**  
  $f = \begin{cases} 6\pi\mu_BR_A & \text{no slip} \\ 4\pi\mu_BR_A & \text{free slip} \end{cases}$

- **Stoke-Einstein Equation  Diffusivity of dilute liquid A**  
  $D_{AB} = \dfrac{k_BT}{4\pi\mu_BR_A}$

- **Wilke-Chang correlation  Diffusivity of dilute liquid A  $\tilde{V} [=] \mathrm{cm^3/mol} \\ \mu_B [=] \mathrm{cP} \\ T [=] \mathrm{K}$**  
  $D_{AB}\left(\mathrm{\frac{cm^2}{s}}\right) = 7.4 \times 10^{-8} \dfrac{(\psi_B \mathcal{M}_B)^{1/2} T}{\mu \tilde{V}_A^{0.6}}$

- **Vigne’s equation  Diffusivity of liquid mixture**  
  $D_{AB} = (D_{AB}^0)^{x_B} (D_{BA}^0)^{x_A}$

- **$T$ dependence of transport coefficients of liquids  (no $P$ dependence)**  
  $\begin{aligned} \mu &= Ae^{B/T} \\ D_{AB}\mu_B &\propto T \\ D_{AB} &\not= D_{BA} \end{aligned}$

## Shell Balance (Bottom-Up)

*Context:* Boundary conditions and shell volume

- **Rectilinear shell volume**  
  $\Delta V = LW\Delta y$

- **Cylindrical shell volume**  
  $\Delta V = 2\pi r L \Delta r$

- **Spherical shell volume**  
  $\Delta V = 4 \pi r^2 \Delta r$

- **Newton’s law of cooling**  
  $q = h(T_{\text{solid}} - T_{\text{fluid}})$

- **Relationship between $N_A$ and $c_A$ at boundary**  
  $N_A = k_m (c_{A, \text{solid}} - c_{A, \text{fluid}})$

- **Reynolds number**  
  $\mathrm{Re} = \dfrac{L_{\text{char}}v_{\text{char}}\rho}{\mu}$

- **No slip condition**  
  $v_1 = v_2$

- **Free slip condition**  
  $-\mu_1\left(\dfrac{dv_x}{dy}\right)_1 = 0$

- **Continuity of stress**  
  $\begin{aligned}\tau_{y, 1} &= \tau_{y, 2} \\ -\mu_1\left(\dfrac{dv_x}{dy}\right)_1 &= -\mu_2\left(\dfrac{dv_x}{dy}\right)_2 \end{aligned}$

- **Shell balance method**  
  Sketch the system with coordinate system  Sketch the shell that is thin in the direction of transport (change)  Write shell volume $\Delta V$  Write shell balance OIGA of transported quantity  $\mathrm{out - in = generation - accumulation}$

- **Take limit as shell thickness approach 0** — Differential equation of flux distribution

- **Separate variable and integrate**  
  Flux distribution, $c_1$

- **Substitute rate law**  
  Separate variable and integrate  Profile, $c_1, c_2$

## Evaluate $c_1, c_2$ using boundary conditions

*Context:* Axial transport in rectilinear systems; Rectilinear coordinates; No generation; No driving force; Steady state

- **Differential equation of flux distribution**  
  $\dfrac{dq}{dy} = 0$

- **Temperature profile (linear)**  
  $T(y) = T_1 - \dfrac{q}{k} y$

- **Flux distribution (inverse)**  
  $q(y) = \dfrac{k(T_1 - T)}{y}$

- **Flux across the whole layer**  
  $q = \dfrac{k(T_1 - T_2)}{H}$

## Radial transport in cylindrical systems

*Context:* Cylindrical coordinates; No generation; No driving force; Steady state

- **Differential equation of flux distribution**  
  $\dfrac{d(rq)}{dr} = 0$

- **Flux distribution (inverse)**  
  $q(r) = \dfrac{k(T_i - T_0)}{r \ln(\frac{R_0}{R_i})}$

- **Temperature profile (logarithmic)**  
  $T(r) = T_i - \dfrac{T_i - T_0}{\ln(\frac{R_0}{R_i})} \ln\left(\dfrac{r}{R_i}\right)$

## Radial transport in spherical systems

*Context:* Spherical coordinates; No generation; No driving force; Steady state

- **Differential equation of flux distribution**  
  $\dfrac{d(r^2 q)}{dr} = 0$

- **Flux distribution (inverse squared)**  
  $q(r) = \dfrac{k(T_i - T_0)}{r^2 (\frac{1}{R_i} - \frac{1}{R_0})}$

- **Temperature profile (inverse)**  
  $T(r) = T_i - \dfrac{T_i - T_0}{(\frac{1}{R_i} - \frac{1}{R_0})} \left(\dfrac{1}{r} - \dfrac{1}{R_i}\right)$

## Axial transport in rectilinear systems (with generation)

*Context:* Rectilinear coordinates; With generation; No driving force; Steady state

- **Differential equation of flux distribution**  
  $\dfrac{dq}{dy} = S$

- **Flux distribution (linear)**  
  $q(y) = Sy + \dfrac{k}{H}(T_2 - T_1) - \dfrac{SH}{2}$

- **Temperature profile (quadratic)**  
  $T(y) = T_1 - \dfrac{S}{2k} y^2 + \left[ \dfrac{SH}{2k} - \dfrac{T_2 - T_1}{H} \right] y$

## Flow down inclined plane (falling film)

*Context:* Rectilinear coordinates; Gravity driving force, but no pressure gradient; Steady state

- **Differential equation of flux distribution**  
  $\dfrac{d\tau_{yx}}{dy} = \rho g \cos\beta$

- **Flux distribution (linear)**  
  $\tau_{yx}(y) = -\rho g \cos\beta (\delta - y)$

- **Velocity profile (quadratic)**  
  $v_x(y) = \dfrac{g \cos\beta}{2\nu}(2\delta y - y^2)$

- **★ No entry length effect**  
  $L \gg \delta$

- **★ No edge effect**  
  $W \gg \delta$

- **★ Incompressible Newtonian fluid**  
  $\Delta\mu = 0, \Delta\rho = 0$

- **★ No end effect, no ripple**  
  $\mathrm{Re}_{\text{rippling}} \lesssim 20$

- **Reynolds number for falling film**  
  $\mathrm{Re} = \dfrac{4\delta \langle v_x \rangle\rho}{\mu}$

## Flow descriptors

- **Skin friction**  
  $\tau^0 = \rho g \cos(\beta)\delta$

- **Free surface velocity**  
  $v_x^{\text{surf}} = \dfrac{g \cos\beta}{2\nu}\delta^2$

- **Volumetric flow rate**  
  $Q = \int v_\perp \ dA$

- **Volumetric flow rate per unit area**  
  $\dfrac{Q}{W} = \dfrac{g \cos(\beta) \delta^3}{3\nu}$

- **Average velocity**  
  $\langle v_x \rangle = \dfrac{g\cos(\beta)\delta^2}{3\nu}$

- **Mass flow rate**  
  $\dot{m} = \rho Q$

- **Mass flow rate per unit width**  
  $\Gamma = \dfrac{\rho Q}{W} = \dfrac{\rho g \cos(\beta) \delta^3}{3\nu}$

- **Film thickness given $\Gamma$**  
  $\delta = \sqrt[3]{\dfrac{3\nu \Gamma}{\rho g \cos\beta}}$

## Flow in round tube (Hagen-Poiseuille flow)

*Context:* Cylindrical coordinates; Pressure-gravity driving force; Steady state; No tube bents, constant cross section; Negligible P dependence with r

- **Modified pressure**  
  $\mathcal{P} = P + \rho gh$

- **Pressure-gravity driving force**  
  $-\dfrac{dP}{dz} + \rho g \cos\beta = \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L}$

- **Differential equation of flux distribution**  
  $\dfrac{d (r\tau_{rz})}{dr} = \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) r$

- **Flux distribution (linear)**  
  $\tau_{rz}(r) = \dfrac{1}{2} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) r$

- **Velocity profile (quadratic)**  
  $v_z(r) = \dfrac{R^2}{4\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) \left[ 1 - \left( \dfrac{r}{R} \right)^2 \right]$

- **★ Incompressible Newtonian fluid**  
  $\Delta\mu = 0, \Delta\rho = 0$

- **★ Laminar flow**  
  $\mathrm{Re}_{\text{laminar}} \le 2100$

- **★ Fully developed flow (no entry length effect)**  
  $L_e \approxeq 0.035 D \mathrm{Re}$

- **Reynolds number for pipe flow**  
  $\mathrm{Re}_{\text{pipe}} = \dfrac{D \langle v_z \rangle\rho}{\mu}$

## Flow descriptors

- **Skin friction**  
  $\tau_{rz}^0 = \dfrac{1}{2} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) R$

- **Volumetric flow**  
  $Q = \dfrac{R^4 \pi}{8 \mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$

- **Average velocity**  
  $\langle v_z \rangle = \dfrac{R^2}{8\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$

- **Mass flow rate**  
  $\dot{m} = \dfrac{R^4 \pi\rho}{8\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$

## Laminar flow through porous media

- **Darcy’s law - average velocity  $\kappa$ - bed permeability**  
  $\langle v \rangle = \dfrac{\kappa}{\mu L}(\mathcal{P}_1 - \mathcal{P}_2)$

- **Darcy’s law - volumetric flow rate  $A$ - empty bed cross section  $\varepsilon$ - porosity, void fraction**  
  $Q = \dfrac{\kappa A \varepsilon}{\mu L}(\mathcal{P}_1 - \mathcal{P}_2)$

- **Blake-Kozeny model  Bed permeability**  
  $\kappa = \dfrac{D_p^2}{150} \left( \dfrac{\varepsilon}{1 - \varepsilon} \right)^2$

- **Effective packing particle diameter**  
  $D_p = \dfrac{6}{a_v} = \dfrac{6 V}{A} \\ D_{p, \text{spheres}} = D$

- **Bed Reynolds number**  
  $\mathrm{Re}_{\text{bed}} = \dfrac{D_p Q \rho}{\mu A (1-\varepsilon)}$

- **★ Laminar flow**  
  $\mathrm{Re}_{\text{laminar}} < 10$

## Fluid pressure, hydrostatic, manometer

- **Equation of hydrostatic**  
  $P_1 - P_2 = \rho g(h_2 - h_1)$

- **Manometer equation**  
  $P_1 - P_2 = (\rho_m - \rho) gH + \rho g(h_2 - h_1)$

- **Manometer equation**  
  $\mathcal{P}_1 - \mathcal{P}_2 = (\rho_m - \rho) gH$

## Unsteady state transport

- **Unsteady state conduction in rectilinear system**  
  $\left(\dfrac{\partial T}{\partial t}\right)_y = \alpha \dfrac{\partial^2 T}{\partial y^2} + \dfrac{S}{\rho \hat{c_p}}$

- **Unsteady state diffusion in rectilinear system**  
  $\left(\dfrac{\partial c_A}{\partial t}\right)_y = D_{AB} \dfrac{\partial^2 c_A}{\partial y^2} + R_A$

- **Unsteady state Couette flow (1D rectilinear shear flow)**  
  $\left(\dfrac{\partial v_x}{\partial t}\right)_y = \nu \left(\dfrac{\partial^2 v_x}{\partial y^2}\right)_t$

- **Unsteady state flow in cylindrical system**  
  $\left(\dfrac{\partial v_z}{\partial t}\right)_r = \nu \left[ \dfrac{\partial^2 v_z}{\partial r^2} + \dfrac{1}{r} \dfrac{\partial v_z}{\partial r} \right] + \dfrac{1}{\rho} \left[\dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L}\right]$

## Rate Laws in 3D

- **Fourier’s law in 3D**  
  $\utilde{q} = -k \nabla T$

- **Fick’s law in 3D**  
  $\utilde{J}_A^* = -D_{AB} \nabla c_A$

- **Newton’s law of viscosity in 3D**  
  $\underset{\approx}{\tau} = -\mu (\underset{\approx}{\Delta} + \underset{\approx}{\Delta}^{\dagger})$

- **Viscous stress tensor**  
  $\underset{\approx}{\tau} = \begin{bmatrix} \tau_{xx} & \tau_{xy} & \tau_{xz} \\ \tau_{yx} & \tau_{yy} & \tau_{yz} \\ \tau_{zx} & \tau_{zy} & \tau_{zz} \end{bmatrix}$

- **Rate of strain tensor**  
  $\underset{\approx}{\Delta} = \begin{bmatrix} \dfrac{\partial v_x}{\partial x} & \dfrac{\partial v_x}{\partial y} & \dfrac{\partial v_x}{\partial z} \\ \\ \dfrac{\partial v_y}{\partial x} & \dfrac{\partial v_y}{\partial y} & \dfrac{\partial v_y}{\partial z} \\ \\ \dfrac{\partial v_z}{\partial x} & \dfrac{\partial v_z}{\partial y} & \dfrac{\partial v_z}{\partial z} \end{bmatrix}$

## Conservation Laws in 3D

- **Conservation of thermal energy**  
  $\nabla\cdot\utilde{q} = S - \rho \hat{c_p} \dfrac{\partial T}{\partial t}$

- **Conduction equation  ★ No convection**  
  $\dfrac{\partial T}{\partial t} = \alpha \nabla^2 T + \dfrac{S}{\rho \hat{c_p}}$

- **Molecular diffusion equation  ★ No convection**  
  $\dfrac{\partial c_A}{\partial t} = D_{AB} \nabla^2 c_A + R_A$

# Fluid Mechanics
Navier-Stokes Equation

## Navier-Stokes Equation

- **Continuity equation**  
  $\dfrac{\partial \rho}{\partial t} + \nabla\cdot(\rho\utilde{v}) = 0$

- **Continuity equation of incompressible liquid  ★ Constant $\rho$**  
  $\nabla\cdot\utilde{v} = 0$

- **Equation of motion ($v$-form)**  
  $\rho\dfrac{D\utilde{v}}{Dt} = -\nabla p + \mu\nabla^2\utilde{v} + \rho g$

- **Equation of motion ($\tau$-form)**  
  $\rho\dfrac{D\utilde{v}}{Dt} = -\nabla p - \nabla\cdot\underset{\approx}{\tau} + \rho g$

- **Equation of motion ($x$-component)**  
  $\begin{aligned} &\rho \left[ \dfrac{\partial v_x}{\partial t} + \utilde{v}\cdot\nabla v_x \right] \\ =& -\dfrac{\partial p}{\partial x} - \left[ \dfrac{\partial \tau_{xx}}{\partial x} + \dfrac{\partial \tau_{yx}}{\partial y} + \dfrac{\partial \tau_{zx}}{\partial z} \right] + \rho g_x \end{aligned}$

## Operators

Gradient operator $\nabla$ Operates on scalar to give a vector, whose magnitude is the maximum rate of change of the scalar with position, and whose direction points in the direction of that change

Divergence operator $(\nabla\cdot)$ Operates on a vector to give a scalar

Divergence of a flux vector $(\nabla\cdot\utilde{f})$ Rate of efflux (outflow) of the transported quantity per unit volume

- **Laplacian operator**  
  $\nabla^2 = \nabla\cdot\nabla$

- **Substantial derivative operator**  
  $\dfrac{D}{Dt} = \dfrac{\partial}{\partial t} + \utilde{v}\cdot\nabla$

## Generalization to convection

- **Thermal energy equation**  
  $\dfrac{DT}{Dt} = \alpha \nabla^2 T + \dfrac{S}{\rho \hat{c_p}}$

- **Convective diffusion equation**  
  $\dfrac{D c_A}{Dt} = D_{AB} \nabla^2 c_A + R_A$

## Flow in conduit

- **Mach number**  
  $\mathrm{Ma} = \dfrac{v_{\text{char}}}{v_{\text{sound}}}$

- **Conduit flow**  
  $\begin{aligned} \dot{m}_1 &= \dot{m}_2 \\ \rho_1 Q_1 &= \rho_2 Q_2 \end{aligned}$

- **Incompressible conduit flow  ★ Constant $\rho$**  
  $\begin{aligned} Q_1 &= Q_2 \\ A_1 \langle v \rangle_1 &= A_2 \langle v \rangle_2 \end{aligned}$

## Apply N-S Equations (Top-Down) Flow between parallel plates

- **Rectilinear coordinates**  
  $f(x, y, z)$

- **Constant $\rho, \mu$**  
  $\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0$

- **Laminar flow**  
  $\mathrm{Re} < \mathrm{Re}_{\text{cr}}$

- **Steady state**  
  $\frac{\partial}{\partial t} = 0$

- **$v_x$ component only**  
  $v_y = v_z = 0$

- **No edge effect**  
  $\frac{\partial}{\partial z} = 0$

- **No end effect**  
  $\frac{\partial v_x}{\partial x} = 0$

## No hydrostatic pressure diff between plates

*Context:* $b \ll W, L \implies -\frac{\partial p}{\partial y} + \rho g_y = 0$

- **$x$-momentum equation**  
  $\dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} + \mu\dfrac{\partial^2 v_x}{\partial y^2} = 0$

- **Velocity profile (quadratic)**  
  $v_x(y) = \dfrac{1}{2\mu}\left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)(-y^2 + by)$

- **Average velocity**  
  $\langle v_x \rangle = \dfrac{b^2}{12\mu}\left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)$

- **Skin friction at bottom plate**  
  $\tau^0 = \dfrac{b}{2} \left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)$

## Couette flow between concentric rotating cylinders

- **Cylindrical coordinates**  
  $f(r, \theta, z)$

- **Constant $\rho, \mu$**  
  $\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0$

- **Laminar flow**  
  $\mathrm{Re} < \mathrm{Re}_{\text{cr}}$

- **Steady state**  
  $\frac{\partial}{\partial t} = 0$

- **$v_\theta$ component only**  
  $v_r = v_z = 0$

- **Axial symmetry**  
  $\frac{\partial}{\partial \theta} = 0$

- **No end effect**  
  $\frac{\partial v_\theta}{\partial z} = 0$

## Vertical orientation

*Context:* $g_z = -g, g_\theta = g_r = 0$

- **$r$-momentum equation**  
  $-\rho\dfrac{v_\theta^2}{r} = -\dfrac{\partial p}{\partial r}$

- **$\theta$-momentum equation**  
  $\mu\dfrac{\partial}{\partial r} \left( \dfrac{1}{r}\dfrac{\partial}{\partial r} (rv_\theta) \right) = 0$

- **$z$-momentum equation**  
  $-\dfrac{\partial p}{\partial z} - \rho g = 0$

- **Velocity profile (general form)**  
  $v_\theta(r) = c_1\dfrac{r}{2} + \dfrac{c_2}{r}$

- **Velocity profile**  
  $v_\theta(r) = \dfrac{\Omega_0}{1 - \kappa^2}\left[r - \dfrac{(\kappa R)^2}{r}\right]$

- **Pressure profile**  
  $P - P_{\kappa R} = \dfrac{1}{2}\rho \left(\dfrac{\Omega_0\kappa R}{1-\kappa^2}\right)^2 \left[\left(\dfrac{r}{\kappa R}\right)^2 - \left(\dfrac{\kappa R}{r}\right)^2 - 4\ln\left(\dfrac{r}{\kappa R}\right) \right]$

- **Shear stress distribution**  
  $\tau_{r\theta} = -2\mu\kappa^2\left(\dfrac{\Omega_0}{1-\kappa^2}\right)\left(\dfrac{R}{r}\right)^2$

- **Torque**  
  $\mathcal{T} = 4\pi\mu L \Omega_0 R^2\dfrac{\kappa^2}{1 - \kappa^2}$

- **Couette viscometer**  
  $\mu = \dfrac{\mathcal{T}}{4\pi L \Omega_0 R^2}\dfrac{1 - \kappa^2}{\kappa^2}$

## Stoke’s law: Flow around a sphere

- **Spherical coordinates**  
  $f(r, \theta, \phi)$

- **Constant $\rho, \mu$**  
  $\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0$

- **Laminar flow**  
  $\mathrm{Re} < \mathrm{Re}_{\text{cr}}$

- **Steady state**  
  $\frac{\partial}{\partial t} = 0$

- **Axial symmetry**  
  $\frac{\partial}{\partial \phi} = 0$

- **No spinning**  
  $v_\phi = 0$

- **Vertical orientation**  
  $g_r = -g \cos\theta, g_\theta = g \sin\theta, g_\phi = 0$

## $v_\theta$ component only

*Context:* $v_r = v_z = 0$

- **$r$ velocity profile**  
  $v_r = v_\infty \left[ 1 - \dfrac{3}{2}\left(\dfrac{R}{r}\right) + \dfrac{1}{2}\left(\dfrac{R}{r}\right)^2 \right] \cos\theta$

- **$\theta$ velocity profile**  
  $v_\theta = -v_\infty \left[ 1 - \dfrac{3}{4}\left(\dfrac{R}{r}\right) - \dfrac{1}{4}\left(\dfrac{R}{r}\right)^3 \right] \sin\theta$

- **Pressure profile**  
  $p = p_0 - \rho gz - \dfrac{3}{2}\dfrac{\mu v_\infty}{R}\left(\dfrac{R}{r}\right)^2 \cos\theta$

- **Viscous drag**  
  $4\pi\mu v_\infty R$

- **Pressure force (buoyancy + form frag)**  
  $\frac{4}{3}\pi R^3 \rho g + 2\pi R \mu v_\infty$

- **Stoke’s law**  
  $v_\infty = \dfrac{2R^2 (\rho_s - \rho)g}{9\mu}$

- **Falling ball viscometer**  
  $\mu = \dfrac{2R^2 (\rho_s - \rho)g}{9 v_\infty}$

## Centrifuge viscometer

- **Terminal velocity**  
  $v_\infty = \dfrac{2R^2 (\rho_s - \rho) \omega ^2r}{9\mu}$

- **Centrifuge viscometer**  
  $\mu = \dfrac{2R^2 (\rho_s - \rho)\omega^2}{9 \ln\left(\frac{R_2}{R_1}\right)} \Delta t$

- **Turbulence** — Transition to turbulence

- **Geometry** — Reynolds Number; Critical Reynolds Number

- **Circular tube flow**  
  $\mathrm{Re} = \dfrac{D \langle v \rangle \rho}{\mu}$  $\mathrm{Re_c} \approx 2100$

- **Falling film**  
  $\mathrm{Re} = \dfrac{4 \delta \langle v \rangle \rho}{\mu}$  $\mathrm{Re_c} \approx 1500$

- **Flow between parallel plates**  
  $\mathrm{Re} = \dfrac{2b \langle v \rangle \rho}{\mu}$  $\mathrm{Re_c} \approx 1780$

- **Tangential flow in an annulus (Couette flow between rotating cylinders)**  
  $\mathrm{Re} = \dfrac{\Omega_0 R^2 \langle v \rangle \rho}{\mu}$  $\mathrm{Re_c} \approx 50000$

Laminar vs. turbulent

- **Property**  
  Laminar Flow $(\mathrm{Re} < 2100)$  Turbulent Flow $(\mathrm{Re} \in [10^4, 10^5])$

- **Velocity profile**  
  $\dfrac{v_z}{v_{z, \max}} = 1 - \left(\dfrac{r}{R}\right)^2$  $\dfrac{v_z}{v_{z, \max}} \approx \left(1 - \dfrac{r}{R}\right)^{1/7}$

- **Average velocity**  
  $\langle v_z \rangle = \frac{1}{2}v_{z, \max}$  $\langle v_z \rangle \approx \frac{4}{5}\bar{v}_{z, \max}$

- **Volumetric flow rate**  
  $Q = \dfrac{\pi R^4}{8\mu} \left(\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right)$  $Q \propto \left(\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right)^{4/7}$

- **Entry length**  
  $L_e = 0.035 D \mathrm{Re}$  $L_e \approx 40D$

## Derivation

*Context:* From theory; From experiment

- **Velocity decomposition**  
  $v_z = \bar{v}_z + v_z'$

- **Velocity profile in turbulent flow**  
  $\bar{v}_z = \bar{v}_{z, \max}\left(1 - \dfrac{r}{R}\right)^{1/n}$  $n = \begin{cases} 6 & \mathrm{Re} \in [2\times 10^3, 10^4] \\ 7 & \mathrm{Re} \in [10^4, 10^5] \\ 8 & \mathrm{Re} \in [10^5, 10^6] \end{cases}$

## Time-smoothed N-S equation

- **Time-smoothed continuity equation**  
  $\nabla\cdot\utilde{\bar{v}} = 0 \\ \nabla\cdot\utilde{v}' = 0$

- **Time-smoothed equation of motion ($\tau$-form)**  
  $\rho\dfrac{D\utilde{\bar{v}}}{Dt} = -\nabla \bar{p} - \nabla\cdot\underset{\approx}{\bar{\tau}}^{\text{total}} + \rho g$

- **Time-smoothed equation of motion ($x$-component)**  
  $\begin{aligned} &\rho \left[ \dfrac{\partial \bar{v}_x}{\partial t} + \utilde{\bar{v}}\cdot\nabla \bar{v}_x \right] \\ =& -\dfrac{\partial \bar{p}}{\partial x} - \left[ \dfrac{\partial \bar{\tau}^{\text{total}}_{xx}}{\partial x} + \dfrac{\partial \bar{\tau}^{\text{total}}_{yx}}{\partial y} + \dfrac{\partial \bar{\tau}^{\text{total}}_{zx}}{\partial z} \right] + \rho g_x \end{aligned}$

- **Total shear stress (viscous + turbulent)**  
  $\begin{aligned} \bar{\tau}^{\text{total}}_{yx} &= \bar{\tau}_{yx}^{(v)} + \bar{\tau}_{yx}^{(t)} \\ &= \bar{\tau}_{yx} + \rho \overline{v_y' v_x'} \end{aligned}$

## Shear stress distribution

- **Shear stress distribution in round tube**  
  $\tau_{r\theta} = \dfrac{1}{2}\left[\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right]r$

- **Shear stress distribution in general conduit**  
  $\tau_{r\theta} = \left[\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right] R_H$

- **Hydraulic radius**  
  $R_H = \mathrm{\dfrac{cross \ sectional \ area}{wetted \ perimeter}}$

- **Characteristic length**  
  $l_{\text{char}} = 4R_H$

- **Characteristic velocity**  
  $v_{\text{char}} = \langle v_z \rangle$

Universal velocity profile

- **Layer** — Normalized velocity; Normalized length range

- **Laminar sublayer**  
  $v^+ = y^+$  $y^+ \in (0, 5)$

- **Buffer layer**  
  $v^+ = 5 \ln(y^+ + 0.205) - 3.27$  $y^+ \in (5, 30)$

## Turbulent core

*Context:* $v^+ = 2.5 \ln(y^+) + 5.5$; $y^+ \in (30, \infty)$

- **Characteristic length**  
  $y_* = \dfrac{\mu}{v_* \rho}$

- **Characteristic velocity**  
  $v_* = \sqrt{\dfrac{\tau^0}{\rho}}$

- **Normalized length**  
  $y^+ = \dfrac{y}{y_*}$

- **Normalized velocity**  
  $v^+ = \dfrac{v}{v_*}$

- **Eddie viscosity**  
  $\mu^{(t)} = - \dfrac{\bar{\tau}_{yz}^{\text{total}}}{\left(\frac{dv_z}{dy}\right)} - \mu = - \dfrac{\left[\frac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right] \frac{r}{2}}{\left(\frac{dv_z}{dy}\right)} - \mu$

## Dynamic Similarity and Dimensional Analysis

*Context:* Flow around a sphere outside of Stoke’s law

- **★ Non-Stoke’s law condition**  
  $\mathrm{Re} \ge 0.1$

- **Nondimensionalized continuity equation**  
  $\breve{\nabla}\cdot\utilde{\breve{v}} = 0$

- **x-component of momentum equation**  
  $\dfrac{D\breve{v}_x}{D\breve{t}} = -\dfrac{\partial\breve{p}}{\partial\breve{x}} + \dfrac{1}{\mathrm{Re}}\breve{\nabla}^2 \breve{v}_x + \dfrac{1}{\mathrm{Fr}}\breve{g}_x$

- **Drag coefficient  Friction factor**  
  $c_D = f = \dfrac{F_D}{\frac{1}{2}\rho v_\infty^2 A_{\text{approach}}}$

- **Drag coefficient in Stoke’s law region**  
  $c_D = \dfrac{24}{\mathrm{Re}}$

- **Drag coefficient in non-Stoke’s law region**  
  $c_D = \left(\sqrt{\dfrac{24}{\mathrm{Re}}} + 0.5407\right)^2$

## Dimensionless groups

- **Reynolds number**  
  $\mathrm{Re} = \dfrac{l_0 v_0 \rho}{\mu} = \mathrm{\dfrac{inertial \ forces}{viscous \ forces}}$

- **Froude number**  
  $\mathrm{Fr} = \dfrac{v_0^2}{gl_0} = \mathrm{\dfrac{inertial \ forces}{gravitational \ forces}}$

- **Capillary number**  
  $\mathrm{Ca} = \dfrac{\mu v_0}{\sigma} = \mathrm{\dfrac{viscous \ forces}{surface \ tension \ forces}}$

- **Weber number**  
  $\mathrm{Fr} = \dfrac{l_0 \rho v_0^2}{\sigma} = \mathrm{\dfrac{inertial \ forces}{surface \ tension \ forces}}$

- **Euler’s number**  
  $\mathrm{Eu} = \dfrac{(\Delta p)D^4}{\rho Q^2}$

- **Dimensional analysis**  
  Buckingham $\pi$ theorem - A function $f(X_1, X_2, \dots, X_k)$ with dimensional variables $X_i$ can be rewritten in a function $\Phi(\Pi_1, \Pi_2, \dots, \Pi_{k-n})$ with dimensionless variables $\Pi_j$ by enforcing dimensional consistency using $n$ fundamental dimensions.  Define fundamental dimensions  Choose stand-in variables for fundamental dimensions  Rewrite other variables in terms of stand-in variables to get dimensionless groups

## Bernoulli Analysis and Applications N-S equation for steady flow in stream tubes

- **Constant density fluid**  
  $\Delta \rho = 0$

- **1D flow in $z$ direction**  
  $v_r = v_\theta = 0$

- **Plug flow - uniform velocity across cross section**  
  $\langle v \rangle = v = \mathrm{constant} \\ v_z = v_z(z)$

- **Inviscid flow**  
  $\mu \approx 0, \mathrm{Re} \ge 10000$

## No sharp bends

*Context:* Straight stream lines

- **Continuity equation**  
  $\begin{aligned} Q_1 &= Q_2 \\ A_1 \langle v \rangle_1 &= A_2 \langle v \rangle_2 \end{aligned}$

- **Equation of motion**  
  $\rho v \dfrac{dv}{dz} = -\dfrac{dp}{dz} - \rho g \dfrac{dh}{dz}$

## Bernoulli equation

- **Bernoulli equation (energy form)**  
  $p_1 + \frac{1}{2}\rho v_1^2 + \rho gh_1 = p_2 + \frac{1}{2}\rho v_2^2 + \rho gh_2$

- **Bernoulli equation (head form)**  
  $\dfrac{v_1^2}{2g} + \dfrac{p_1}{\rho g} + h_1 = \dfrac{v_2^2}{2g} + \dfrac{p_2}{\rho g} + h_2$

- **Bernoulli head**  
  $\mathcal{B} = \dfrac{v^2}{2g} + \dfrac{p}{\rho g} + h = \mathrm{constant}$

- **Drag coefficient**  
  $c_D = \dfrac{F_D}{\frac{1}{2}\rho v_\infty^2 A_{\text{approach}}}$

- **Lift coefficient**  
  $c_L = \dfrac{F_L}{\frac{1}{2}\rho v_\infty^2 A_{\text{planform}}}$

- **Pressure change in contracting conduit  $\Delta p \equiv p_1 - p_2$**  
  $\Delta p = \dfrac{8\rho Q^2}{\pi^2 D_1^4}\left[\left(\dfrac{D_1}{D_2}\right)^4 - 1\right] + \rho g (h_2 - h_1)$

- **Torricelli’s law**  
  $\langle v \rangle = \sqrt{2g\Delta h}$

- **Pressure at stagnation point**  
  $\begin{aligned} p &= p_{\text{static}} + p_{\text{dynamic}} \\ &= p_{\text{static}} + \textstyle\frac{1}{2}\rho v_\infty^2 \end{aligned}$

## Flow-metering devices

- **Manometer equation**  
  $\Delta p = (\rho_\mathrm{m} - \rho)gH$

- **Local velocity  Pitot tube**  
  $v = \sqrt{\dfrac{2\Delta p}{\rho}}$

- **Volumetric flow rate  Venturi meter $c_0 \in [0.96, 0.98]$  Orfice meter $c_0 \in [0.40, 0.80]$  Nozzle meter $c_0 \in [0.96, 0.98]$**  
  $Q = c_0\pi D_0^2 \sqrt{\dfrac{\Delta p}{8\rho [1 - (\frac{D_0}{D})^4]}}$

- **Rotameter** — Calibrated specifically to the fluid with falling sphere

## Full Bernoulli analysis

- **Full Bernoulli equation**  
  $\dfrac{v_1^2}{2g} + \dfrac{p_1}{\rho g} + h_1 = \dfrac{v_2^2}{2g} + \dfrac{p_2}{\rho g} + h_2 + H_{L12}$

- **Head loss**  
  $H_{L12} = H_{L12f} + H_{L12c}$

Skin friction loss $H_{L12f}$ Viscous work done per unit weight by fluid on walls of conduit in moving from 1 to 2

- **Skin friction loss (general)**  
  $H_{L12f} = \dfrac{\tau^0 L}{\rho g R_H}$

- **Skin friction loss for circular tube**  
  $H_{L12f} = \dfrac{4\tau^0 L}{\rho g D}$

- **Fanning friction factor**  
  $f = \dfrac{\tau^0}{\frac{1}{2}\rho \langle v \rangle^2}$

- **Skin friction loss for circular tube**  
  $H_{L12f} = \dfrac{2\langle v \rangle^2 L}{g D}f = \dfrac{32Q^2 L}{\pi^2 D^5 g}f$

- **Skin friction loss for non-circular tube**  
  $H_{L12f} = \dfrac{\langle v \rangle^2 L}{2 g R_H}f = \dfrac{Q^2 L}{2g A_c^2 R_H}f$

- **Reynolds number for noncircular pipes**  
  $\mathrm{Re} = \dfrac{4R_H \langle v \rangle \rho}{\mu}$

- **Configurational loss of one fitting in circular tube**  
  $H_{Lc} = e_v\dfrac{\langle v \rangle^2_{\text{downstream}}}{2g}$

- **Configurational loss of all fittings in circular tube**  
  $H_{L12c} = \dfrac{\langle v \rangle^2_{\text{down}}}{2g} (\sum\limits_i e_{v, i}) = \dfrac{8Q^2}{\pi^2 D^4 g} (\sum\limits_i e_{v, i})$

- **Total head loss for circular tube**  
  $H_{L12} = \begin{cases} \dfrac{2 \langle v \rangle^2}{Dg} [(\sum\limits_i L_i)f + \frac{D}{4} (\sum\limits_i e_{v, i})] \\ \dfrac{32 Q^2}{\pi^2 D^5 g} [(\sum\limits_i L_i)f + \frac{D}{4} (\sum\limits_i e_{v, i})] \end{cases}$

- **Kinetic head correction factor**  
  $\alpha = \dfrac{\langle v^3 \rangle}{\langle v \rangle^3}$

- **Brake horse power**  
  $\mathrm{bhp} = \dfrac{P}{\eta} = \dfrac{H_p \rho g Q}{\eta}$

## Fanning friction factor correlations

- **Description** — Equations; Conditions

- **Hydraulically smooth pipes (Blasius)**  
  $f = \dfrac{0.0791}{\mathrm{Re}^1/4}$  $\mathrm{Re} \in [2100, 10^5]$

- **Hydraulically smooth pipes (Koo)**  
  $f = 0.0014 + \dfrac{0.125}{\mathrm{Re}^{0.32}}$  $\mathrm{Re} \in [10^4, 10^7]$

- **Pipes of general roughness (Haaland)**  
  $\dfrac{1}{\sqrt{f}} = -3.6\log_{10} \left[\dfrac{6.9}{\mathrm{Re}} + \left(\dfrac{k/D}{3.7}\right)^{10/9}\right]$  $\mathrm{Re} \in [4\times 10^4, 10^7] \\ k/D < 0.05$

- **Commercial standard piping (Drew)**  
  $f = 0.0014 + \dfrac{0.090}{\mathrm{Re}^{0.27}}$  $\mathrm{Re} \in [10^4, 10^7] \\ k/D \approx 0.00015$

- **Full rough conduit**  
  $\dfrac{1}{\sqrt{f}} = 2.28 - 4.0 \log_{10} \left(\dfrac{k}{D}\right)$  $\mathrm{Re} > 10^4 \\ k/D > 0.01$

Kinetic head correction factor

- **$\mathrm{Re}$**  
  $n$  $\alpha$

- **$2 \times 10^3 \sim 10^4$**  
  $6$  $1.08$

- **$10^4 \sim 10^5$**  
  $7$  $1.06$

- **$10^5 \sim 10^7$**  
  $8$  $1.05$

## Flow through packed bed

- **Specific area of packing element**  
  $a_v = \dfrac{\text{area of packing element}}{\text{volume of packing element}}$

- **Effective diameter of packing element (particle)**  
  $D_p = \dfrac{6}{a_v}$

- **Darcy’s law  ★ $\mathrm{Re_{bed}} \lesssim 10$**  
  $\langle v \rangle = \dfrac{\kappa}{\mu} \left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right]$

- **Volumetric flow rate**  
  $Q = \langle v \rangle \varepsilon A = v_0 A$

- **Superficial velocity**  
  $v_0 = \langle v \rangle \varepsilon$

- **Bed Reynolds number**  
  $\begin{aligned}\mathrm{Re_{bed}} &= \dfrac{D_p v_0 \rho}{\mu}\dfrac{1}{1 - \varepsilon} \\ &= \dfrac{D_p \langle v \rangle \rho}{\mu}\dfrac{\varepsilon}{1 - \varepsilon} \\ &= \dfrac{D_p Q \rho}{\mu A}\dfrac{1}{1 - \varepsilon}\end{aligned} $

- **Tube Reynolds number**  
  $\mathrm{Re_{tube}} = \dfrac{2}{3}\mathrm{Re_{bed}}$

- **Hydrolic radius**  
  $R_H = \dfrac{D_p\varepsilon}{6(1-\varepsilon)}$

- **Friction factor of tube  ★ $\mathrm{Re_{bed}} \le 10$**  
  $f_{\text{tube}} = \dfrac{24(1-\varepsilon)\mu}{D_p v_0 \rho}$

- **Friction factor of tube  ★ $\mathrm{Re_{bed}} > 1000$**  
  $f_{\text{tube}} = \dfrac{7}{12}$

- **Bed permeability**  
  $\kappa = \dfrac{D_p^2}{150} \left(\dfrac{\varepsilon}{1-\varepsilon}\right)^2$

- **Blake-Kozeny equation  ★ $\mathrm{Re_{bed}} \le 10$**  
  $\left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right] = 150 \dfrac{\mu v_0}{D_p^2}\dfrac{(1-\varepsilon)^2}{\varepsilon^3}$

- **Burke-Plummer equation  ★ $\mathrm{Re_{bed}} > 1000$**  
  $\left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right] = \dfrac{7}{4}\dfrac{\rho v_0^2}{D_p}\dfrac{1-\varepsilon}{\varepsilon^2}$

- **Superficial mass flux**  
  $G_0 = \rho v_0 = \dfrac{\dot{m}}{A}$

- **Ergun equation  ★ $\mathrm{Re_{bed}} \in [10, 1000]$**  
  $\left[ \dfrac{(\mathcal{P}_0 - \mathcal{P}_L)\rho}{G_0^2} \right] \dfrac{D_p}{L}\dfrac{\varepsilon^3}{1-\varepsilon} = 150 \left[ \dfrac{1-\varepsilon}{\frac{D_p G_0}{\mu}} \right] + \dfrac{7}{4} \\ \left[ \dfrac{(\mathcal{P}_0 - \mathcal{P}_L)\rho}{G_0^2} \right] \dfrac{D_p}{L}\dfrac{\varepsilon^3}{1-\varepsilon} = 150 \dfrac{1}{\mathrm{Re_{bed}}} + \dfrac{7}{4}$

## Cavitation and vortex motion

- **Cavitation number**  
  $\sigma = \dfrac{p_A - p_C}{\frac{1}{2}\rho v_\infty^2}$

## Forced vortex flow in rotating cylinder

- **Velocity profile**  
  $v_\theta = r\Omega$

- **Pressure difference  ★ 1 defined arbitrarily, 2 defined at center**  
  $p_2 - p_1 = \dfrac{1}{2}\rho\Omega^2 (r_2^2 - r_1^2) + \rho g (z_1 - z_2)$

- **Height**  
  $h = \dfrac{\Omega^2}{2g} r^2$

## Free vortex flow during drainage

- **Pressure difference   ★ 1 defined arbitrarily, 2 defined at $r \to\infty$**  
  $p_2 - p_1 = \dfrac{1}{2}\rho C^2 \left(\dfrac{1}{r_1^2} - \dfrac{1}{r_2^2}\right) + \rho g (z_1 - z_2)$

- **Depth**  
  $h = \dfrac{C^2}{2g} \dfrac{1}{r^2}$

## Microfluidics*

*Context:* Validity of continuum description

- **Mean free path**  
  $\lambda = \dfrac{1}{\sqrt{2}\pi d^2 n} \\ \lambda(\mathrm{\mu m}) \approx 3.1\times 10^{-3} \dfrac{T(\mathrm{K})}{\sigma^2(\mathrm{\mathring{A}^2}) p(\mathrm{atm})}$

- **Knudsen number**  
  $\mathrm{Kn} = \dfrac{\lambda}{L_c}$

- **Characteristics** — Range

- **Molecular flow**  
  $\mathrm{Kn} \in (10, \infty)$

- **Transition flow**  
  $\mathrm{Kn} \in (0.1, 10)$

- **N-S equations hold, but no-slip condition fails**  
  $\mathrm{Kn} \in (0.001, 0.1)$

- **N-S equations hold, and no-slip condition holds**  
  $\mathrm{Kn} \in (0, 0.001)$

Forces in microfluidic flows Viscous force dominate over inertial forces and gravity forces Driving force Pressure Capillary (surface tension) forces Electro-kinetic forces Magnetic forces

## Resisting forces: viscous force, dominated by wall effects

- **Reynolds number  ★ Creeping flow**  
  $\mathrm{Re} = \dfrac{\text{inertial forces}}{\text{viscous forces}} = \dfrac{Lv\rho}{\mu} \to 0$

- **Froude number**  
  $\mathrm{Fr} = \dfrac{\text{inertial forces}}{\text{gravity forces}} = \dfrac{v^2}{gL}$

- **Viscous force dominates gravity force**  
  $\mathrm{\dfrac{Re}{Fr}} = \dfrac{\text{gravity forces}}{\text{viscous forces}} = \dfrac{gL^2}{\mu v} \to 0$

## Generalized Hagen-Poiseuille flow

- **Differential equation of generalized H-P flow**  
  $0 = \dfrac{\Delta p}{L} + \mu \left(\dfrac{\partial^2 v_z}{\partial x^2} + \dfrac{\partial^2 v_z}{\partial y^2}\right)$

- **No-slip condition  $F(x, y)$ is equation of conduit perimeter**  
  $v_z(x, y) = 0 for F(x, y) = 0$

- **Velocity profile**  
  $v_z(x, y) = \dfrac{\Delta p}{\mu L} F(x, y)$

- **Volumetric flow rate**  
  $Q = \dfrac{\Delta p}{\mu L} \displaystyle\iint F(x, y) \ dy\ dx$

## Hydraulic resistance in micro-channels

- **Flow equation**  
  $\Delta p = \mathcal{R}_{\text{hyd}}Q$

- **Volumetric flow rate**  
  $Q = \dfrac{\Delta p}{\mathcal{R}_{\text{hyd}}}$

## Capillary driving force and wicking phenomena

- **Pressure difference**  
  $\Delta p = \sigma\kappa = \dfrac{2\sigma}{R}$

- **Wicking velocity**  
  $v = \dfrac{r^2}{8\mu}\dfrac{\Delta P}{x} = \dfrac{r\sigma \cos\theta}{4\mu x}$

- **Washburn equation**  
  $x = \sqrt{\dfrac{r\sigma\cos\theta}{2\mu} t} \propto \sqrt{t}$

- **Wicking into porous media**  
  $h = \sqrt{\dfrac{r_e\sigma\cos\theta}{2\mu} t} \propto \sqrt{t}$

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

- **Equilibrium conditions**  
  $\begin{aligned}T_1 &= T_2 \\ P_1 &= P_2 \\ \bar{f}_2 &= \bar{f}_2 \\ a_1 &= a_2\end{aligned}$

- **Fugacity**  
  $\bar{f}_i = \bar{f}_i^\circ \exp\left(\dfrac{\mu_i}{RT}\right)$

- **Fugacity coefficient**  
  $\phi_i = \dfrac{f_i}{P}$

- **Partial fugacity coefficient**  
  $\phi_i = \dfrac{f_i}{x_iP}$

- **Activity**  
  $a_i = \dfrac{\bar{f}_i}{f_i^\circ}$

- **Activity coefficient**  
  $\gamma_i = \dfrac{a_i}{x_i}$

## $K$-values

- **$K$-value (vapor-liquid equilibrium ratio)**  
  $K_i = \dfrac{y_i}{x_i}$

- **Distribution ratio (partition coefficient, liquid-liquid equilibrium ratio**  
  $K_{D_i} = \dfrac{x_i^\alpha}{x_i^\beta}$

- **Relative volatility**  
  $\alpha_{i, j} = \dfrac{K_i}{K_j}$

- **Relative selectivity**  
  $\beta{i, j} = \dfrac{K_{D_i}}{K_{D_j}}$

- **Raoult’s law  ★ Ideal solution**  
  $K_i = \dfrac{P_i^*}{P}$

- **Modified Raoult’s law  ★ Low pressure**  
  $K_i = \gamma_{i, L}\dfrac{P_i^*}{P}$

- **Poynting correction  ★ Moderate pressure**  
  $K_i = \gamma_{i, L}\phi_{i, V}^\mathrm{sat}\left(\dfrac{P_i^\mathrm{sat}}{P}\right) \exp\left[\dfrac{1}{RT}\displaystyle\int^P_{P_i^{\mathrm{sat}}} v_{i, L} dP \right]$

- **Henry’s law  ★ Dilute species**  
  $K_i = \dfrac{H_i}{P}$

## Mass Transfer and Diffusion

*Context:* Steady-state ordinary molecular diffusion (OMD)

- **Fick’s first law  Molecular diffusion flux of species A**  
  $\begin{aligned} J_{A} &= -cD_{AB}\dfrac{dx_A}{dx} \\ &= -D_{AB} \dfrac{dc_A}{dz} \end{aligned}  \\ j_{A} = -\rho D_{AB}\dfrac{dw_A}{dz}$

- **Bulk flow flux**  
  $N = N_A + N_B$

- **Bulk flow flux of species A**  
  $x_A N$

- **Molar flux of species A (definition)**  
  $N_A = \dfrac{\dot{n}_A}{A}$

- **Molar flux of species A  ★ No eddie diffusion flux**  
  $\begin{aligned} N_A &= \text{bulk flow flux} + \text{molecular diffusion flux}\\ N_A &= x_A N - cD_{AB} \dfrac{dx_A}{dz} \end{aligned}$

- **Total velocity of species A**  
  $v_A = \dfrac{N_A}{c_A}$

- **Molar-average mixture velocity**  
  $v_M = v_Ax_A + v_Bx_B$

- **Diffusion velocity of species A**  
  $v_{D, A} = \dfrac{J_A}{c_A}$

- **Velocity relations**  
  $v_A = v_M + v_{D, A}$

## Equimolar counter diffusion (EMD)

- **Equimolar counter diffusion**  
  $N_A = - N_B$

- **No bulk flow**  
  $N = 0$

- **Molar flux of species A  Molecular diffusion flux of species A**  
  $N_A = J_A = -cD_{AB} \dfrac{\Delta x_A}{\Delta z}$

- **Concentration profile of species A**  
  $c_A = c_{A0} - \dfrac{J_A z}{D_{AB}}$

- **Concentration profile of species B**  
  $c_B = c_{B0} + \dfrac{J_A (z-L)}{D_{AB}}$

## Unimolecular diffusion (UMD)

- **Stagnant B**  
  $N_B = 0$

- **Molar flux of species A  Bulk flow flux**  
  $N = N_A$

- **Molar flux of species A**  
  $N_A = \dfrac{cD_{AB}}{z - z_1} \ln\left(\dfrac{1 - x_A}{1 - x_{A, 1}}\right)$

- **Molar flux of species A**  
  $N_A = -\dfrac{cD_{AB}}{(1 - x_A)_{\mathrm{LM}}} \dfrac{\Delta x_A}{\Delta z}$

- **Dilute A reduces UMD to EMD (no bulk flow)**  
  $(1 - x_A)_{\mathrm{LM}} \approx 1 \quad \text{if } x_A \to 0$

- **Log-mean**  
  $x_{\mathrm{LM}} = \dfrac{x_2 - x_1}{\ln(x_2/x_1)}$

- **Composition profile**  
  $x_A(z) = 1 - (1 - x_A) \exp\left[\dfrac{N_A (z - z_1)}{cD_{AB}}\right]$

- **Molecular diffusion and bulk flow flux of species**  
  $J_A = x_B N = - J_B$

- **Changing liquid level of A with stagnant B**  
  $N_A = -\dfrac{cD_{AB}}{(1 - x_A)_{\mathrm{LM}}} \dfrac{\Delta x_A}{z} = \dfrac{\rho_A}{\mathcal{M}_A}\dfrac{dz}{dt}$

## Diffusivity

*Context:* Diffusivity of gas mixtures

- **Fuller-Schettler-Giddings correlation  ★ Low pressure (0 - 10 atm)  ★ $D_{AB} \ [\mathrm{cm^2/s}]$  ★ $P \ [\mathrm{atm}], T \ [\mathrm{K}]$  ★ $\mathcal{M}_{AB} \ [\mathrm{g/mol}]$**  
  $D_{AB} = D_{BA} = \dfrac{0.00143 T^{1.75}}{P \mathcal{M}_{AB}^{1/2} \left[(\sum_V)_A^{1/3} + (\sum_V)_B^{1/3}\right]^2} \\ $

- **Effective molecular mass**  
  $\mathcal{M}_{AB} = \dfrac{2}{\dfrac{1}{\mathcal{M}_A} + \dfrac{1}{\mathcal{M}_B}}$

- **Summation of atomic and structural diffusion volumes (Table 3.1)**  
  $\sum_V$

- **Takahashi correlation  ★ High pressure (Figure 3.3)**  
  $\dfrac{D_{AB} P}{(D_{AB}P)_{\text{low }P}} = \mathrm{const}$

- **Molar averaged reduced properties**  
  $T_r = x_A T_{r, A} + x_B T_{r, B} \\ P_r = x_A P_{r, A} + x_B P_{r, B}$

## Diffusivity of nonelectrolyte liquid mixtures

- **Stoke-Einstein equation  ★ Infinite dilution**  
  $(D_{AB})_\infty = \dfrac{RT}{6\pi \mu_B R_A N_A} \propto \dfrac{T}{\mu_B R_A}$

- **Wilke-Chang equation  ★ Low pressure (0 - 10 atm)  ★ $D_{AB} \ [\mathrm{cm^2/s}]$  ★ $\mu_B \ [\mathrm{cP}], T \ [\mathrm{K}]$  ★ $\mathcal{M}_{AB} \ [\mathrm{g/mol}]$  ★ $v_A \ [\mathrm{cm^3/mol}]$**  
  $(D_{AB})_\infty = 7.4\times 10^{-8} \dfrac{(\phi_B \mathcal{M}_B)^{1/2}T}{\mu_B v_A^{0.6}}$

- **Hayduk-Minhas correlation  (Modified Wilke-Chang equation)**  
  $(D_{AB})_\infty = 13/3\times 10^{-8} \dfrac{T^{1.47}\mu_B^\varepsilon}{v_A^{0.71}} \\ \varepsilon = \dfrac{10.2}{v_A} - 0.791$

## Film theory for mass transfer at fluid-fluid interface

*Context:* Single film theory

- **Concentration and mole fraction**  
  $c_A = x_Ac$

- **Mass transfer coefficient (no bulk flow)**  
  $k_c = \dfrac{D_{AB}}{\delta}$

- **Mass transfer coefficient (with bulk flow)**  
  $k'_c = \dfrac{D_{AB}}{\delta (1 - x_A)_{\mathrm{LM}}}$

- **Molar flux of species A  ★ Interface (i), bulk (b)**  
  $N_A = \pm k_c (c_{A, i} - c_{A, b}) \\ N_A = \pm k'_c (c_{A, i} - c_{A, b})$

- **Film thickness**  
  $\delta = \dfrac{D_{AB}}{k_c} = \dfrac{D_{AB}}{k'_c (1 - x_A)_{\mathrm{LM}}}$

Mass transfer coefficient and driving force

- **Concentration (liquid)**  
  $k_c \ [\mathrm{m/s}]$  $N_A = \pm k_c (c_{A, i} - c_{A, b})$

- **Pressure (vapor)**  
  $k_p \ [\mathrm{mol/m^2 \cdot s \cdot Pa}]$  $N_A = \pm k_p (P_{A, i} - P_{A, b})$

- **Mole fraction (liquid)**  
  $k_x \ [\mathrm{mol/m^2 \cdot s}]$  $N_A = \pm k_x (x_{A, i} - x_{A, b})$

## Mole fraction (vapor)

*Context:* $k_y \ [\mathrm{mol/m^2 \cdot s}]$; $N_A = \pm k_y (y_{A, i} - y_{A, b})$

- **Liquid phase coefficient conversion**  
  $k_x = k_c c = k_c \dfrac{\rho_L}{\mathcal{M}_L}$

- **Vapor phase coefficient conversion**  
  $k_y = k_p P = (k_c)_g c = (k_c)_g \dfrac{P}{RT} = (k_c)_g \dfrac{\rho_G}{\mathcal{M}_G}$

- **Liquid phase bulk flow correction**  
  $k' = \dfrac{k}{(1 - x_A)_{\mathrm{LM}}}$

- **Gas phase bulk flow correction**  
  $k' = \dfrac{k}{(1 - y_A)_{\mathrm{LM}}}$

Two-film theory

- **Based on** — Overall Mass Transfer Coefficient; Equations; Fictitious properties

- **Liquid phase**  
  $\dfrac{1}{K_L} = \dfrac{H_A}{k_p} + \dfrac{1}{k_c}$  $N_A = \pm K_L (c_A^* - c_{A, b})$  $c_A^* = P_{A, b} H_A$

- **Gas phase**  
  $\dfrac{1}{K_G} = \dfrac{1}{k_p} + \dfrac{1}{H_A k_c}$  $N_A = \pm K_G (P_{A, b} - P_A^*)$  $P_A^* = \dfrac{c_{A, b}}{H_A}$

- **Liquid phase mole fraction**  
  $\dfrac{1}{K_x} = \dfrac{1}{K_a k_y} + \dfrac{1}{k_x}$  $N_A = \pm K_y (y_{A, b} - y_{A}^*)$  $y_A^* = x_{A, b}K_A$

- **Gas phase mole fraction**  
  $\dfrac{1}{K_y} = \dfrac{1}{k_y} + \dfrac{K_A}{k_x}$  $N_A = \pm K_x (x_{A}^* - x_{A, b})$  $x_A^* = \dfrac{y_{A, b}}{K_A}$

## Single Equilibrium Stages

*Context:* Degrees of freedom

- **Gibbs' phase rule**  
  $\mathrm{DOF = component - phase + 2}$

- **Degree of freedom**  
  $\small\text{DOF = \# intensive variables} - \text{\# independent eqns}$

- **Azeotrope**  
  $x_i = y_i$

- **$q$-line**  
  $y_H = \left[\dfrac{(V/F) - 1}{(V/F)}\right] x_H + \left[\dfrac{1}{(V/F)}\right] z_H$

Rachford-Rice algorithm for isothermal flash calculation

Symbol Conventions

- **Molar flow rates**  
  $F$ - Feed  $V$ - Output vapor  $L$ - Output liquid

## Molar fraction of component i

*Context:* $x_i$ - In the liquid; $y_i$ - In the vapor; $z_i$ - Overall

- **Road map**  
  Known -  $K_i, z_i, F$  Solve - $\Psi \to V \to L \to x_i, y_i \to Q$

- **Vapor-to feed ratio**  
  $\Psi \equiv \dfrac{V}{F}$

- **Objective function  ★ Derived from $\sum y_i - \sum x_i = 0$**  
  $f(\Psi) = \displaystyle\sum_i \dfrac{z_i (1 - K_i)}{[1 + \Psi(K_i - 1)]} = 0$

- **Derivative of objective function**  
  $f'(\Psi) = \displaystyle\sum_i \dfrac{z_i (1 - K_i)^2}{[1 + \Psi(K_i - 1)]^2}$

- **Newton’s method for root finding**  
  $\Psi_{n+1} = \Psi_n - \dfrac{f(\Psi_n)}{f'(\Psi_n)}$

- **Vapor molar flow rate**  
  $V = \Psi F$

- **Liquid molar flow rate**  
  $L = F - V$

- **Vapor mole fraction**  
  $x_i = \dfrac{z_i}{1 + \Psi(K_i - 1)}$

- **Liquid mole fraction**  
  $y_i = \dfrac{z_i K_i}{1 + \Psi(K_i - 1)}$

- **Heat**  
  $Q = h_V V + h_L L - h_F F$

## Bubble and dew point calculations

*Context:* Flash operations of flash vaporization and partial condensation. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p93, Figures 4.8, 4.9.)

- **Bubble point**  
  $\Psi = 0 \\ \sum z_i K_i = 1 \\ \sum \dfrac{y_i}{P_i^* (T)} = \dfrac{1}{P}$

- **Dew point**  
  $\Psi = 1 \\ \sum \dfrac{z_i}{K_i} = 1 \\ \sum x_i P_i^* (T) = P$

Ternary liquid-liquid extraction

Symbol Conventions

- **Components**  
  $A$ - Carrier (feed solvent)  $B$ - Solute  $C$ - Solvent

- **Mass flow rates**  
  $F$ - Feed  $S$ - Solvent  $E$ - Extract (Majority of solvent $C$ carrier extracted solute $B$)  $R$ - Raffinate

- **Mass fraction of component i**  
  $x_i$ - In the liquid  $y_i$ - In the vapor  $z_i$ - Overall

## Mass ratio of component i

*Context:* $X_i$ - In the liquid; $Y_i$ - In the vapor

- **Mass fraction**  
  $x_i = \dfrac{m_i}{m}$

- **Mass ratio**  
  $X_i = \dfrac{m_i}{m - m_i}$

- **Conversion between mass fraction and ratio**  
  $X_i = \dfrac{x_i}{1 - x_i} \\ x_i = \dfrac{X_i}{1 - X_i}$

- **Solute balance  ★ Solvent A, Solute B  ★ Feed F, Solvent S, Extract E, Raffinate R**  
  $\begin{aligned} F_B &= E_B + R_B & \\ X_{F, B} F_A &= Y_{E, B} S + X_{R, B}F_A & Y_{E, B} = K'_{D_B} X_{R, B} \\ X_{F, B}F_A &= K'_{D_B} X_{R, B}S + X_{R, B}F_A & \\ X_{R, B} &= \dfrac{X_{F, B} F_A}{F_A + K'_{D_B} S} \end{aligned}$

- **Extraction factor of solute B**  
  $\mathcal{E} = \dfrac{K'_{D_B} S}{F_A}$

- **Fraction of solute B unextracted**  
  $\dfrac{X_{R, B}}{X_{F, B}} = \dfrac{1}{1 + \mathcal{E}}$

Liquid-liquid extraction of ternary mixture. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p98, Figure 4.12.) Ternary phase diagram General principles are the same for different types of ternary phase diagrams. Here, algorithm for using equilateral ternary phase diagrams is presented. Identify chemical species at the apexes: feed solvent (A), feed solute (B), and pure solvent (S) Apexes are pure components Lines parallel to the apex are used to read values Label each side of the triangle according to the apex

- **Identify compositions of entering streams: feed (F) and solvent (S)**  
  Assume feed only contains A and B, and solvent is pure S  Calculate composition of mixture (M) with component balances  $x_{M, A} = \dfrac{x_{F, A} F}{F + S}, \quad x_{M, B} = \dfrac{x_{F, B} F}{F + S}, \quad x_{M, C} = \dfrac{S}{F + S}$

- **Interpolate tie line on the ternary phase diagram** — Identify compositions of exiting streams: extract (E) and raffinate (R); E and R lies on the intersection of tie line and miscibility boundary (binodal) curve; E has a larger S component than R (extracted component is dissolved in solvent), being closer to point S

- **Identify plait point (P)** — P lies between E and R on the miscibility boundary curve; P the the point where E and R merge together and tie line collapses to a point

- **Determine flow rate ratio with inverse level rule**  
  $\dfrac{E}{F + S} = \dfrac{E}{E + R} = \dfrac{\overline{MR}}{\overline{ER}}, \quad \dfrac{E}{R} = \dfrac{\overline{MR}}{\overline{ME}}$

- **Sample equilateral ternary phase diagram. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p101, Figure 4.14.)** — Multistage Cascades

- **Single stage**  
  $\dfrac{X_{R, B}}{X_{F, B}} = \dfrac{1}{1 + \mathcal{E}}$

- **Cocurrent cascade ($N$ stages)**  
  $\dfrac{X_{N, B}}{X_{F, B}} = \dfrac{1}{1 + \mathcal{E}}$

- **Crosscurrent cascade ($N$ stages)**  
  $\dfrac{X_{N, B}}{X_{F, B}} = \dfrac{1}{(1 + \mathcal{E}/N)^N}$

- **Crosscurrent cascade ($\infty$ stages)**  
  $\dfrac{X_{\infty, B}}{X_{F, B}} = \dfrac{1}{\exp(\mathcal{E})}$

- **Countercurrent cascade ($N$ stages)**  
  $\dfrac{X_{R, B}}{X_{F, B}} = \left[\displaystyle\sum_{n = 0}^N \mathcal{E}^n\right]^{-1} = \dfrac{\mathcal{E} - 1}{\mathcal{E}^{N+1} - 1}$

- **Countercurrent cascade ($\infty$ stages)**  
  $\begin{cases} \dfrac{X_{\infty, B}}{X_{F, B}} = 0, & \mathcal{E} \in [1, \infty) \\ \dfrac{X_{\infty, B}}{X_{F, B}} = 1 - \mathcal{E}, & \mathcal{E} \in (-\infty, 1) \end{cases}$

- **Multistage arrangements of cocurrent, crosscurrent, and countercurrent. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p120, Figures 5.4.)** — Absorption and Stripping; Graphical method for trayed towers

Symbol Conventions

- **Molar flow rates**  
  $L$ - Total liquid feed  $V$ - Total gas feed  $L'$ - solute-free absorbent - constant at each stage  $V'$ - solute-free gas (carrier gas) - constant at each stage

- **Mole ratio of solute to solute-free absorbent**  
  $X$ - In the liquid  $Y$ - In the vapor

Equilibrium curve and operating lines of absorber and stripper. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p144, 146, Figures 6.9, 6.12.)

- **Construct the equilibrium curve from thermodynamics**  
  $K_n = \dfrac{y_n}{x_n} = \dfrac{Y_n}{X_n}\dfrac{1 + X_n}{1 + Y_n} \implies Y_n = \dfrac{K_n X_n}{1 + X_n - K_n X_n}$

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

- **Absorption operating line**  
  $Y_{n+1} = X_n \dfrac{L'}{V'} + Y_1 - X_0 \dfrac{L'}{V'}$

- **Absorbent flow rate**  
  $L' = V' \dfrac{Y_{N+1} - Y_1}{X_N - X_0}$

- **Minimum absorbent flow rate ($\infty$ stages)**  
  $L'_{\min} = V' K_N \cdot (\text{fraction solute absorbed})$

- **Absorption factor**  
  $\mathcal{A} = \dfrac{L}{K V}$

## Stripping

- **Stripping operating line**  
  $Y_{n} = X_n \dfrac{L'}{V'} + Y_0 - X_1 \dfrac{L'}{V'}$

- **Stripping agent flow rate**  
  $V' = L'\dfrac{X_{N} - X_1}{Y_N - Y_0}$

- **Minimum stripping agent flow rate ($\infty$ stages)**  
  $V'_{\min} = \dfrac{L'}{K_N} \cdot (\text{fraction solute stripped})$

- **Stripping factor**  
  $\mathcal{S} = \dfrac{V}{L}K$

- **Relating stripping factor and adsorption factor**  
  $\mathcal{S} = \dfrac{1}{\mathcal{A}}$

## Stage efficiency and packed columns

- **Overall stage efficiency**  
  $E_o = \dfrac{\text{\# theoretical stages}}{\text{\# actual stages}}$

- **Drickamer and Bradford correlation  ★ Hydrocarbons, $\mu_L \in (0.2, 1.6) \ \mathrm{cP}$**  
  $E_o [\%] = 19.2 - 57.8 \log(\mu_L)$

- **Height equivalent to a theoretical plate (HETP)**  
  $\mathrm{HETP} = \dfrac{l_T}{N_t} = \dfrac{\text{packed height}}{\text{\# equiv eqm stages}}$

- **Packed height**  
  $l_T = H_{OG}N_{OG}$

- **Overall height of a transfer unit (HTU)**  
  $H_{OG} = \dfrac{V}{K_y a A_c}$

- **Overall number of transfer unit (NTU)**  
  $N_{OG} = \displaystyle\int_{y_{\text{out}}}^{y_{\text{in}}}\dfrac{dy}{y - y^*}$

- **Overall volumetric mass transfer coefficient**  
  $K_y a$

- **Distillation of Binary Mixtures** — McCabe-Thiele graphical method for trayed towers

Symbol Conventions

- **Molar flow rates**  
  $F$ - Feed  $D$ - Distillate  $B$ - Bottoms  $L$ - Liquid in the rectifying section, Reflux  $V$ - Vapor in the rectifying section  $\overline{L}$ - Liquid in the stripping section  $\overline{V}$ - Vapor in the stripping section, Boilup

- **Mole fraction of the light key component**  
  $x$ - In the liquid  $y$ - In the vapor  $x_D$ - In the distillate  $x_B$ - In the bottoms

## Ratio

*Context:* $\alpha_{1, 2}$ - Relative volatility; $R$ - Reflux ratio; $V_B$ - Boilup ratio

- **McCabe-Thiele assumptions**  
  1. Equal and constant $\Delta H_{\text{vap}}$  2. Negligible $C_P \Delta T$ and $\Delta H_{\text{mix}}$  3. Insulated column $q = 0$  4. No pressure drop $\Delta P = 0$

- **Constant molar overflow in rectifying section**  
  $L_1 = L_i = L \\ V_1 = V_i = V$

- **Constant molar overflow in stripping section**  
  $\overline{L}_1 = \overline{L}_i = \overline{L} \\ \overline{V}_1 = \overline{V}_i = \overline{V}$

- **Non-equal flow rate in rectifying and stripping sections**  
  $L \not= \overline{L} \\ V \not= \overline{V}$

- **Reflux ratio**  
  $R = \dfrac{L}{D}$

- **Boilup ratio**  
  $V_B = \dfrac{\overline{V}}{B}$

- **Equilibrium curve**  
  $y_1 = \dfrac{\alpha_{1, 2}x_1}{1 + x_1(\alpha_{1, 2} - 1)}$

- **Rectifying section operating line**  
  $y = \left(\dfrac{R}{R + 1}\right)x + \left(\dfrac{x_D}{R + 1}\right)$

- **Stripping section operating line**  
  $y = \left(\dfrac{V_B + 1}{V_B}\right)x - \left(\dfrac{x_B}{V_B}\right)$

- **$q$-parameter**  
  $\begin{cases} q > 1 & \text{subcooled liq} \\ q = 1 & \text{saturated liq (bubble pt)} \\ q \in (0, 1) & \text{liq + vap} \\ q = 0 & \text{saturated vap (dew pt)} \\ q < 0 & \text{superheated vap} \end{cases}$

- **$q$-parameter**  
  $q = \dfrac{\overline{L} - L}{F} = 1 + \dfrac{\overline{V} - V}{F}$

- **$q$-line**  
  $y = \left(\dfrac{q}{q - 1}\right)x + \left(\dfrac{z_F}{q - 1}\right)$

## Limiting conditions

- **Total reflux  (Useless)**  
  $R_\infty = \infty \\ N_{\min} = 0 \\ L = V \\ D = B = 0$

- **Minimum reflux**  
  $R_{\min} = \dfrac{(L/V)_{\min}}{1 - (L/V)_{\min}} \\ N_\infty = \infty \\ V_{B, \min} = \dfrac{1}{(\overline{L}/\overline{V})_{\min} - 1}$

- **Perfect separation**  
  $x_D = 1, \quad x_B = 0 \\ R \ge R_{\min}  \begin{cases} R_{\min} = \dfrac{1}{z_F (\alpha_{1, 2} - 1)} & q = 1 \\ R_{\min} = \dfrac{\alpha_{1, 2}}{z_F (\alpha_{1, 2} - 1)} - 1 & q = 0 \end{cases}$

## Membrane Separations

*Context:* Equilibrium curve and operating lines of rectifying and stripping sections of distillation column. Optimal feed stage is indicated by the transition between operating lines on the equilibrium curve. (Separation Process Principles with Applications Using Process Simulators 4e by Seader p195, 196, 197, 200, Figures 7.5, 7.6, 7.7, 7.10.)

- **Transmembrane molar flux**  
  $\begin{aligned}N_i &= \dfrac{P_{M, i}}{l_M} \cdot (\text{driving force}) \\ &= \bar{P}_{M, i} \cdot (\text{driving force}) \end{aligned}$

- **Permeance**  
  $\bar{P}_{M, i} = \dfrac{P_{M, i}}{l_M}$

- **Permeability**  
  $P_{M, i} = \bar{P}_{M, i} l_M$

- **Selectivity**  
  $S_{i, j} = \dfrac{P_{M, i}}{P_{M, j}}$

- **Gas permeability unit**  
  $\begin{aligned}&1 \ \mathrm{barrer} \\ &= 10^{-10} \ \mathrm{cm^3_{STP} \cdot cm/(cm^2 \cdot s \cdot cmHg)} \\ &= 3.35 \times 10^{-16} \ \mathrm{mol \cdot m / (m^2 \cdot s \cdot Pa)} \\ &= 5.58 \times 10^{-12} \ \mathrm{lbmol \cdot ft / (ft^2 \cdot h \cdot psi)}\end{aligned}$

- **Mole of gas in standard temperature and pressure (STP)**  
  $1 \ \mathrm{mol} \sim 22.4 \ \mathrm{L_{STP}}$

## Transport through porous membranes

*Context:* Bulk flow

- **Hagen-Poiseuille flow  ★ Laminar flow $\mathrm{Re} < 2100$**  
  $v = \dfrac{D^2}{32\mu L}(P_0 - P_L)$

- **Pore number density**  
  $n = \dfrac{n_\text{total}}{A_c} = \dfrac{\text{total \# of pores}}{\text{membrane cross sectional area}}$

- **Porosity (void fraction)  ★ Straight cylindrical pore**  
  $\varepsilon = \frac{1}{4}n\pi D^2$

- **Bulk flow flux  ★ Straight cylindrical pore**  
  $\begin{aligned}N &= v\rho\varepsilon \\ &= \dfrac{\varepsilon\rho D^2}{32 \mu l_M} (P_0 - P_L) \\ &= \dfrac{n\pi\rho D^4}{128 v l_M}(P_0 - P_L)\end{aligned}$

- **Empirical hydraulic diameter**  
  $d_H = \dfrac{4\varepsilon}{a_v}$

- **Specific surface area**  
  $a_v = \dfrac{a}{1 - \varepsilon}$

- **Total pore surface area**  
  $a = a_v (1 - \varepsilon)$

- **Tortuosity correction of membrane width**  
  $\tau l_M$

- **Bulk flow flux  ★ General pore**  
  $N = \dfrac{\rho\varepsilon^2}{2(1-\varepsilon)^2 \tau a_v^2 \mu l_M}(P_0 - P_L)$

- **Ergun equation**  
  $\dfrac{P_0 - P_L}{l_M} = \dfrac{150 \mu v_0 (1-\varepsilon)^2}{D_P^2 \varepsilon^3} + \dfrac{1.75 \rho v_0^2 (1 - \varepsilon)}{D_P \varepsilon^3}$

- **Mean spherical particle diameter**  
  $D_P = \dfrac{6}{a_v}$

## Liquid diffusion

- **Concentration driving force**  
  $\Delta c \not= 0 \\ \Delta P = 0$

- **Transmembrane mass flux**  
  $N_i = \dfrac{D_{e, i}}{l_M}(c_{i, 0} - c_{i, L})$

- **Effective diffusivity**  
  $D_{e, i} = \dfrac{\varepsilon D_i}{\tau} K_{r, i}$

- **Restrictive factor of solute**  
  $K_r = \left[ 1 - \dfrac{d_m}{d_p}\right]^4$

- **Selectivity**  
  $S_{i, j} = \dfrac{D_i K_{r, i}}{D_j K_{r, j}}$

## Gas diffusion

- **Transmembrane molar flux  ★ Ideal gas, uniform transmembrane T, P**  
  $\begin{aligned} N_i &= \dfrac{c_M}{P}\dfrac{D_{e, i}}{l_M}(P_{i, 0} - P_{i, L}) \\ &= \dfrac{1}{RT}\dfrac{D_{e, i}}{l_M}(P_{i, 0} - P_{i, L}) \end{aligned}$

- **Effective diffusivity**  
  $D_{e, i} = \dfrac{\varepsilon}{\tau} \left[\dfrac{1}{(1/D_i) + (1/D_{K, i})}\right]$

- **Knudsen diffusivity of straight cylindrical pore  ★ Kinetic theory of gas**  
  $D_{K, i} \ [\mathrm{cm/s}] = 4850 d_p \ [\mathrm{cm}] \sqrt{\dfrac{T}{\mathcal{M}_i}\dfrac{[\mathrm{K}]}{[\mathrm{g/mol}]}}$

- **Selectivity of Knudsen diffusion  ★ $D_i \gg D_{K, i}$  ★ $D_{e, i} \sim D_{K, i}$**  
  $S_{i, j} = \dfrac{P_{M, i}}{P_{M, j}} = \sqrt{\dfrac{\mathcal{M}_j}{\mathcal{M}_i}}$

## Transport through nonporous (dense) membranes

*Context:* Solution-diffusion of liquid mixtures

- **Thermodynamic equilibrium partition coefficient**  
  $K_i = \dfrac{c_i}{c_i'}$

- **Transmembrance mass flux  ★ Fick’s law**  
  $N_i = \dfrac{D_i}{l_M}(c_{i, 0} - c_{i, L})$

- **Transmembrance mass flux  ★ $K_{i, 0} = K_{i, L} = K_{i}$**  
  $N_i = \dfrac{K_i D_i}{l_M}(c'_{i, 0} - c'_{i, L})$

- **Transmembrance mass flux  ★ No mass transfer resistance in fluid boundary layers  ★ $c'_{i, 0} = c_{i, F}$ and $c'_{i, L} = c_{i, P}$**  
  $N_i = \dfrac{K_i D_i}{l_M}(c_{i, F} - c_{i, P})$

## Solution-diffusion of gas mixtures

- **Henry’s constant**  
  $H_i = \dfrac{c_i}{P_i}$

- **Transmembrance mass flux  ★ Fick’s law**  
  $N_i = \dfrac{D_i}{l_M}(c_{i, 0} - c_{i, L})$

- **Transmembrance mass flux  ★ $H_{i, 0} = H_{i, L} = H_{i}$**  
  $N_i = \dfrac{H_i D_i}{l_M}(P_{i, 0} - P_{i, L})$

- **Transmembrance mass flux  ★ No mass transfer resistance in external boundary layers  ★ $P_{i, 0} = P_{i, F}$ and $P_{i, L} = P_{i, P}$**  
  $N_i = \dfrac{H_i D_i}{l_M}(P_{i, F} - P_{i, P})$

## Separation factor

- **Ideal separation factor  ★ Downstream permeate pressure negligible compared to upstream feed pressure  ★ $x_{i, P} P_P \ll x_{i, F} P_F$ and $x_{j, P} P_P \ll x_{j, F} P_F$**  
  $\alpha^*_{i, j} = \dfrac{H_i D_i}{H_j D_j} = \dfrac{P_{M, i}}{P_{M, j}}$

- **Separation factor**  
  $\alpha_{i, j} = \alpha^*_{i, j} \left[\dfrac{(x_{j, F} / x_{j, P}) - r\alpha_{i, j}}{(x_{j, F} / x_{j, P}) - r}\right]$

- **Cut (fraction of feed permeated)**  
  $\theta = \dfrac{\dot{n}_P}{\dot{n}_F}$

Summary of transport through membranes

- **Type of transport** — Permselective; Membrane Type; Driving Force; Permeability

- **(L) Bulk flow**  
  No  Macroporous  $\Delta P$  $\begin{aligned}P_M = \dfrac{\rho\varepsilon^3}{2(1 - \varepsilon)^2 \tau a_v^2 \mu}\end{aligned}$

- **(L) Molecular diffusion**  
  Yes  Microporous  $\Delta c$  $P_M = D_{e, i} = \dfrac{\varepsilon D_i K_{r, i}}{\tau}$

- **(G) Molecular diffusion  ★ high P  ★ $d_p > d_m$**  
  Yes  Microporous  $\Delta P_i \\ \Delta P = 0$  $P_{M, i} = \dfrac{D_{e, i}}{RT}$

- **(G) Knudsen diffusion  ★ low P  ★ $d_p \sim d_m$**  
  Yes  Microporous  $\Delta P_i \\ \Delta P = 0$  $P_{M, i} = \dfrac{D_{e, i}}{RT}$

- **(L) Solution diffusion**  
  Yes  Nonporous (dense)  $\Delta c$  $P_{M, i} = K_i D_i$

- **(G) Solution diffusion**  
  Yes  Nonporous (dense)  $\Delta P_i \\ \Delta P = 0$  $P_{M, i} = H_i D_i$

## Reverse osmosis

- **Osmotic pressure  ★ Equilibrium**  
  $\Pi \equiv P_1 - P_{\ce{H2O}}$

- **Osmotic pressure of water**  
  $\Pi_{\ce{H2O}} = 0$

- **Osmotic process**  
  $P_1 - P_{\ce{H2O}} < \Pi$

- **Reverse osmotic process**  
  $P_1 - P_{\ce{H2O}} > \Pi$

- **Osmotic pressure’s thermodynamic derivation  ★ Between pure water and solution  ★ Solvent $A$, solute $B$**  
  $\Pi = -\dfrac{RT}{v_{A}} \ln(x_A \gamma_A)$

- **Osmotic pressure  ★ Ideal solution, dilute $B$**  
  $\Pi = \dfrac{RT n_B}{v_A} = \dfrac{RTc_B}{\mathcal{M}_B}$

## Seawater reverse osmosis

- **Seawater as solution 1; salt as solute B**  
  $\ce{A} = \text{water} = \ce{H2O} \\ \ce{B} = \text{salt} = \ce{S}$

- **Molar mass**  
  $\mathcal{M} = \dfrac{m}{n}$

- **Molarity (molar concentration)**  
  $M = \dfrac{n}{V} = \dfrac{\mathrm{wt \% \ S}}{100 \% - \mathrm{wt \% \ S}}\dfrac{\rho_{\ce{H2O}}}{\mathcal{M}_S}$

- **Seawater osmotic pressure correlation**  
  $\Pi \ [\mathrm{psia}] = 1.12 T \ [\mathrm{K}] \sum M_i \ [\mathrm{mol/L}]$

- **Transmembrane molar flux of water (solvent A)**  
  $N_{\ce{H2O}} = \dfrac{P_{M, \ce{H2O}}}{l_M} (\Delta P - \Delta \pi)$

- **Salt passage**  
  $\mathrm{SP} = \dfrac{c_{S, P}}{c_{S, F}}$

- **Salt rejection**  
  $\mathrm{SR} = 1 - \mathrm{SP}$

- **Concentration polarization factor**  
  $\Gamma \equiv \dfrac{c_{S, i} - c_{S, F}}{c_{S, F}} = \dfrac{N_{\ce{H2O}} (\mathrm{SR})}{k_S}$

- **Significant concentration polarization**  
  $\Gamma > 0.2$

