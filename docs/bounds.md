
# Bloch's theorem 
Our lattice is periodic under translation by a lattice vector $\bR$. While it is not immediately clear how this will play into our final solution, it is helpful to start by introducing a translation operator $\That$ such that 

$$ \That \psi(\br)=\psi(\br+\bR) $$

The eigenspectrum of this operator seems a little easier to understand than that of $\Hhat$. Because our lattice is periodic in $\bR$, implying $\Hhat(\br + \bR) = \Hhat(\br)$, we can show that the operators $\That$ and $\Hhat$ commute:


$$\That\Hhat(\br)\psi(\br) = \Hhat(\br + \bR)\psi(\br + \bR) = \Hhat(\br)\That\psi(\br) $$


By a well-known property, showing that $\That$ and $\Hhat$ commute under periodicity $\bR$ implies that they share a common set of eigenfunctions. Finding the eigenfunctions of $\That$ then equates to solving for the eigenfunctions of $\Hhat$, a powerful simplification.

We now wish to determine the form of the eigenfunctions of $\That$. For example, eigenfunctions of eigenvalue $\lambda=1$ are totally periodic in $\bR$, such that $f(\br)$  does not change when translated by $\bR$:

$$\That f(\br)=f(\br+\bR)=f(\br)$$


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


# Free particle solution 
It is useful to understand the relationship between the structure of $V(x)$ and the resulting band structure. We can begin by considering one extreme: solutions to the Schr\"odinger equation when $V(x)=0$, i.e. the case of free electrons. 

$$
  -\frac{\hbar^2}{2m}\frac{d^2}{dx^2}\psi(x)=E\,\psi(x)
$$

The solutions to the free electron problem are the family of plane waves

$$
    \psi_k(x)=e^{iqx} \, , \quad \quad E = \frac{\hbar^2 q^2}{2 m}
$$

 where $q$ is not restricted to be in the Brillouin zone. However, if $q$ does not belong to the Brillouin zone, we can decompose $q$ as $q=G+k$, where $G$ is the reciprocal lattice vector $G$ and $k$ a vector bounded within the Brillouin zone $\left(-\frac{\pi}{a}, \frac{\pi}{a}\right)$.

Because $V$ is a constant function, our problem is trivially periodic, but for the sake of argument we can choose a particular periodicity $G$, defining the corresponding solutions in the the form of Bloch's theorem

$$
    \psi(x)=e^{iqx}=e^{iGx}e^{ikx}
$$

where $e^{iGx}$ is effectively $u(x)$, the component that is periodic with the ``lattice", modulated by $e^{ikx}$. The energy of a free particle is given by 

$$
  E=\frac{\hbar^2}{2m}|q|^2
$$

Where $G=\frac{2\pi n}{a}$ and $q=k+G$
Our energy can then be expressed as 

$$
    E = \frac{\hbar^2}{2m}|G+k|^2
$$

With this formulation of our wavefunction, we can plot our solutions inside the Brillouin zone. While this band structure is unquestionably a toy example, its characteristics will be useful for comparison to band structures induced by nontrivial periodic potentials. 

