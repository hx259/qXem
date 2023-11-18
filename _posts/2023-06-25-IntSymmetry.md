---
title: Symmetry of Electron Integrals
author: HXu
date: 2023-06-25
category: notes
layout: post
---

For later use, we define the following symmetry operations for two-electron integrals:

- Interchange of electron 1 and 2 (permutation P1)
- Interchange of orbital indices on electron 1 (permutation P2)
- Interchange of orbital indices on electron 2 (permutation P3)

## Unperturbed Integrals

### One-Electron Integrals
The symmetry for one-electron integrals is simple:

$$
\begin{align}
  h _{pq} = \langle p \vert \hat{h} \vert q\rangle = \langle q \vert \hat{h} \vert p \rangle ^{*} = h _{qp}^{*}
\end{align}
$$

for complex orbitals and $h _{pq} = h _{qp}$ for real orbitals. 

### Two-Electron Integrals: General Case
In most general case (**complex orbitals**), we have 4-fold symmetry for the 2e integrals:

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
For **real orbitals**, we remove the complex conjugate restriction, and P2/P3 could be applied alone, producing the ordinary 8-fold symmetry:

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

Using the permutation symmetry of the 2e integrals, we find for **complex orbitals**:

$$
\begin{align}
  \langle pq \vert \vert rs \rangle = \langle qp \vert \vert sr\rangle = \langle rs \vert \vert pq\rangle ^{*} = \langle sr \vert \vert qp \rangle ^{*}
  = - \langle pq \vert \vert sr \rangle = - \langle qp \vert \vert rs \rangle = - \langle rs \vert \vert qp \rangle ^{*} = - \langle sr \vert \vert pq \rangle ^{*}
\end{align}
$$

and for **real orbitals**, we simply drop the complex conjugate:

$$
\begin{align}
  \langle pq \vert \vert rs \rangle = \langle qp \vert \vert sr\rangle = \langle rs \vert \vert pq\rangle = \langle sr \vert \vert qp \rangle
  = - \langle pq \vert \vert sr \rangle = - \langle qp \vert \vert rs \rangle = - \langle rs \vert \vert qp \rangle = - \langle sr \vert \vert pq \rangle
\end{align}
$$

## Perturbed Integrals
The perturbed electron integrals, i.e. the derivative integrals, may possess different permutation symmetry than the unperturbed ones, depending on the nature of the perturbation.  
For unperturbed integrals, the permutation symmetry is identical for AO and MO representation as the integral transformation is simple and all MO coefficients are real.
As for integral derivatives, we have to be more careful as we are dealing with **perturbed MO coefficients**. In this case, we start with AO representation and then work our way towards the MO representation through integral transformation, which may seem not trivial at first.

### GIAO Two-Electron Integrals
The GIAO 2e integrals inherit the permutation symmetry of 2e integrals in general case, and by the imaginary nature of magnetic perturbation, the first derivative GIAO 2e integrals are purely imaginary, therefore possess 4-fold symmetry (abbreviating $\pdv{\langle \mu \nu \vert \rho \sigma\rangle}{\mathbf{B}}$ as $\langle \mu \nu \vert \rho \sigma\rangle ^{\mathbf{B}}$ ):

$$
\begin{align}
  (\mu \nu \vert \kappa \tau) ^{\mathbf{B}} = - (\nu \mu \vert \tau \kappa \rangle ^{\mathbf{B}}
  =  (\kappa \tau \vert \mu \nu) ^{\mathbf{B}} = - (\tau \kappa \vert \nu \mu) ^{\mathbf{B}}
\end{align}
$$

To see this in a more rigorous manner, we start from the general expression of the GIAOs:

$$
\begin{align}
  \vert \chi _{\nu}(\mathbf{B})\rangle = e ^{-\frac{i}{2}(\mathbf{B} \times \mathbf{R}^{\mu O})\cdot \mathbf{r}} \vert \chi _{\mu}(\mathbf{0})\rangle
\end{align}
$$

With the vector identities (Einstein summation convention applied):

$$
\begin{gather}
  (\mathbf{B} \times \mathbf{R}^{\mu O} ) \cdot \mathbf{r} = \epsilon _{ijk}r _{i}B _{j}R _{k}^{\mu O} \\
  \pdv{B _{\alpha}}[(\mathbf{B} \times \mathbf{R}^{\mu O} ) \cdot \mathbf{r}] = \epsilon _{ijk}r _{i}\delta _{j \alpha}R _{k}^{\mu O} = [\mathbf{R}^{\mu O} \times \mathbf{r}]_{\alpha}
\end{gather}
$$

We can evaluate the field deriavtive for the basis function as:

$$
\begin{align}
  \pdv{\vert\chi _{\mu}(\mathbf{B})\rangle}{B _{\alpha}} = \pdv{B _{\alpha}}e ^{-\frac{i}{2}(\mathbf{B} \times \mathbf{R}^{\mu O})\cdot \mathbf{r}} \vert\chi _{\mu}(\mathbf{0})\rangle
  = -\frac{i}{2} [\mathbf{R}^{\mu O}\times \mathbf{r}]_{\alpha}\vert\chi _{\mu}(\mathbf{B})\rangle \nonumber
\end{align}
$$

The derivative 2e integral can then be expressed as (in chemists' notation):

$$
\begin{align}
  \pdv{B _{\alpha}}(\mu \nu\vert \kappa \tau) =& (\pdv{\chi _{\mu}}{B _{\alpha}} \nu \vert \kappa \tau)
  + (\mu \pdv{\chi _{\nu}}{B _{\alpha}}\vert \kappa \tau) + (\mu \nu \vert \pdv{\chi _{\kappa}}{B _{\alpha}}\tau)
  + (\mu \nu\vert \kappa \pdv{\chi _{\tau}}{B _{\alpha}}) \nonumber \\
  =& (-\frac{i}{2})^{*}\left(\mu \nu \Big\vert \frac{[\mathbf{R}^{\mu O}\times \mathbf{r}_{1}]_{\alpha}}{r _{12}} \Big\vert \kappa \tau\right) + \frac{i}{2}\left(\mu \nu\Big\vert \frac{\mathbf{R}^{\nu O}\times \mathbf{r}_{1}}{r _{12}} \Big\vert \kappa \tau\right) \nonumber \\
  &+ (-\frac{i}{2})^{*}\left(\mu \nu \Big\vert \frac{[\mathbf{R}^{\kappa O}\times \mathbf{r}_{2}]_{\alpha}}{r _{12}} \Big\vert \kappa \tau\right) + \frac{i}{2}\left(\mu \nu\Big\vert \frac{\mathbf{R}^{\tau O}\times \mathbf{r}_{2}}{r _{12}} \Big\vert \kappa \tau\right) \nonumber \\
  =& \frac{i}{2}\left(\mu \nu \Big\vert \frac{[\mathbf{R}^{\mu \nu} \times \mathbf{r _{1}} + \mathbf{R}^{\kappa \tau} \times \mathbf{r}_{2}]_{\alpha}}{r _{12}} \Big\vert \kappa \tau\right)
\end{align}
$$

Generally, in 3-dimensional space:

$$
\begin{align}
  \pdv{(\mu \nu \vert \kappa \tau)}{\mathbf{B}} = \frac{i}{2}\left(\mu \nu \Big\vert \frac{\mathbf{R}^{\mu \nu} \times \mathbf{r _{1}} + \mathbf{R}^{\kappa \tau} \times \mathbf{r}_{2}}{r _{12}} \Big\vert \kappa \tau\right) = \frac{i}{2}\left(\mu \nu \Big\vert \frac{\mathbf{Q} _{\mu \nu}\mathbf{r}_{1}+\mathbf{Q}_{\kappa \tau}\mathbf{r}_{2}}{r _{12}} \Big\vert \kappa \tau\right)
\end{align}
$$

Now we can see the symmetry clearly:
  * by simultaneously swapping $\mu \leftrightarrow \nu$ and $\kappa \leftrightarrow \tau$, $\mathbf{R}^{\mu\nu}$ becomes $\mathbf{R}^{\nu\mu} = -\mathbf{R}^{\mu\nu}$, and $\mathbf{R}^{\kappa\tau}$ becomes $\mathbf{R}^{\tau\kappa} = -\mathbf{R}^{\kappa\tau}$, hence $(-1)$
  * by simultaneously swapping $\mu \leftrightarrow \kappa$ and $\nu \leftrightarrow \tau$, we get back the same expression, hence $(+1)$
  * any other swaps do not lead to valid symmetry

This could be summarized as:

$$
\begin{align}
  (\mu \nu \vert \kappa \tau) ^{\mathbf{B}} = - (\nu \mu \vert \tau \kappa \rangle ^{\mathbf{B}}
  =  (\kappa \tau \vert \mu \nu) ^{\mathbf{B}} = - (\tau \kappa \vert \nu \mu) ^{\mathbf{B}}
\end{align}
$$

#### Integral Transformation into MO Basis

With unperturbed MO coefficients $\mathbf{C}(0)$, the transformed integrals possess the same 4-fold symmetry:

$$
\begin{align}
  (pr|qs)^{\mathbf{(B)}} = (qs|pr)^{\mathbf{(B)}} = -(rp|sq)^{\mathbf{(B)}} = - (sq|rp)^{\mathbf{(B)}}
\end{align}
$$

or in physicists' notation:

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

Therefore, we have the same 4-fold symmetry for the total integral derivatives in MO representation (using the fact that $\mathbf{U}^{\mathbf{B}*} = -\mathbf{U}^{\mathbf{B}}$ ),just as the AO ones:

$$
\boxed{
\begin{align}
  \langle pq \vert rs\rangle ^{\mathbf{B}} = \langle qp \vert sr\rangle ^{\mathbf{B}} =& - \langle rs \vert pq\rangle ^{\mathbf{B}} = - \langle sr \vert qp\rangle ^{\mathbf{B}} \\
  \langle \mu \nu \vert \rho \sigma \rangle ^{\mathbf{B}} = \langle \nu \mu \vert \sigma \rho \rangle ^{\mathbf{B}}
  =& - \langle \rho \sigma \vert \mu \nu \rangle ^{\mathbf{B}} = - \langle \sigma \rho \vert \nu \mu \rangle ^{\mathbf{B}}
\end{align}
}
$$

### GIAO One-Electron Integrals
With the same argument, the GIAO 1e integrals are imaginary and anti-symmetric:

$$
\boxed{\begin{align}
  h _{\mu \nu}^{\mathbf{B}} =& - h _{\nu \mu}^{\mathbf{B}} = - h _{\mu \nu}^{\mathbf{B}*} = h _{\nu \mu}^{\mathbf{B}*} \\
  h _{pq}^{\mathbf{B}} =& - h _{qp}^{\mathbf{B}} = - h _{pq} ^{\mathbf{B}*} = h _{qp}^{\mathbf{B}*}
\end{align}}
$$