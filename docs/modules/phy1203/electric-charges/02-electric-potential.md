# Capacitance and the Membrane as a Capacitor

!!! info "Definition: Capacitance"
    A capacitor stores electric charge on two conducting surfaces separated by an insulator (dielectric). Capacitance \(C\) is defined as:
    \[
    C = \frac{Q}{V}, \qquad [C] = \text{Farad (F)}
    \]
    For a parallel-plate capacitor of plate area \(A\), plate separation \(d\), and permittivity \(\varepsilon = \varepsilon_0\varepsilon_r\):
    \[
    C = \varepsilon\frac{A}{d} = \varepsilon_0\varepsilon_r\frac{A}{d}
    \]
    where \(\varepsilon_0 = 8.85\times10^{-12}\ \text{F/m}\) and \(\varepsilon_r\) is the relative permittivity of the insulating material.

!!! tip "Analogy: Capacitor as a Water Tank"
    Think of a capacitor as a water tank with a rubber membrane stretched across the middle. Water (charge) can accumulate on one side, stretching the membrane and building up pressure (voltage). The bigger the tank (larger \(A\)), the more water it holds at the same pressure — larger capacitance. The thicker the membrane (larger \(d\)), the harder it is to stretch — smaller capacitance.

!!! success "Result: Energy Stored in a Capacitor"
    \[
    U = \frac{1}{2}CV^2 = \frac{Q^2}{2C} = \frac{1}{2}QV
    \]
    All three forms are equivalent; use whichever variables are given.

!!! question "Biological Connection: The Cell Membrane as a Capacitor"
    The cell membrane is a phospholipid bilayer approximately 5–7 nm thick. On either side are conducting ionic solutions (cytoplasm inside, extracellular fluid outside). This is a textbook parallel-plate capacitor:

    - **Conductors:** intracellular and extracellular fluid.
    - **Insulator:** the hydrophobic lipid bilayer (\(\varepsilon_r \approx 2\)).
    - **Plate separation:** \(d \approx 5\ \text{nm}\).
    - **Specific capacitance:** \(\approx 1\ \mu\text{F/cm}^2\), remarkably consistent across almost all cell types, suggesting it is set by the universal bilayer structure.

    **Why does capacitance matter for neurons?** When a voltage pulse arrives, the neuron must *charge* its membrane capacitor before the voltage can change. A larger membrane (more area \(A\)) has larger \(C\), requiring more charge to change \(V_m\) by the same amount — so large neurons respond more slowly. Myelination dramatically reduces effective \(C\) by increasing \(d\) (the myelin wrapping is a thick insulator), allowing rapid signal propagation.

!!! example "Example: Membrane Capacitance Calculation"
    A spherical cell of radius \(r = 10\ \mu\text{m}\) has membrane area
    \[
    A = 4\pi r^2 = 4\pi(10^{-5})^2 = 1.26\times10^{-9}\ \text{m}^2 = 1.26\times10^{-5}\ \text{cm}^2.
    \]
    With specific capacitance \(c_m = 1\ \mu\text{F/cm}^2\):
    \[
    C_m = c_m \times A = 1\times10^{-6} \times 1.26\times10^{-5}
    = 1.26\times10^{-11}\ \text{F} = 12.6\ \text{pF}
    \]
    Energy stored at resting potential \(V_m = 70\ \text{mV}\):
    \[
    U = \tfrac{1}{2}C_m V_m^2 = \tfrac{1}{2}(1.26\times10^{-11})(0.07)^2
    \approx 3.1\times10^{-14}\ \text{J}
    \]
    This tiny energy must be restored after every action potential by the ATP-powered Na\(^+\)/K\(^+\) pump.

## Practice Problems

**3. Membrane Capacitance.** A spherical cell of radius \(r = 10\ \mu\text{m}\) has specific membrane capacitance \(c_m = 1\ \mu\text{F/cm}^2\).

(a) Calculate the total membrane capacitance \(C_m\).
(b) How much charge \(Q\) is stored at resting potential \(V_m = 70\ \text{mV}\)?
(c) Calculate the energy stored \(U\).

**4. Conceptual.** Why do membranes act as capacitors? Explain in terms of the physical structure of the lipid bilayer. What would happen to the capacitance if the bilayer became thinner (as in some genetic disorders)?