---
title: Symmetry of Electron Integrals
author: HXu
date: 2023-06-25
category: notes
layout: post
---

## Unperturbed Integrals
For later use, we define the following symmetry operations for two-electron integrals:

- Interchange of electron 1 and 2 (permutation P1)
- Interchange of orbital indices on electron 1 (permutation P2)
- Interchange of orbital indices on electron 2 (permutation P3)

### One-Electron Integrals
The symmetry for one-electron integrals is simple:

$$
\begin{align}
  h _{pq} = \langle p \vert \hat{h} \vert q\rangle = \langle q \vert \hat{h} \vert p \rangle ^{*} = h _{qp}^{*}
\end{align}
$$

for complex orbitals and $h _{pq} = h _{qp}$ for real orbitals. 

### Two-Electron Integrals: General Case
In most general case (complex orbitals), we have 4-fold symmetry for the 2e integrals:

$$
\begin{align}
  \langle pq \vert rs\rangle = \langle qp \vert sr\rangle = \langle rs \vert pq\rangle ^{*} = \langle sr \vert qp\rangle ^{*}
\end{align}
$$

or in chemists' notation:

$$
\begin{align}
  (pq \vert rs) = (rs \vert pq) = (qp \vert sr) ^{*} = (sr \vert qp)^{*}
\end{align}
$$

during which we applied P1, and/or P2+P3.
Note that in general case P2 and P3 must be applied simultaneously, resulting a complex conjugate.

### Two-Electron Integrals: Real Orbital Basis
For real orbitals, we remove the complex conjugate restriction, and P2/P3 could be applied alone, producing the ordinary 8-fold symmetry:

$$
\begin{align}
  \langle pq \vert rs\rangle = \langle qp \vert sr\rangle = \langle rs \vert pq \rangle = \langle sr \vert qp\rangle
  = \langle rq \vert ps \rangle = \langle qr \vert sp\rangle = \langle ps \vert rq \rangle = \langle sp \vert qr \rangle
\end{align}
$$

or in chemists' notation:

$$
\begin{align}
  (pq \vert rs) = (qp \vert rs) = (qp \vert sr) = (pq \vert sr) = (rs \vert pq) = (rs \vert qp) = (sr \vert qp) = (sr \vert pq)
\end{align}
$$

### Anti-Symmetrized Two-Electron Integrals
The anti-symmetrized integrals are conveniently defined as:

$$
\begin{align}
  \langle pq \vert \vert rs\rangle = \langle pq \vert rs\rangle - \langle pq \vert sr \rangle
\end{align}
$$

Using the permutation symmetry of the 2e integrals, we find in general:

$$
\begin{align}
  \langle pq \vert \vert rs \rangle = \langle qp \vert \vert sr\rangle = \langle rs \vert \vert pq\rangle ^{*} = \langle sr \vert \vert qp \rangle ^{*}
  = - \langle pq \vert \vert sr \rangle = - \langle qp \vert \vert rs \rangle = - \langle rs \vert \vert qp \rangle ^{*} = - \langle sr \vert \vert pq \rangle ^{*}
\end{align}
$$

and for real orbitals, we simply drop the complex conjugate:

$$
\begin{align}
  \langle pq \vert \vert rs \rangle = \langle qp \vert \vert sr\rangle = \langle rs \vert \vert pq\rangle = \langle sr \vert \vert qp \rangle
  = - \langle pq \vert \vert sr \rangle = - \langle qp \vert \vert rs \rangle = - \langle rs \vert \vert qp \rangle = - \langle sr \vert \vert pq \rangle
\end{align}
$$

## Perturbed Integrals
The perturbed electron integrals, i.e. the derivative integrals, may possess different permutation symmetry than the unperturbed ones, depending on the nature of the perturbation.  
For unperturbed integrals, the permutation symmetry is identical for AO and MO representation as the integral transformation is simple and all MO coefficients are real.
As for integral derivatives, we have to be more careful as we are dealing with perturbed MO coefficients. In this case, we start with AO representation and then work our way towards the MO representation through
integral transformation, which may seem not trivial at first.

### GIAO Two-Electron Integrals
The GIAO 2e integrals inherit the permutation symmetry of 2e integrals in general case, and by the imaginary nature of magnetic perturbation, the first derivative GIAO 2e integrals are purely imaginary, therefore possess 4-fold symmetry (abbreviating $\pdv{\langle \mu \nu \vert \rho \sigma\rangle}{\mathbf{B}}$ as $\langle \mu \nu \vert \rho \sigma\rangle ^{\mathbf{B}}$ ):

$$
\begin{align}
  \langle \mu \nu \vert \rho \sigma \rangle ^{\mathbf{B}} = \langle \nu \mu \vert \sigma \rho \rangle ^{\mathbf{B}}
  = - \langle \rho \sigma \vert \mu \nu \rangle ^{\mathbf{B}} = - \langle \sigma \rho \vert \nu \mu \rangle ^{\mathbf{B}}
\end{align}
$$

With unperturbed MO coefficients, the transformed integrals possess the same 4-fold symmetry:

$$
\begin{align}
  \langle pq \vert rs\rangle ^{(\mathbf{B})} = \langle qp \vert sr \rangle ^{(\mathbf{B})} = - \langle rs \vert pq \rangle ^{(\mathbf{B})} = - \langle sr \vert qp \rangle ^{(\mathbf{B})}
\end{align}
$$

We quote here the equation for integral transformation:

$$
\begin{align}
  \langle pq \vert rs\rangle ^{\mathbf{B}} =& \langle pq \vert rs\rangle ^{(\mathbf{B})} + \sum_{t}U _{tp}^{\mathbf{B}*}\langle tq \vert rs\rangle + \sum_{t}U _{tq}^{\mathbf{B}*}\langle pt \vert rs\rangle
  + \sum_{t}\langle pq \vert ts \rangle U _{tr}^{\mathbf{B}} + \sum_{t}\langle pq \vert rt\rangle U _{ts}^{\mathbf{B}} \\
  =& \langle pq \vert rs\rangle ^{(\mathbf{B})} + \langle p ^{\mathbf{B}} q \vert rs\rangle + \langle p q ^{\mathbf{B}} \vert rs\rangle + \langle pq \vert r ^{\mathbf{B}}s \rangle + \langle pq \vert rs ^{\mathbf{B}}\rangle \nonumber
\end{align}
$$

To investigate the P1 symmetry on the derivative integrals, we look at the CPSCF terms in the integral transformation for $\langle qp\vert sr \rangle ^{\mathbf{B}}$ :

$$
\begin{align}
  \langle qp \vert sr \rangle ^{\mathbf{B}} \leftarrow & \langle q ^{\mathbf{B}}p \vert sr \rangle + \langle qp ^{\mathbf{B}} \vert sr\rangle + \langle qp \vert s ^{\mathbf{B}}r\rangle + \langle qp \vert sr ^{\mathbf{B}}\rangle \\
  =& \langle pq ^{\mathbf{B}}|rs \rangle + \langle p ^{\mathbf{B}}q\vert rs\rangle + \langle pq \vert rs ^{\mathbf{B}}\rangle + \langle pq \vert r ^{\mathbf{B}}s\rangle \rightarrow \langle pq\vert rs\rangle ^{\mathbf{B}} \nonumber
\end{align}
$$

in which we used P1 symmetry for the unperturbed 2e integrals.  
Similarly, we can look at CPSCF contributions to $\langle rs \vert pq\rangle ^{\mathbf{B}}$ and $\langle sr\vert qp\rangle ^{\mathbf{B}}$ for P2 and P3:

$$
\begin{align}
  \langle rs \vert pq\rangle ^{\mathbf{B}} \leftarrow & \langle r ^{\mathbf{B}} s \vert pq\rangle + \langle rs ^{\mathbf{B}}\vert pq\rangle + \langle rs\vert p ^{\mathbf{B}}q\rangle + \langle rs\vert pq ^{\mathbf{B}}\rangle \\
  =& \langle pq \vert r ^{\mathbf{B}}s\rangle ^{*} + \langle pq\vert rs ^{\mathbf{B}}\rangle ^{*} + \langle p ^{\mathbf{B}}q\vert rs\rangle ^{*} + \langle pq ^{\mathbf{B}}\vert rs\rangle ^{*} \rightarrow \langle pq\vert rs\rangle ^{\mathbf{B}*} \nonumber \\
  \langle sr \vert qp\rangle ^{\mathbf{B}} \leftarrow & \langle s ^{\mathbf{B}}r \vert qp\rangle + \langle sr ^{\mathbf{B}}\vert qp\rangle + \langle sr\vert q ^{\mathbf{B}}p\rangle + \langle sr\vert qp ^{\mathbf{B}}\rangle \\
  =& \langle qp \vert s ^{\mathbf{B}}r\rangle ^{*} + \langle qp \vert sr ^{\mathbf{B}}\rangle ^{*} + \langle q ^{\mathbf{B}}p\vert sr\rangle ^{*} + \langle qp ^{\mathbf{B}}\vert sr\rangle ^{*} \rightarrow \langle qp \vert sr\rangle ^{\mathbf{B}*} \nonumber
\end{align}
$$

in which we used P2 and P3 symmetry for the unperturbed 2e integrals, e.g.:

$$
\begin{align}
  \langle r ^{\mathbf{B}}s\vert pq\rangle = \sum_{t}U _{tr}^{\mathbf{B}*}\langle ts\vert pq\rangle
  = \sum_{t}U _{tr}^{\mathbf{B}*}\langle pq\vert ts\rangle ^{*} = \Big(\sum_{t}U _{tr}^{\mathbf{B}}\langle pq\vert ts\rangle \Big)^{*}
  = \langle pq\vert r ^{\mathbf{B}}s\rangle ^{*}
\end{align}
$$

Therefore, we have the same 4-fold symmetry for the total integral derivatives in MO representation (using the fact that $\mathbf{U}^{\mathbf{B}*} = -\mathbf{U}^{\mathbf{B}}$ ):

$$
\begin{align}
  \langle pq \vert rs\rangle ^{\mathbf{B}} = \langle qp \vert sr\rangle ^{\mathbf{B}} = - \langle rs \vert pq\rangle ^{\mathbf{B}} = - \langle sr \vert qp\rangle ^{\mathbf{B}}
\end{align}
$$

### GIAO One-Electron Integrals
With the same argument, the GIAO 1e integrals are imaginary and anti-symmetric:

$$
\begin{align}
  h _{\mu \nu}^{\mathbf{B}} =& - h _{\nu \mu}^{\mathbf{B}} = - h _{\mu \nu}^{\mathbf{B}*} = h _{\nu \mu}^{\mathbf{B}*} \\
  h _{pq}^{\mathbf{B}} =& - h _{qp}^{\mathbf{B}} = - h _{pq} ^{\mathbf{B}*} = h _{qp}^{\mathbf{B}*}
\end{align}
$$