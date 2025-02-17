# Formal introduction to bands 

## Bloch's theorem 
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


## Free particle solution 
It is useful to understand the relationship between the structure of $V(x)$ and the resulting band structure. We can begin by considering one extreme: solutions to the Schrödinger equation when $V(x)=0$, i.e. the case of free electrons. 

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

## Kronig-Penney 

In the previous section, we found the band structure for a 1D chain in a constant, trivially periodic potential. It is now time to see how this changes with a more complex, truly ``crystal'' potential, which is non-constant and has well-defined periodicities. As we will see, even small deviations from a constant potential field can lead to significant changes to certain features of the band structure.
%
As in the last example, we want to find the solutions $\psi(x)$ to the one-electron Schr\"odinger equation

$$
    -\frac{\hbar^2}{2m}\frac{d^2}{dx^2}\psi(x)+V(x)\psi(x)=E\,\psi(x)
$$

We now consider a potential $V(x)$ of repeating finite square wells such that $V(x)=V(x+a)$ where $V(x)$ is 

$$
\begin{align}
    V(x) &=
    \begin{cases} 
        0 & \text{if }\quad 0 < x < a-b \quad( \text{region I}), \\ 
    -V_0 & \text{if } \quad -b <x < 0 \quad     (\text{region II}).        
    \end{cases}
\end{align}
$$

If we consider this potential function as an approximate model for a crystal lattice, then
the ions are assumed to be located in region II at the center of the square well. 
%
We start by determining the solution of a single potential well. 
%
The potential is defined to be zero in region I. As before, the solutions to the Schr\"odinger equation in region I are then
%

$$
    -\frac{\hbar^2}{2m}\frac{d^2}{dx^2}\psi_{\rm I}(x)=E\,\psi_{\rm I}(x)
$$


$$
    \psi_{\rm I} = A\, e^{i\kappa x} + B\,e^{-i\kappa x}, \quad 
    \kappa = \sqrt{\frac{2mE}{\hbar^2}}.
$$


In the potential well (i.e. region II), where $V(x)=-V_0$ we consider solutions 

$$
    -\frac{\hbar^2}{2m}\frac{d^2}{dx^2}\psi_{\rm II}(x)=(E+V_0)\,\psi_{\rm II}(x)
$$

$$
    \psi_{ {\rm II}} = C\, e^{iqx} + D\, e^{-iqx}, \quad q = \sqrt{\frac{2m(E + V_0)}{\hbar^2}}
$$

%
The standard scattering problem would consist of matching the solutions of region I and II in both slope and derivative at the boundaries of the well in order to determine the coefficients. This condition is still necessary but insufficient, as it fails to incorporate the periodicity of the lattice. We use Bloch's theorem to relate the solution at $-b$ to the solution at $a-b, 2a-b, 3a-b \ldots$ 

This is why Bloch's theorem is so powerful. We previously demonstrated that for a periodic potential, the solutions take the form


$$
    \psi_k(x+ma)=e^{ikam}\psi_k(x)
$$

%
Given this, we can express the periodic solutions in region I as  
%
$$
\psi_{\rm I}(x+ma)=Ae^{i\kappa x}e^{i\kappa ma}+Be^{-i\kappa x}e^{i\kappa ma}=\left(Ae^{i\kappa x}+Be^{-i\kappa x}\right)e^{ik am}
$$

%
and the periodic solutions in region II as 

$$
\psi_{\rm II}(x+ma)=Ce^{iqx}e^{iqma}+De^{-iqx}e^{iqma}=\left(Ce^{iqx}+De^{-iqx}\right)e^{ikam}
$$

%
we now have four boundary conditions 
%
%
%
% We need the solutions for region I for the first cell (I=0 and $x=-b$) to match with the periodic copy in region II, at I=1, $x=a-b$.
%

$$
% \left(Ae^{-i\kappa b}+Be^{i\kappa b}\right)=\left(Ce^{-iqb}+De^{iqb}\right)e^{ikaI}
$$ 
<!-- %
%
%
% We have four conditions. The solutions must match at the boundary and the periodic solutions must also match. The condition for matching the periodic solution is given by 
%
% \begin{equation}
%     \psi_k(x+a+b)=e^{ik(a+b)}\psi_k(x)
% \end{equation}
% The periodic boundary conditions are given in item 3 and 4. 
%
% -->
1. **Continuity of \(\psi(x)\) at \(x=0\)**

   $$
   Ae^{ik0} + Be^{-ik0} = Ce^{iq0} + De^{-iq0}
   \quad (A + B - C - D = 0)
   $$

2. **Continuity of \(\frac{d\psi}{dx}\) at \(x=0\)**

   $$
   i\kappa A e^{i\kappa 0} - i\kappa B e^{-i\kappa 0}
   =
   i q C e^{i q 0} - i q D e^{-i q 0}
   \quad (\kappa A - \kappa B - qC + qD)
   $$

3. **Continuity of \(\psi_{\text{I}}(a-b) = \psi_{\text{II}}(-b) e^{ik a}\)**

   $$
   A e^{i\kappa (b-a)} + B e^{-i\kappa (b-a)}
   =
   \bigl(C e^{i q b} + D e^{-i q b}\bigr) e^{i k a}
   $$

4. **Continuity of \(\psi'_{\text{I}}(a-b) = \psi'_{\text{II}}(-b) e^{ik a}\)**

   $$
   i\kappa A e^{i\kappa (b-a)} - i\kappa B e^{-i\kappa (b-a)}
   =
   \bigl(i q C e^{i q b} - i q D e^{-i q b}\bigr) e^{i k a}
   $$



$$
     \psi_k(x+Ia)=e^{ikaI}\psi_k(x)
$$

% Then at $x=-b$ and $x=a$ we have 

% \begin{equation}
%     \psi_(x+a+b)=e^{ik(a+b)}\psi_k(x)
% \end{equation}


$$
     \psi_1(a)=e^{ik(a+b)}\psi_2(-b)
$$

$$
     \psi'_1(a)=e^{ik(a+b)}\psi'_2(-b)
$$

The coefficients can easily be identified by setting the determinant of the resulting constraint matrix, $M$, to zero:

$$
\det(M) = \begin{vmatrix}
1 & 1 & -1 & -1 \\
\kappa & -\kappa & -q & q \\
e^{i \kappa (a - b)} & e^{-i \kappa (a - b)} & -e^{i k a - i q b} & -e^{i k a + i q b} \\
\kappa e^{i \kappa (a - b)} & -\kappa e^{-i \kappa (a - b)} & -q e^{i k a - i q b} & q e^{i k a + i q b}
\end{vmatrix}=0
$$