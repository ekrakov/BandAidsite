# Introduction to bands 

## Free particle solution 

It is useful to understand the relationship between the structure of $V(x)$ and the resulting band structure. We can begin by considering one extreme: solutions to the Schr\"odinger equation when $V(x)=0$, i.e. the case of free electrons. 
$$
  -\frac{\hbar^2}{2m}\frac{d^2}{dx^2}\psi(x)=E\,\psi(x)
$$
%
The solutions to the free electron problem are the family of plane waves

$$
    \psi_k(x)=e^{iqx} \, , \quad \quad 
    E = \frac{\hbar^2 q^2}{2 m}
$$
 where $q$ is not restricted to be in the Brillouin zone. However, if $q$ does not belong to the Brillouin zone, we can decompose $q$ as $q=G+k$, where $G$ is the reciprocal lattice vector $G$ and $k$ a vector bounded within the Brillouin zone $\left(-\frac{\pi}{a}, \frac{\pi}{a}\right)$.
%
Because $V$ is a constant function, our problem is trivially periodic, but for the sake of argument we can choose a particular periodicity $G$, defining the corresponding solutions in the the form of Bloch's theorem
\begin{equation}
    \psi(x)=e^{iqx}=e^{iGx}e^{ikx}
\end{equation}
where $e^{iGx}$ is effectively $u(x)$, the component that is periodic with the ``lattice", modulated by $e^{ikx}$. The energy of a free particle is given by 

$$
  E=\frac{\hbar^2}{2m}|q|^2
$$
%
Where $G=\frac{2\pi n}{a}$ and $q=k+G$
Our energy can then be expressed as 

$$
    \frac{\hbar^2}{2m}|G+k|^2
$$
%
With this formulation of our wavefunction, we can plot our solutions inside the Brillouin zone. While this band structure is unquestionably a toy example, its characteristics will be useful for comparison to band structures induced by nontrivial periodic potentials. 



## Introduction to Bands

## Multi–Square-Well Animation: From Isolated Levels to Energy Bands

In this animation, we explore how discrete quantum energy levels evolve into **energy bands** when multiple square wells are arranged in one dimension—mimicking, in a simplified way, how an electron behaves in a crystalline solid. Note that we are only solving the **single-electron** Schrödinger equation.

---

### 1. Single Square Well (One “Atom”)

- Begin with **one** square well by setting the number of wells to **1**. The square potential represents a simplified model of an electron bound to a single atomic nucleus.  
- In the second figure, you can see a set of **discrete bound-state** energy levels. If we were to solve the full 3D Schrödinger equation, these levels would correspond to the energies of particular orbital configurations.  
- The third figure plots the **wavefunction** corresponding to a selected energy level. Change the **index** in the second figure to explore how the wavefunction evolves with different eigenstates.

---

### 2. Adding Two Wells

- Next, increase the number of wells to **2**. The idea is that each well represents an atomic nucleus at its center, and the single electron can interact with either nucleus.  
- In the third plot, you can see the wavefunction and its probability amplitude. For the **first** eigenstate (index 0), the electron is primarily localized **between** the two wells—analogous to a **bonding** orbital in chemistry.  
- Now set the eigenvalue index to **1**. You’ll observe that the probability of finding the electron between the wells is negligible, which corresponds to an **antibonding** orbital. The first two orbitals can be roughly viewed as **s-type** bonding and antibonding states.  
- If you move on to the **second** and **third** eigenstates (indices 2 and 3), you’ll notice bonding and antibonding states that resemble **p-like** orbitals in shape.

---

### 3. Formation of Bands

- Continue by changing the number of wells to **14**.  
- As more wells are added, the individual energy levels split and begin to form a **nearly continuous band** of allowed energies, separated by **band gaps**—energies the electron **cannot** occupy.  
- This captures, in a simplified manner, how overlapping atomic orbitals in a real crystal produce **valence and conduction bands**, with forbidden energy regions (band gaps) between them.

---

### 4. Additional Parameters: Well Depth, Spacing, and Width

- The animation allows you to tune various parameters: the **depth** of each square well, their **barrier width**, and the **distance** between wells.  
- The **barrier width** (distance between wells) controls wavefunction overlap. A **larger barrier** typically **reduces** overlap and **widens** the band gap.  
- The **well depth** determines how tightly bound each state is, shifting the entire set of energy levels up or down.  

Experiment with these parameters to see how they affect the shape of the wavefunctions, the spacing between energy levels, and the formation of continuous bands versus isolated levels.





<iframe src="https://bandaidsite-cs2bnku8pho7jigyznpczz.streamlit.app/?embed=true&embed_options=show_toolbar"
        style="width: 90%; height: 85vh; border: none;"></iframe>



### Bloch's theorem 
Our lattice is periodic under translation by a lattice vector $\bR$. While it is not immediately clear how this will play into our final solution, it is helpful to start by introducing a translation operator $\That$ such that 

$$
    \That \psi(\br)=\psi(\br+\bR)
$$

The eigenspectrum of this operator seems a little easier to understand than that of $\Hhat$. Because our lattice is periodic in $\bR$, implying $\Hhat(\br + \bR) = \Hhat(\br)$, we can show that the operators $\That$ and $\Hhat$ commute:


$$
    \That\Hhat(\br)\psi(\br) = \Hhat(\br + \bR)\psi(\br + \bR) = \Hhat(\br)\That\psi(\br)
$$


By a well-known property, showing that $\That$ and $\Hhat$ commute under periodicity $\bR$ implies that they share a common set of eigenfunctions. Finding the eigenfunctions of $\That$ then equates to solving for the eigenfunctions of $\Hhat$, a powerful simplification.

We now wish to determine the form of the eigenfunctions of $\That$. For example, eigenfunctions of eigenvalue $\lambda=1$ are totally periodic in $\bR$, such that $f(\br)$  does not change when translated by $\bR$:

$$
\That f(\br)=f(\br+\bR)=f(\br)
$$


More generally, consider a function that is not trivially periodic but  satisfies $\psi(\br+\bR)=\lambda \psi(\br)$. This behavior is well described by an exponential, but because we are describing a quantum system, it has to be an exponential that is normalizable, i.e., a complex exponential of the form $\psi = e^{i\bk\cdot\br}$. We apply $\That$ to find its eigenvalue: 

\[
   \That e^{i\bk\cdot\br} = e^{i(\bk \cdot \br + \bk \cdot \bR)} = 
\underbrace{e^{i \bk \cdot \bR}}_{\lambda} e^{i \bk \cdot \br}
\]

Our final eigenstate $\psi$ can be either periodic or of the form of the complex exponential. In general, any eigenfunction of $\That$ can be written

$$
    \psi(\br)=e^{i\bk \cdot \br}f(\br)
$$

%
where once again, $f(\br) = f(\br + \bR)$, and $e^{i\bk \cdot \br}$ is a consequence of the translational invariance of the system. As before, we can find the eigenvalue:

$$
    \That \psi(\br) = e^{i \bk \cdot \bR} e^{i \bk \cdot \br} f(\br+\bR)=e^{i \bk \cdot \bR} e^{i \bk \cdot \br} f(\br)
$$

Now we reiterate that the eigenfunction $\psi$ also belongs to $\Hhat$---we've exploited the commutativity of the two operators to find a solution for our periodic system simply by considering $\That$. This is Bloch's theorem. These so-called \textit{Bloch waves} can be written in full as

$$
\psi_{n\bk}(\br)=e^{i \bk \cdot \br} f_{n\bk}(\br)
$$