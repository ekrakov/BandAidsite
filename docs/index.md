# Introduction

To a first-order approximation, one could say that computational material science is essentially the prediction of material behavior. For example, we might wish to see if some arrangement of atoms forms a semiconductor or a metal, or to go further and compute the thermal and electrical conductivity of the material. Here, we focus on crystalline solids where we may assume the atoms are arranged periodically. The properties of materials are largely determined by the behavior of the electrons under the potential landscape created by this arrangement. 

Solving for electron behavior in an isolated atom yields the familiar $s$, $p$, $d$, $\ldots$, orbitals we get from solving the Schrödinger equation in spherical coordinates. However, a material contains many atoms, resulting in a periodic potential. Electrons now display complex *interatomic* behavior, with linear combinations of bonding and antibonding states. This drastically changes the energy landscape: single-atom electron orbitals have neatly-spaced discrete energies, but electrons in a many-atom system have orbitals that hybridize and combine, yielding a continuous spectrum of allowed energies around the single-atom energies. These solutions are numerous enough to form a continuous band in reciprocal space, and the result is what is known as a band structure.  


Out interest is in solving the energy states of the Schrödinger equation under a periodic potential such that $V(\br)=V(\br+\bR)$. The following tutorial will provide an introduction into how to interpret band structure. 

- **[1D square well](1Dfinite.md)**  
  Explains how to solve the Schrödinger equation for a single square well potential.

- **[Multiple square wells](bands.md)**  
  Shows how the energy states evolve as more wells are added, introducing the concept of band structure by animating the formation of bands.

- **[Formal introduction to bands](bounds.md)**  
  Provides a formal look at band theory, starting with Bloch’s theorem and then moving on to the free-particle solution and the Kronig–Penney model—a direct method for solving the periodic Schrödinger equation.

<!-- - [Usage]( -->