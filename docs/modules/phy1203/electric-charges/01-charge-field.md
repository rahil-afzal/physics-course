# Electric Charge and Coulomb's Law

## Why Electricity is the Language of Life

Before the 19th century, "electricity" and "life" were thought to be entirely separate domains of nature. Luigi Galvani's famous 1780 experiment — a dissected frog's leg twitching when touched with two different metals — shattered that boundary forever. We now know that **every cell in your body is an electrical device**.

Consider: your heart beats because of an electrical signal that sweeps across cardiac muscle 60–100 times per minute. Your brain processes information using electrical impulses travelling at up to 120 m/s along nerve fibres. Every muscle contraction, every sensory perception, every hormone release is ultimately triggered by an electrical event at a cell membrane. Even DNA replication depends on the electrostatic forces between charged molecules.

This chapter covers the physical principles of electricity — charge, fields, potential, current, resistance, capacitance, and circuits — and connects each concept directly to the biological systems that exploit them.

## Electric Charge

!!! info "Definition: Electric Charge"
    Electric charge is a fundamental property of matter. It comes in two types: **positive** (protons, \(+e\)) and **negative** (electrons, \(-e\)). Like charges repel; unlike charges attract. The elementary charge is \(e = 1.602\times10^{-19}\ \text{C}\) (coulombs).

Charge is *conserved*. It can be transferred between objects but never created or destroyed. This is why the total charge inside a living cell remains constant even as ions rush in and out through channels.

| Ion | Charge | Inside cell (mM) | Outside cell (mM) |
|---|---|---|---|
| Na\(^+\) | \(+e\) | 12 | 145 |
| K\(^+\) | \(+e\) | 140 | 5 |
| Cl\(^-\) | \(-e\) | 4 | 116 |
| Ca\(^{2+}\) | \(+2e\) | 0.0001 | 2 |

These *gradients* of charge across the cell membrane are the source of all bioelectrical phenomena.

## Coulomb's Law

!!! success "Result: Coulomb's Law"
    The electrostatic force between two point charges \(q_1\) and \(q_2\) separated by distance \(r\):
    \[
    F = k_e \frac{|q_1 q_2|}{r^2}
    \qquad k_e = 8.99\times10^9\ \text{N\,m}^2/\text{C}^2
    \]
    Attractive if the charges are opposite; repulsive if they are the same sign. Force falls as \(1/r^2\) — the same inverse-square law as gravity.

!!! tip "Analogy: Gravity vs. Electrostatics"
    Coulomb's law and Newton's gravity law are structurally identical: \(F = Gm_1m_2/r^2\) vs. \(F = k_e q_1 q_2/r^2\). The key difference: gravity is always attractive; electrostatic forces can be either attractive or repulsive. Also, \(k_e \approx 10^{40}\) times larger than \(G\), meaning the electric force between a proton and electron is \(\sim10^{39}\) times stronger than their gravitational attraction. Atoms are held together by electricity, not gravity.

!!! example "Example: Force Between Ions"
    A Na\(^+\) ion (\(q_1 = +e\)) and Cl\(^-\) ion (\(q_2 = -e\)) are separated by \(r = 0.28\ \text{nm}\) (typical ionic bond length in NaCl crystal):
    \[
    F = k_e \frac{e^2}{r^2}
    = \frac{8.99\times10^9 \times (1.6\times10^{-19})^2}{(2.8\times10^{-10})^2}
    \approx 2.94\times10^{-9}\ \text{N}
    \]
    This \(\approx 3\ \text{nN}\) force is small in everyday terms, but it is enormous relative to the mass of an ion (producing accelerations \(\sim 10^{18}\ \text{m/s}^2\)). It is this force that drives ions through open channels and holds protein structures together.

!!! question "Biological Connection: Electrostatics in Molecular Biology"
    - **Protein folding.** Oppositely charged amino acid side-chains form "salt bridges" — electrostatic bonds that stabilise the 3-D fold. Disrupting them (e.g., by changing pH, which alters charge states) causes protein denaturation.
    - **DNA double helix.** The phosphate groups on DNA's backbone carry a negative charge. The double helix is therefore strongly anionic; positively charged histone proteins wrap around it to compact it into chromatin.
    - **Enzyme–substrate binding.** Many enzymes use positively charged residues in their active site to attract negatively charged substrates.
    - **Drug design.** Drugs are often designed with specific charge distributions to dock electrostatically with their target protein.

## Electric Field

!!! info "Definition: Electric Field"
    The electric field \(\vec{E}\) at a point in space is the force per unit positive test charge placed at that point:
    \[
    \vec{E} = \frac{\vec{F}}{q}, \qquad |\vec{E}| = k_e\frac{|Q|}{r^2}
    \]
    Units: V/m (volts per metre) \(=\) N/C. Direction: outward from positive charges, inward toward negative charges.

!!! tip "Analogy: Field Lines as a Map"
    Think of the electric field like a topographic map of a hillside. The hill (positive charge) pushes a ball (positive test charge) outward in all directions; a valley (negative charge) pulls it inward. Field lines show the direction a positive charge would naturally move from high electric potential (hilltop) to low (valley). Where lines are dense, the field is strong; where they are sparse, it is weak.

## Electric Potential

!!! success "Result: Electric Potential and Potential Difference"
    Electric potential \(V\) at a distance \(r\) from a point charge \(Q\):
    \[
    V = k_e\frac{Q}{r}
    \]
    Units: Volts (V = J/C). The **potential difference** \(\Delta V = V_B - V_A\) between two points is the work done per unit charge moving a positive charge from \(A\) to \(B\). A positive charge moves naturally from high to low potential (downhill); a negative charge moves from low to high.

!!! tip "Analogy: Potential as Electrical Height"
    Electric potential is exactly analogous to gravitational height. A ball rolls downhill (from high gravitational PE to low). A positive ion drifts toward lower electric potential; a negative ion drifts toward higher potential. The membrane potential \(V_m \approx -70\ \text{mV}\) means the inside of the cell is 70 mV "lower" (more negative) than the outside — a valley for positive ions, pulling them inward through any open channel.

!!! question "Biological Connection: Membrane Potential"
    The resting membrane potential of a typical neuron is \(V_m \approx -70\ \text{mV}\). This arises from the combined effect of:

    - The **concentration gradient** of ions (especially K\(^+\) high inside, Na\(^+\) high outside).
    - The **electrical gradient** pulling ions opposite to their concentration gradient.
    - The **Na\(^+\)/K\(^+\)-ATPase pump** that actively restores gradients, consuming 1 ATP to move 3 Na\(^+\) out and 2 K\(^+\) in — net outward positive charge, maintaining the negative resting potential.

    At rest, the membrane is most permeable to K\(^+\) (through leak channels), so \(V_m\) is close to but slightly above the K\(^+\) Nernst potential of \(-90\ \text{mV}\).

## Practice Problems

**1. Coulomb's Law.** A Na\(^+\) ion (\(+e\)) and a Cl\(^-\) ion (\(-e\)) are separated by \(r = 0.28\ \text{nm}\) in aqueous solution (treat as free charges). Calculate the electrostatic force. Is it attractive or repulsive?

**2. Electric Potential.** A charge \(Q = +5\times10^{-9}\ \text{C}\) is fixed at the origin. Calculate the electric potential at \(r = 5\ \text{cm}\).