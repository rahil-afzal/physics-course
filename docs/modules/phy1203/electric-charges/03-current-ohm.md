# Current, Resistance, and Ohm's Law

## Electric Current

!!! info "Definition: Electric Current"
    Current is the rate of charge flow:
    \[
    I = \frac{\Delta Q}{\Delta t}
    \qquad [I] = \text{Ampere (A)} = \text{C/s}
    \]
    **Conventional current** flows in the direction positive charges move (from high to low potential). In biological systems, current is carried by ions (not electrons), moving through aqueous solution and ion channels.

!!! note "Note: Biological Current Magnitudes"
    Biological currents are tiny by household standards but enormous at the single-channel level:

    | Biological event | Current |
    |---|---|
    | Single ion channel (open) | \(\sim 1\)–\(10\ \text{pA}\) |
    | Axon action potential | \(\sim 1\)–\(100\ \text{nA}\) |
    | Cardiac pacemaker cell | \(\sim 1\ \mu\text{A}\) |
    | Whole-heart ECG surface current | \(\sim 1\ \text{mA}\) |

## Resistance and Ohm's Law

!!! success "Result: Resistance and Ohm's Law"
    The resistance of a conductor of length \(L\), cross-section \(A\), and resistivity \(\rho\) (a material property):
    \[
    R = \rho\frac{L}{A}
    \qquad [R] = \Omega\ (\text{ohm})
    \]
    Ohm's Law (for ohmic, i.e., linear, conductors):
    \[
    V = IR
    \]

!!! tip "Analogy: Water Pipe Analogy — The Complete Picture"
    The water pipe analogy is the most powerful tool for intuition:

    | Electrical | Hydraulic |
    |---|---|
    | Voltage \(V\) (V) | Pressure difference (Pa) |
    | Current \(I\) (A) | Flow rate (m\(^3\)/s) |
    | Resistance \(R\) (\(\Omega\)) | Fluidic resistance |
    | Capacitance \(C\) (F) | Elastic reservoir |
    | Charge \(Q\) (C) | Volume of water |
    | Conductor wire | Wide pipe (low resistance) |
    | Thin wire / resistor | Narrow pipe (high resistance) |
    | Open switch | Closed valve |
    | Battery | Pump |

    Ohm's law \(V = IR\) is perfectly analogous to Poiseuille's law \(\Delta P = Q \cdot R_{\text{fluid}}\) from the fluid mechanics chapter.

!!! question "Biological Connection: Ion Channels as Resistors"
    Each type of ion channel has a characteristic **conductance** \(g = 1/R\) (siemens, S). A typical single channel has \(g \approx 10\)–\(100\ \text{pS}\).

    - **Closed channel** \(\equiv\) infinite resistance / zero conductance.
    - **Open channel** \(\equiv\) finite resistance, allowing ion flow.
    - The more channels open, the lower the total membrane resistance, and the larger the current for a given driving voltage.
    - Drugs that block channels (e.g. tetrodotoxin blocks Na\(^+\) channels) increase membrane resistance and prevent action potentials — used as a model toxin in neuroscience research.

## Kirchhoff's Laws and Circuit Analysis

!!! success "Result: Kirchhoff's Laws"
    **Kirchhoff's Current Law (KCL)**: conservation of charge —
    \[
    \sum I_\text{in} = \sum I_\text{out} \qquad \text{at any junction}
    \]
    **Kirchhoff's Voltage Law (KVL)**: conservation of energy —
    \[
    \sum_{\text{loop}} V = 0 \qquad \text{around any closed loop}
    \]

!!! tip "Analogy: KCL as a River Junction"
    At a river confluence (junction), the total water flowing in equals the total flowing out — water doesn't pile up at the junction. This is KCL: charge doesn't accumulate at a node (under steady state). At a river fork (branching axon), the flow splits between branches according to their widths (conductances).

!!! success "Result: Series and Parallel Resistance"
    **Series:** \(R_\text{eq} = R_1 + R_2 + \cdots\) (same current through each; voltages add)

    **Parallel:** \(\dfrac{1}{R_\text{eq}} = \dfrac{1}{R_1} + \dfrac{1}{R_2} + \cdots\) (same voltage across each; currents add)

!!! example "Example: Worked Circuit — Kirchhoff's Laws"
    A 12 V battery drives current through \(R_1 = 100\ \Omega\) in series with \(R_2 = 150\ \Omega\) and \(R_3 = 300\ \Omega\) in parallel.

    **Step 1 — Parallel combination:**
    \[
    \frac{1}{R_{23}} = \frac{1}{150} + \frac{1}{300} = \frac{2}{300} + \frac{1}{300}
    = \frac{3}{300} \;\Rightarrow\; R_{23} = 100\ \Omega
    \]
    **Step 2 — Total resistance:**
    \[
    R_\text{eq} = R_1 + R_{23} = 100 + 100 = 200\ \Omega
    \]
    **Step 3 — Total current (KVL on outer loop):**
    \[
    I_1 = \frac{V}{R_\text{eq}} = \frac{12}{200} = 0.06\ \text{A} = 60\ \text{mA}
    \]
    **Step 4 — Branch currents (KCL at node):** voltage across parallel pair: \(V_{23} = I_1 \times R_{23} = 0.06\times100 = 6\ \text{V}\)
    \[
    I_2 = \frac{V_{23}}{R_2} = \frac{6}{150} = 0.04\ \text{A}, \qquad
    I_3 = \frac{V_{23}}{R_3} = \frac{6}{300} = 0.02\ \text{A}
    \]
    **Check KCL:** \(I_2 + I_3 = 0.04 + 0.02 = 0.06 = I_1\ \checkmark\)

!!! question "Biological Connection: KCL at an Axon Branch Point"
    When a nerve axon branches into two daughter fibres at a node, the ionic current carried by the action potential must split between the two branches according to their conductances (inverse resistances). A thicker axon (lower \(R\)) carries more current. If one branch has much higher resistance (e.g. a thin branch to a small muscle fibre), it receives less current — Kirchhoff's current law determines exactly how much current each branch receives, and therefore whether the action potential can propagate into that branch at all.

## RC Circuits and Bioelectric Membranes

!!! info "Definition: RC Circuit"
    A resistor \(R\) in series with a capacitor \(C\) connected to a voltage source \(V_0\). The voltage across the capacitor changes exponentially, governed by the **time constant** \(\tau = RC\).

!!! success "Result: RC Charging and Discharging"
    **Charging:**
    \[
    V_C(t) = V_0\!\left(1 - e^{-t/RC}\right)
    \]
    **Discharging:**
    \[
    V_C(t) = V_0\,e^{-t/RC}
    \]
    At \(t = \tau\): \(V_C \approx 63\%\) of final value (charging) or \(37\%\) remaining (discharging). After \(5\tau\), the capacitor is considered fully charged/discharged (\(>99\%\)).

!!! tip "Analogy: RC Charging as Filling a Leaky Bucket"
    Imagine filling a bucket (capacitor) with water from a tap through a narrow nozzle (resistor). At first, water rushes in quickly (large current) because the bucket is empty. As the bucket fills, back-pressure builds and the flow slows. Eventually the flow almost stops — the bucket is "charged." Pull out the plug (discharge) and the bucket empties fast at first, then slower. The narrower the nozzle (\(R\)), or the larger the bucket (\(C\)), the slower the process — the larger \(\tau = RC\).

!!! question "Biological Connection: Neuron Membrane — A Biological RC Circuit"
    The neuron membrane combines resistance (ion channels, \(R_m\)) and capacitance (lipid bilayer, \(C_m\)) in a parallel RC arrangement. The membrane time constant:
    \[
    \tau_m = R_m C_m
    \]
    determines how quickly the membrane potential responds to a stimulus.

    For a typical neuron: \(R_m = 40\ \text{M}\Omega\), \(C_m = 200\ \text{pF}\):
    \[
    \tau_m = 40\times10^6 \times 200\times10^{-12} = 8\times10^{-3}\ \text{s} = 8\ \text{ms}
    \]
    A stimulus briefer than \(\sim\tau_m\) is "blurred out" by the membrane capacitance. Fast-signalling interneurons have small \(\tau_m\) (by reducing \(R_m\) through more open channels); integrating neurons have large \(\tau_m\) (to average inputs over time).

    **Clinical relevance:** General anaesthetics partially block Na\(^+\) channels (\(\uparrow R_m \Rightarrow \uparrow \tau_m\)), slowing neuronal response and suppressing consciousness.

## Ohmic Current and the Nernst Potential

The current through an ion channel is not simply \(V/R\). What matters is not the membrane potential alone, but how far the membrane potential is from the *equilibrium potential* of that particular ion.

!!! success "Result: Ohmic Current Through an Ion Channel"
    \[
    I_x = g_x\,(V_m - E_x)
    \]
    | Symbol | Meaning |
    |---|---|
    | \(I_x\) | current of ion \(x\) (A); positive = outward current |
    | \(g_x\) | membrane conductance for ion \(x\) (S = A/V = siemens) |
    | \(V_m\) | membrane potential (V) |
    | \(E_x\) | Nernst (equilibrium) potential for ion \(x\) (V) |

!!! tip "Analogy: Driving Force as Net Pressure"
    Think of ion current like water through a pipe where both a pump (concentration gradient) and gravity (electrical gradient) are acting. If the pump exactly cancels gravity, there is no net flow — this is the equilibrium potential \(E_x\). The quantity \((V_m - E_x)\) is the **driving force**: positive driving force pushes current out; negative pushes it in. Opening more channels (increasing \(g_x\)) amplifies whichever direction the driving force dictates.

!!! note "Note: Sign Convention and Current Direction"
    - If \(V_m > E_x\): driving force is positive, ion \(x\) current is outward (leaving the cell, conventionally positive for a positive ion).
    - If \(V_m < E_x\): driving force is negative, ion \(x\) current is inward.
    - If \(V_m = E_x\): driving force is zero; **no net current** even if many channels are open.

    This is why Na\(^+\) channels, once open during an action potential, drive the membrane toward \(E_{\text{Na}} \approx +60\ \text{mV}\) and then current stops — it cannot overshoot the Nernst potential.

### The Nernst Potential

!!! abstract "Derivation: Why the Nernst Potential Exists"
    An ion \(X\) is at equilibrium when two opposing tendencies exactly cancel:

    1. **Concentration gradient:** ion \(X\) diffuses from high \([X]\) to low \([X]\) (random thermal motion).
    2. **Electrical gradient:** the membrane voltage creates an electric force opposing diffusion (since the diffusing ion carries charge).

    At equilibrium the electrochemical potential is equal on both sides. Setting the entropy-driven diffusion energy equal to the electrical work gives the Nernst equation.

!!! success "Result: Nernst Equation"
    \[
    E_x = \frac{RT}{zF}\ln\frac{[X]_\text{out}}{[X]_\text{in}}
    \]
    | Symbol | Meaning |
    |---|---|
    | \(R = 8.314\ \text{J/(mol\,K)}\) | gas constant |
    | \(T\) | absolute temperature (K) |
    | \(z\) | ionic valence (e.g. \(+1\) for K\(^+\), \(-1\) for Cl\(^-\), \(+2\) for Ca\(^{2+}\)) |
    | \(F = 96{,}485\ \text{C/mol}\) | Faraday constant |

    At body temperature (\(T = 310\ \text{K}\)), \(RT/F \approx 26.7\ \text{mV}\), so:
    \[
    E_x \approx \frac{26.7}{z}\ln\frac{[X]_\text{out}}{[X]_\text{in}}\ \text{mV}
    \qquad \text{or} \qquad
    \frac{61.5}{z}\log_{10}\frac{[X]_\text{out}}{[X]_\text{in}}\ \text{mV}
    \]

!!! example "Example: Nernst Potentials for Key Ions at 310 K"
    Using the intracellular and extracellular concentrations from the ion table in the Charges chapter:

    **Potassium K\(^+\) (\(z=+1\)):**
    \[
    E_K = 26.7\ln\frac{5}{140} = 26.7\times(-3.332) \approx -89\ \text{mV}
    \]
    **Sodium Na\(^+\) (\(z=+1\)):**
    \[
    E_{\text{Na}} = 26.7\ln\frac{145}{12} = 26.7\times 2.493 \approx +67\ \text{mV}
    \]
    **Chloride Cl\(^-\) (\(z=-1\)):**
    \[
    E_{\text{Cl}} = \frac{26.7}{-1}\ln\frac{116}{4} = -26.7\times 3.367 \approx -90\ \text{mV}
    \]
    **Calcium Ca\(^{2+}\) (\(z=+2\)):**
    \[
    E_{\text{Ca}} = \frac{26.7}{2}\ln\frac{2}{0.0001} = 13.35\times 9.903 \approx +132\ \text{mV}
    \]

    The resting membrane potential (\(-70\ \text{mV}\)) lies between \(E_K\) and \(E_{\text{Na}}\), pulled toward \(E_K\) by the high resting K\(^+\) permeability.

![Nernst potentials for K+, Cl-, Na+, and Ca2+ compared to the resting membrane potential](assets/nernst-chart.png)

!!! question "Biological Connection: Goldman Equation — Extending the Nernst Equation"
    The resting membrane potential is not set by a single ion but by all permeable ions simultaneously. The **Goldman–Hodgkin–Katz (GHK) equation** generalises the Nernst equation:
    \[
    V_m = \frac{RT}{F}\ln
    \frac{P_K[K^+]_o + P_{Na}[Na^+]_o + P_{Cl}[Cl^-]_i}
    {P_K[K^+]_i + P_{Na}[Na^+]_i + P_{Cl}[Cl^-]_o}
    \]
    where \(P_x\) is the permeability of ion \(x\). At rest, \(P_K \gg P_{Na}\), so \(V_m \approx E_K\). During an action potential, Na\(^+\) channels open, \(P_{Na}\) surges, and \(V_m\) shifts rapidly toward \(E_{Na} \approx +67\ \text{mV}\). This is the physical basis of the depolarisation phase — covered in full in the next chapter.

## Practice Problems

**5. Circuit Analysis (KCL/KVL).** A 12 V battery, \(R_1 = 100\ \Omega\) in series, \(R_2 = 150\ \Omega\) and \(R_3 = 300\ \Omega\) in parallel. Find total current, branch currents, and voltage drop across \(R_1\).

**6. RC Time Constant.** A neuron has \(R_m = 20\ \text{M}\Omega\) and \(C_m = 0.5\ \mu\text{F}\).

(a) Calculate \(\tau\).
(b) What fraction of the final voltage is reached after \(t = 2\tau\)?
(c) After how long (in \(\tau\)) is 95% of the final voltage reached?

**7. Power Dissipation.** An ion channel carries a current \(I = 50\ \text{pA}\) at a driving force of \(V_m - E_x = -65\ \text{mV}\). Calculate the power dissipated.

**8. Nernst Potential.** Calculate the Nernst potential for K\(^+\) at \(T = 310\ \text{K}\), given \([\text{K}^+]_{\text{in}} = 140\ \text{mM}\) and \([\text{K}^+]_{\text{out}} = 5\ \text{mM}\).

**9. Nernst Potential — Calcium.** Ca\(^{2+}\) has \([\text{Ca}^{2+}]_{\text{in}} = 0.0001\ \text{mM}\) and \([\text{Ca}^{2+}]_{\text{out}} = 2\ \text{mM}\) at \(T = 310\ \text{K}\). Calculate \(E_{\text{Ca}}\).

**10. Ohmic Current.** A membrane has K\(^+\) conductance \(g_K = 5\ \text{nS}\) and \(E_K = -90\ \text{mV}\). If \(V_m = -70\ \text{mV}\):

(a) Calculate \(I_K\).
(b) State the direction of K\(^+\) current (inward or outward).

**11. Parallel Resistance Network.** Three ion channel types have conductances \(g_1 = 10\ \text{nS}\), \(g_2 = 5\ \text{nS}\), \(g_3 = 2\ \text{nS}\). They are all open simultaneously. Find the total membrane conductance and total resistance \(R_m\).

**12. Conceptual.** The Nernst potential for K\(^+\) is \(\approx -90\ \text{mV}\) and for Na\(^+\) is \(\approx +67\ \text{mV}\). The resting membrane potential is \(\approx -70\ \text{mV}\). Which ion is closer to equilibrium at rest? What does this imply about which ion carries most of the resting current?

**13. Conceptual.** Describe how Kirchhoff's current law applies to a branching axon. If one branch has twice the diameter of the other, how does this affect the fraction of current entering each branch?

**14. Conceptual.** A patient is given a drug that increases membrane resistance \(R_m\) tenfold while leaving \(C_m\) unchanged. How does the membrane time constant \(\tau_m\) change? How does this affect the neuron's ability to follow rapidly changing inputs?
