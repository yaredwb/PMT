---
layout: default
title: Porous Media Theory
bibliography: pmt.bib
mathjax: true
---

#### Author: [Yared W. Bekele](https://yaredwb.github.io/)
{:.no_toc}

**Contents**
* TOC
{:toc}

### Abstract
{:.no_toc}

The fundamental concepts and formulations in porous media
theory are presented. The discussion starts with a brief history of
porous media theory. The volume fraction concept and kinematic relations
are then presented. Conservation laws are derived in a general form
which may be applicable to any porous material subjected to different
physical processes. Thermodynamic formulations and phase transitions in
porous media are briefly discussed. Formulations that complete the
mathematical model for a given porous material, such as constitutive
laws, are also discussed. The main porous materials of interest in this
thesis are soils and specific conservation equations are derived for
hydraulic, hydro-mechanical and thermo-hydro-mechanical processes by
making the necessary assumptions for particular application needs.

# Background

The study of porous materials is essential in various disciplines of science and engineering such as soil mechanics, oil and reservoir engineering, biomechanics, material sciences and chemical engineering. The porous materials studied under porous media theory can either occur naturally, such as soils and rocks, or may be artificial, such as sponges and synthetic polymers. The physical and mechanical properties of such materials have been studied experimentally and mathematically over several decades by a number of researchers. Modern porous media theory, which will be discussed in detail in later sections, developed over a long period of time to reach to what is known today. The historical development of the theory is documented in some publications such as de Boer and Ehlers (1988)[^1] and de Boer (2003)[^2].

There are some important milestones in the development of porous media theory, as presented in de Boer (1998)[^3]. In the earliest stages of the theory, Leonhard Euler presented the first discussion on the geometry of a porous medium and indirectly contributed to the formulation of the axioms of continuum mechanics. The introduction of the volume fraction concept by Reinhard Woltman in the 19th century proved to be a fundamental contribution. This concept was further discussed by Achille Delesse. The development of mixture theory, a branch of porous media theory, was initiated by Adolph Fick. An important mathematical relation describing the motion of a fluid in a porous medium was derived by Henry Darcy, which we refer to today as Darcy’s law. In early 20th century, Paul Fillunger and Karl von Terzaghi made seminal contributions to the theory of liquid-saturated porous solids. Fillunger developed equations for uplift forces while studying the stresses acting on concrete and masonry gravity dams. Terzaghi also studied uplift forces independently of Fillunger and further made contributions to the understanding of capillary pressure, the concept of effective stresses and soil consolidation theory. The effective stress concept was discussed earlier by Fillunger. After mid 20th century, the theory of porous media started taking shape to become what we know today. Some of the contributions in this period include work on the theory of mixtures by Green and Naghdi (1967)[^4], without using the volume fraction concept, the study of fluid motion in porous media by Whitaker (1969)[^5], modeling of simultaneous heat, mass and momentum transfer by Whitaker (1977)[^6], the treatment of the mechanics of continuous porous media by Prevost (1980)[^7], a theory of
immiscible and structured mixtures by Bedford and Drumheller (1983)[^8] and a generalized approach to the derivation of balance laws by Hassanizadeh (1986)[^9]. Application of the theory of mixtures to the modeling of incompressible and compressible porous media was presented by Bowen (1980)[^10] and Bowen (1982) [^11], respectively. A discussion relating mixture theory and Biot’s approach to porous media theory can be found in Coussy et. al. (1986)[^12].

In the following sections, the basic components of porous media theory are presented. The volume faction concept, a fundamental concept in porous media theory, is first discussed. The conservation laws of mass, momentum and energy are then presented in a general form for a porous medium with any number of constituents. The mechanics of phase change in a porous medium and how it affects the conservation laws is then treated. Constitutive equations that govern the constituents of the porous medium are required to complete the theory and these are discussed afterwards. These sections are presented in a brief way here and a detailed presentation of the topics may be referred from modern treatments of porous media theory such as in Coussy (2004)[^13], Vadasz (2008)[^14] and Ehlers and Bluhm (2013)[^15].

# Volume Fraction Concept

One of the most important concepts in the development of porous media theory is the volume fraction concept. This concept is used to a idealize a porous medium with multiple constituents as a homogeneous continuum. An important assumption in the volume fraction concept is that the solid constituent of the porous medium is considered as a reference volume such that only the fluid constituents can enter or leave the reference volume; see Bluhm and de Boer (1997)[^16].

Consider a porous medium composed of $$ N $$ constituents. Let $$ V $$ be the total volume of he porous medium and $$ V^\alpha $$ be the volume of phase $$ \alpha $$. Let $$ \mathrm{d}V $$ be a control volume element in the total volume and $$ \mathbf x $$ be its position vector in a global coordinate system at a given time $$ t $$. Similarly, let $$ \mathbf r $$ be the position vector of a microscopic volume element $$ \mathrm{d} V_\mathrm{\beta} $$ inside $$ \mathrm{d}V  $$. The volume of constituent $$ \alpha $$ within the control volume can be determined by first defining a phase distribution function $$ \chi^\alpha $$ such that 

$$
\begin{equation}
\chi^\alpha(\mathbf r, t) = \begin{cases}
1 & \text{for} \quad \mathbf r \in \mathrm{d} V_\mathrm{\beta} \\
0 & \text{for} \quad \mathbf r \in \mathrm{d} V_\mathrm{\gamma}, \quad \beta \neq \gamma.
\end{cases}
\end{equation}
$$ 

Thus, the partial volume of constituent $$ \alpha $$ in the control volume can be written as

$$
\begin{equation}
\mathrm{d} V^\alpha(\mathbf x,t) =\int_{\mathrm{d} V} \chi^\alpha(\mathbf r, t) \mathrm{d} V_\mathrm{\beta}.
\end{equation}
$$

The volume fraction $$ n^\alpha $$ of phase $$ \alpha $$ can now be defined as

$$
\begin{equation}
n^\alpha (\mathbf x,t) = \frac{\mathrm{d} V^\alpha}{\mathrm{d} V} = \frac{1}{\mathrm{d} V} \int_{\mathrm{d} V} \chi^\alpha(\mathbf r, t) \mathrm{d} V_\mathrm{\beta}.
\end{equation}
$$

The position vector $$ \mathbf r $$ may be written in terms of the global position vector $$ \mathbf x $$ by introducing a local reference system $$ \mathbf \xi $$ with origin at $$ \mathbf x $$, such that $$ \mathbf r = \mathbf x + \mathbf \xi $$. The individual volumes of the constituents and their volume fractions satisfy the conditions

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \mathrm{d} V^\alpha = \mathrm{d} V \quad \text{and} \quad \sum\limits_{\alpha=1}^{N} n^\alpha = 1.
\end{equation}
$$

The volume fractions can now be used to describe the relationship between the densities of the constituents of the porous medium at microscopic and macroscopic levels. We denote the intrinsic real density of constituent $$ \alpha $$ by $$ \rho_\alpha $$ and the partial density at macroscale by $$ \rho^\alpha $$, following the notations according to Prevost (1980)[^7]. The relationship between these two densities in terms of the volume fraction of the phase under consideration is given by 

$$
\begin{equation}
\rho^\alpha(\mathbf x,t) = n^\alpha(\mathbf x,t) \rho_\alpha(\mathbf x,t). \label{e:partialdensities}
\end{equation}
$$ 

The total density of the mixture $$ \rho $$ is then the sum of the partial densities of all constituents i.e.

$$
\begin{equation}
\rho(\mathbf x,t) = \sum\limits_{\alpha=1}^{N} \rho^\alpha(\mathbf x,t).
\end{equation}
$$

# Kinematics

Kinematic relations describing the relative motions of the phases in a porous medium are briefly discussed here. These relations will be used later in deriving the conservation laws for a porous medium. A detailed presentation may be referred from Lewis and Schrefler (1998)[^17].

According to the volume fraction concept, a porous medium composed of $$ N $$ constituents is approximated as a homogeneous continuum. Thus, a material point defined by the position vector $$ \mathbf x $$ is simultaneously occupied by all phases. Let $$ \mathbf X^\alpha $$ be the reference position of phase $$ \alpha $$ at time $$ t=t_\mathrm{o} $$. The position of each material point $$ \mathbf x^\alpha $$ of phase $$ \alpha $$ at time $$ t $$ may be written in a Lagrangian description as

$$
\begin{equation}
\mathbf x^\alpha = \mathbf x^\alpha(\mathbf X^\alpha,t).
\end{equation}
$$

An Eulerian description of motion may be written for a non-singular Lagrangian description as

$$
\begin{equation}
\mathbf X^\alpha = \mathbf X^\alpha(\mathbf x^\alpha,t).
\label{e:xalpha}
\end{equation}
$$ 

For a particle of phase $$ \alpha $$ with a defined path, Lagrangian descriptions of the elocity and acceleration are 

$$
\begin{equation}
\begin{aligned}
\mathbf V^\alpha &= \frac{\partial \mathbf x^\alpha(\mathbf X^\alpha,t)}{\partial t} \\
\mathbf A^\alpha &= \frac{\partial^2 \mathbf x^\alpha(\mathbf X^\alpha,t)}{\partial t^2}.
\end{aligned}
\label{e:vaalpha}
\end{equation}
$$ 

Eulerian description of the velocity and acceleration may be derived by using equation \ref{e:xalpha} in \ref{e:vaalpha}. Given an Eulerian description of the velocity $$ \mathbf v^\alpha(\mathbf x^\alpha,t) $$, the Eulerian acceleration $$ \mathbf a^\alpha $$ may be derived by evaluating the time derivative of the velocity where the Lagrangian coordinates are held constant. That is, by applying the chain rule

$$
\begin{equation}
\mathbf a^\alpha = \frac{\partial \mathbf v^\alpha}{\partial t} + \nabla \mathbf v^\alpha \cdot \mathbf v^\alpha.
\end{equation}
$$

For any differentiable function $$ f^\alpha $$ describing some physical property of phase $$ \alpha $$ in the porous medium, the *material time derivative* (also called *convective derivative* or *Lagrangian derivative*) is introduced to describe its rate of change relative to a chosen phase. If the Eulerian description of $$ f^\alpha =  f^\alpha (\mathbf x^\alpha,t) $$ is given, its material time derivative with respect to a moving particle of phase $$ \alpha $$ is defined by 

$$
\begin{equation}
\frac{\mathrm{D}_\alpha f^\alpha}{\mathrm{D} t} := \frac{\partial f^\alpha}{\partial t} + \nabla f^\alpha \cdot \mathbf v^\alpha.
\label{e:mtdwrtalpha}
\end{equation}
$$

The material time derivative of $$ f^\alpha $$ with respect to a moving particle of another phase, say phase $$ \beta $$, is defined as

$$
\begin{equation}
\frac{\mathrm{D}_\beta f^\alpha}{\mathrm{D} t} := \frac{\partial f^\alpha}{\partial t} + \nabla f^\alpha \cdot \mathbf v^\beta.
\label{e:mtdwrtbeta}
\end{equation}
$$

Equations $$ \ref{e:mtdwrtalpha} $$ and $$ \ref{e:mtdwrtbeta} $$ result in the relation

$$
\begin{equation}
\frac{\mathrm{D}_\beta f^\alpha}{\mathrm{D} t} = \frac{\mathrm{D}_\alpha f^\alpha}{\mathrm{D} t} + \nabla f^\alpha \cdot \mathbf v^{\beta \alpha}
\label{e:mtdwrtbetarel}
\end{equation}
$$

where

$$
\begin{equation}
\mathbf v^{\beta \alpha} = \mathbf v^\beta - \mathbf v^\alpha
\end{equation}
$$

is the relative velocity of a particle of phase $$ \beta $$ with respect to phase $$ \alpha $$.The material time derivative may be applied to either a scalar or a vector quantity.

In porous media theory, we often require the rate of change of volume averaged quantities. For a vector physical property $$ \mathbf f^\alpha $$ of phase $$ \alpha $$ per unit volume, the total time derivative over a volume $$ V $$ is given according to Reynold’s transport theorem by

$$
\begin{equation}
\begin{aligned}
\frac{d}{dt} \int_{V} \mathbf f^\alpha \mathrm{d} V &= \int_{V} \left( \frac{\partial \mathbf f^\alpha}{\partial t} + \nabla \mathbf f^\alpha \cdot \mathbf v^\alpha + \mathbf f^\alpha \nabla \cdot \mathbf v^\alpha \right) \mathrm{d} V \\
&= \int_{V} \left[ \frac{\partial \mathbf f^\alpha}{\partial t} + \nabla \cdot \left( \mathbf f^\alpha \otimes \mathbf v^\alpha \right)  \right] \mathrm{d} V.
\end{aligned}
\label{e:transporttheorem}
\end{equation}
$$ 

For a scalar physical property $$ f^\alpha $$ per unit volume, we have

$$
\begin{equation}
\frac{d}{dt} \int_{V} f^\alpha \mathrm{d} V = \int_{V} \left[ \frac{\partial f^\alpha}{\partial t} + \nabla \cdot \left( f^\alpha \mathbf v^\alpha \right)  \right] \mathrm{d} V.
\end{equation}
$$

Applying the divergence theorem, we get the expression

$$
\begin{equation}
\frac{d}{dt} \int_{V} f^\alpha \mathrm{d} V = \int_{V} \frac{\partial f^\alpha}{\partial t} \mathrm{d} V + \int_{\partial V} f^\alpha \mathbf v^\alpha \cdot \mathbf n \mathrm{d} A
\end{equation}
$$

where $$ \partial V $$ is the boundary of the domain $$ V $$ and $$ \mathbf n $$ is the outward unit normal to the surface $$ \mathrm{d} A $$.

The spatial velocity gradient of phase $$ \alpha $$,

$$
\begin{equation}
\mathbf L^\alpha = \nabla \mathbf v^\alpha,
\end{equation}
$$ 

can be decomposed into symmetric and skew-symmetric parts as

$$
\begin{equation}
\mathbf L^\alpha = \mathbf D^\alpha + \mathbf W^\alpha,
\end{equation}
$$ 

where $$ \mathbf D^\alpha $$ and $$ \mathbf W^\alpha $$ are the rate of deformation and spin tensors, respectively, which may be expressed as

$$
\begin{equation}
\mathbf D^\alpha = \frac{1}{2} (\mathbf L^\alpha + {\mathbf L^\alpha}^\intercal) \quad \text{and} \quad \mathbf W^\alpha = \frac{1}{2} (\mathbf L^\alpha - {\mathbf L^\alpha}^\intercal).
\end{equation}
$$

# Conservation Laws

The various physical processes within a porous medium induced by external and internal factors are described mathematically using  onservation laws, which describe the evolution of physical parameters relevant to the processes. The main conservation laws for a porous medium are mass, momentum and energy balance equations.

The kinematic equations described in the previous section are used to derive the balance equations for a given porous medium. The derivation of these balance equations considers internal and external factors affecting the state of the porous medium and the interactions between the phases in the medium. This is required to ensure that the individual balance equations of the phases result in the balance equation of the whole mixture when superimposed; see Hassanizadeh and Gray (1980)[^18]. In the following sections, the balance equations of mass, momentum and energy are derived for an individual phase in a porous medium and for the mixture as a whole. The presentation follows the works of de Boer (2006)[^19] and Lewis and Schrefler (1998)[^17].

## Mass Balance

The law of conservation of mass for phase $$ \alpha $$ requires that the rate of change of mass be equal to any other mass of that phase being added to or leaving from the system, internally from other constituents or externally from other sources. The rate of change of mass $$ M^\alpha $$ of phase $$ \alpha $$ over a domain $$ V $$ is described by

$$
\begin{equation}
\frac{\mathrm{D}_\alpha M^\alpha}{\mathrm{D} t} = \frac{\mathrm{D}_\alpha}{\mathrm{D} t} \int_{V} \rho^\alpha \mathrm{d} V
\end{equation}
$$

and mass conservation requires this rate to be balanced with all mass exchanges among other phases, i.e.

$$
\begin{equation}
\frac{\mathrm{D}_\alpha}{\mathrm{D} t} \int_{V} \rho^\alpha \mathrm{d} V + \sum_{\beta} M^{\beta\alpha} = 0
\end{equation}
$$

where the second term in the above equation represents the sum of mass exchanges per unit volume from all phases $$ \beta $$ to phase $$ \alpha $$. Applying Reynold’s transport theorem to the rate of change of $$ M^\alpha $$,  a generalized mass balance equation for phase $$ \alpha $$ can be written as

$$
\begin{equation}
\frac{\mathrm{D}_\alpha \rho^\alpha}{\mathrm{D} t} + \rho^\alpha \nabla \cdot \mathbf v^\alpha + \sum_{\beta} M^{\beta\alpha} = 0.
\label{e:masbalalpha}
\end{equation}
$$ 

The general mass balance equation for a porous medium with $$ N $$ constituents is then obtained by summation of the individual mass balance equations for each phase i.e.

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \left[ \frac{\mathrm{D}_\alpha \rho^\alpha}{\mathrm{D} t} + \rho^\alpha \nabla \cdot \mathbf v^\alpha + \sum_{\beta} M^{\beta\alpha} \right] = 0.
\end{equation}
$$

The mass exchange term between the phases has the constraint 

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \sum_{\beta} M^{\beta\alpha} = 0
\label{e:massconstraint}
\end{equation}
$$ 

when summed over all the $$ N $$ constituents of the mixture, reducing the overall mass balance equation to

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \left[ \frac{\mathrm{D}_\alpha \rho^\alpha}{\mathrm{D} t} + \rho^\alpha \nabla \cdot \mathbf v^\alpha \right] = 0.
\end{equation}
$$

In equation \ref{e:masbalalpha}, the motion of a particle of phase $$ \alpha $$ is expressed relative to the same phase. In practice, it is more convenient to take one of the phases (usually the solid phase) as a reference to describe the motion of all other phases. The individual mass balance equations for these phases can then be modified by introducing their relative velocity with respect to the reference phase.

## Linear Momentum Balance

The balance of linear momentum for a given phase $$ \alpha $$ requires that the material time derivative its momentum $$ \mathbf P^\alpha $$ be in equilibrium with the sum of all internal interaction forces and external forces. The rate of change of momentum over a domain $$ V $$ is described by

$$
\begin{equation}
\frac{\mathrm{D}_\alpha \mathbf P^\alpha}{\mathrm{D} t} = \frac{\mathrm{D}_\alpha}{\mathrm{D} t} \int_{V} \rho^\alpha \mathbf v^\alpha \mathrm{d} V
\end{equation}
$$

and the balance of linear momentum requires 

$$
\begin{equation}
\frac{\mathrm{D}_\alpha}{\mathrm{D} t} \int_{V} \rho^\alpha \mathbf v^\alpha \mathrm{d} V + \sum_{\beta} \mathbf P^{\beta\alpha} = \mathbf F^\alpha
\end{equation}
$$

where the second term represents the sum internal momentum exchanges over time to phase $$ \alpha $$ from all other phases $$ \beta $$ and $$ \mathbf F^\alpha $$ represents external forces. The external forces involve body forces $$ rho^\alpha \mathbf b^\alpha $$ acting on the constituents over the volume $$ V $$ and surface forces $$ \mathbf t^\alpha $$ acting on the boundary $$ \partial V $$ i.e.

$$
\begin{equation}
\mathbf F^\alpha = \int_{V} \rho^\alpha \mathbf b^\alpha \mathrm{d} V + \int_{\partial V} \mathbf t^\alpha \mathrm{d} A
\label{e:externalforces}
\end{equation}
$$ 

Cauchy’s stress tensor $$ \mathbf \sigma^\alpha $$ and the surface tractions $$ \mathbf t^\alpha $$ of phase $$ \alpha $$ are related by

$$
\begin{equation}
\mathbf t^\alpha = \mathbf \sigma^\alpha \mathbf n
\end{equation}
$$ 

where $$ \mathbf n $$ is an outward unit normal vector on the boundary. Using \ref{e:transporttheorem}, applying the divergence theorem and considering the mass balance principle, the linear momentum balance equation for phase $$ \alpha $$ becomes

$$
\begin{equation}
\nabla \cdot \mathbf \sigma^\alpha + \rho^\alpha \mathbf b^\alpha + \sum_{\beta} \mathbf P^{\beta\alpha} = \rho^\alpha \mathbf a^\alpha.
\label{e:mombalalpha}
\end{equation}
$$

The overall linear momentum balance equation for the mixture with $$ N $$ constituents is obtained by summation of the individual phase equations i.e.

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \left[ \nabla \cdot \mathbf \sigma^\alpha + \rho^\alpha \mathbf b^\alpha + \sum_{\beta} \mathbf P^{\beta\alpha} \right] = \sum\limits_{\alpha=1}^{N} \rho^\alpha \mathbf a^\alpha.
\label{e:genmombal}
\end{equation}
$$

The sums of the partial stresses, body forces and acceleration can be represented by their total equivalents:

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \mathbf \sigma^\alpha = \mathbf \sigma, \quad \sum\limits_{\alpha=1}^{N} \rho^\alpha \mathbf b^\alpha = \rho \mathbf b \quad \text{and} \quad \sum\limits_{\alpha=1}^{N} \rho^\alpha \mathbf a^\alpha = \rho \mathbf a.
\label{e:partialandtotalsums}
\end{equation}
$$ 

The internal exchange of momentum between the phases is required to satisfy the constraint

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \sum_{\beta} \mathbf P^{\beta\alpha} = 0.
\label{e:momexchangeconstraint}
\end{equation}
$$ 

Using \ref{e:partialandtotalsums} and \ref{e:momexchangeconstraint} in \ref{e:genmombal}, the linear momentum balance equation for the mixture becomes

$$
\begin{equation}
\nabla \cdot \mathbf \sigma + \rho \mathbf b = \rho \mathbf a.
\end{equation}
$$ 

For a static condition ($$ \mathbf a = \mathbf 0 $$), this reduces to

$$
\begin{equation}
\nabla \cdot \mathbf \sigma + \rho \mathbf b = \mathbf 0.
\end{equation}
$$

## Angular Momentum Balance

The balance of angular momentum or moment of momentum states that the material time derivative of the angular momentum is equal to the moments of all external forces where the moments are referred to a certain fixed point. The angular momentum $$ \mathbf H^\alpha $$ of phase $$ \alpha $$ is given by

$$
\begin{equation}
\mathbf H^\alpha = \int_{V} \mathbf x \times \rho^\alpha \mathbf v^\alpha \mathrm{d} V
\end{equation}
$$

where $$ \mathbf x $$ is a position vector to the fixed point. The moment of the external forces using \ref{e:externalforces} is given by

$$
\begin{equation}
\mathbf M^\alpha = \int_{V} \mathbf x \times \rho^\alpha \mathbf b^\alpha \mathrm{d} V + \int_{\partial V} \mathbf x \times \mathbf t^\alpha \mathrm{d} A.
\end{equation}
$$

Angular momentum balance requires

$$
\begin{equation}
\frac{\mathrm{D}_\alpha}{\mathrm{D} t} \int_{V} \mathbf x \times \rho^\alpha \mathbf v^\alpha \mathrm{d} V = \int_{V} \mathbf x \times \rho^\alpha \mathbf b^\alpha \mathrm{d} V + \int_{\partial V} \mathbf x \times \mathbf t^\alpha \mathrm{d} A
\end{equation}
$$

where the moment of the exchanged momentum between the phases is omitted. Simplifying the above equation by applying the mass balance and momentum balance principles derived earlier gives

$$
\begin{equation}
\int_{V} \mathbf x \times \rho^\alpha \mathbf a^\alpha \mathrm{d} V = \int_{V} \mathbf x \times \rho^\alpha \mathbf a^\alpha \mathrm{d} V + \int_{V} \mathbf I \times \mathbf \sigma^\alpha \mathrm{d} V
\end{equation}
$$

where $$ \mathbf I $$ is the identity tensor. The above equation requires 

$$
\begin{equation}
\mathbf I \times \mathbf \sigma^\alpha = \mathbf 0
\end{equation}
$$

and this is satisfied if

$$
\begin{equation}
\mathbf \sigma^\alpha = (\mathbf \sigma^\alpha)^\intercal.
\end{equation}
$$ 

The total stress as the sum of the partial stresses consequently must satisfy

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \mathbf \sigma^\alpha = \sum\limits_{\alpha=1}^{N} (\mathbf \sigma^\alpha)^\intercal \; \Rightarrow \; \mathbf \sigma = \mathbf \sigma^\intercal.
\end{equation}
$$

Thus, the conservation of angular momentum proves that Cauchy’s stress tensor is symmetric. Note that if the angular momentum exchange between the phases is assumed to be non-zero, the stress tensor would not be symmetric, requiring the introduction of additional rotational degrees of freedom.

## Energy Balance

The law of conservation of energy, the first law of thermodynamics, requires that the rate of change of the internal and kinetic energies be balanced by the rate of mechanical work and heat. For phase $$ \alpha $$ in a porous medium, this is written mathematically as

$$
\begin{equation}
\frac{\mathrm{D}_\alpha E^\alpha}{\mathrm{D} t} + \frac{\mathrm{D}_\alpha K^\alpha}{\mathrm{D} t} + \sum\limits_{\beta} E^{\beta \alpha} = W^\alpha + H^\alpha
\label{e:thermodynamics}
\end{equation}
$$ 

where $$ E^\alpha $$ is the internal energy, $$ K^\alpha $$ is the kinetic energy, $$ E^{\beta \alpha} $$ is the rate of internal energy exchange from all other phases $$ \beta $$ to phase $$ \alpha $$, $$ W^\alpha $$ is the rate of mechanical energy or work and $$ H^\alpha $$ is the rate of heat energy. For a given domain $$ V $$, we have 

$$
\begin{equation}
\begin{aligned}
E^\alpha &= \int_{V} \rho^\alpha e^\alpha \mathrm{d} V \\
K^\alpha &= \int_{V} \frac{1}{2 }\rho^\alpha \mathbf v^\alpha \cdot \mathbf v^\alpha \mathrm{d} V \\
W^\alpha &= \int_{V} \mathbf v^\alpha \cdot \rho^\alpha \mathbf b^\alpha \mathrm{d} V + \int_{\partial V} \mathbf v^\alpha \cdot \mathbf t^\alpha  \mathrm{d} A \\
H^\alpha &= \int_{V} \rho^\alpha h^\alpha \mathrm{d} V - \int_{\partial V} \mathbf q^\alpha \mathrm{d} A
\end{aligned}
\label{e:energies}
\end{equation}
$$ 

where $$ e^\alpha = e^\alpha(\mathbf x,t) $$ is the specific internal energy $$ \alpha, h^\alpha = h^\alpha(\mathbf x,t) $$ is the partial energy source and $$ \mathbf q^\alpha = \mathbf q^\alpha(\mathbf x,t) $$ is the partial heat flux
vector.

Using \ref{e:energies} in \ref{e:thermodynamics}, simplifying the material time derivatives of the integrals and utilizing the mass and linear momentum balance equations in \ref{e:masbalalpha} and \ref{e:mombalalpha}, the energy balance equation for phase $$ \alpha $$ becomes

$$
\begin{equation}
\begin{aligned}
\rho^\alpha \frac{\mathrm{D}_\alpha e^\alpha}{\mathrm{D} t} - \sum\limits_{\beta} M^{\beta \alpha} \left( e^\alpha - \frac{1}{2} \mathbf v^\alpha \cdot \mathbf v^\alpha \right) + \rho^\alpha \mathbf v^\alpha \cdot \mathbf a^\alpha - \mathbf \sigma^\alpha : \mathbf L^\alpha  \\
- \mathbf v^\alpha \cdot \left( \nabla \cdot \mathbf \sigma^\alpha + \rho^\alpha \mathbf b^\alpha \right) + \nabla \cdot \mathbf q^\alpha + \sum\limits_{\beta} E^{\beta \alpha} = Q^\alpha
\end{aligned}
\label{e:enebalalpha}
\end{equation}
$$ 

where $$ Q^\alpha = \rho^\alpha h^\alpha $$ is the heat supply to phase $$ \alpha $$. The overall energy balance equation is obtained by summation of the individual energy balance equations of the constituents of the porous medium i.e. 

$$
\begin{equation}
\begin{aligned}
\sum\limits_{\alpha=1}^{N} \left[ \rho^\alpha \frac{\mathrm{D}_\alpha e^\alpha}{\mathrm{D} t} - \sum\limits_{\beta} M^{\beta \alpha} \left( e^\alpha - \frac{1}{2} \mathbf v^\alpha \cdot \mathbf v^\alpha \right) + \rho^\alpha \mathbf v^\alpha \cdot \mathbf a^\alpha - \mathbf \sigma^\alpha : \mathbf L^\alpha \right. \\
- \left. \mathbf v^\alpha \cdot \left( \nabla \cdot \mathbf \sigma^\alpha + \rho^\alpha \mathbf b^\alpha \right) + \nabla \cdot \mathbf q^\alpha + \sum\limits_{\beta} E^{\beta \alpha} \right] = \sum\limits_{\alpha=1}^{N} Q^\alpha.
\end{aligned}
\end{equation}
$$ 

If the momentum exchange between the phases is assumed to be zero, the energy balance equation reduces to 

$$
\begin{equation}
\begin{aligned}
\sum\limits_{\alpha=1}^{N} \left[ \rho^\alpha \frac{\mathrm{D}_\alpha e^\alpha}{\mathrm{D} t} - \sum\limits_{\beta} M^{\beta \alpha} \left( e^\alpha - \frac{1}{2} \mathbf v^\alpha \cdot \mathbf v^\alpha \right) - \mathbf \sigma^\alpha : \mathbf L^\alpha \right. \\
+ \left. \nabla \cdot \mathbf q^\alpha + \sum\limits_{\beta} E^{\beta \alpha} \right] = \sum\limits_{\alpha=1}^{N} Q^\alpha.
\end{aligned}
\label{e:enebal}
\end{equation}
$$ 

The total heat supply and total heat flux can be expressed as

$$
\begin{equation}
Q = \sum\limits_{\alpha=1}^{N} Q^\alpha \quad \text{and} \quad \mathbf q = \sum\limits_{\alpha=1}^{N} \mathbf q^\alpha
\end{equation}
$$

and a constraint on the energy exchange between the phases is introduced as

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \sum_{\beta} E^{\beta\alpha} = 0.
\end{equation}
$$ 

This reduces the energy balance equation to

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \left[ \rho^\alpha \frac{\mathrm{D}_\alpha e^\alpha}{\mathrm{D} t} - \sum\limits_{\beta} M^{\beta \alpha} \left( e^\alpha - \frac{1}{2} \mathbf v^\alpha \cdot \mathbf v^\alpha \right) - \mathbf \sigma^\alpha : \mathbf L^\alpha \right] + \nabla \cdot \mathbf q  = Q.
\end{equation}
$$

# Thermodynamics and Phase Change

The second law of thermodynamics (entropy inequality) is used to state the restrictions on constitutive equations. It follows from the conservation of energy (first law of thermodynamics) with the introduction of the absolute temperature.

## Entropy Inequality

The assumption of entropy inequality for each phase $$ \alpha $$ is a sufficient but restrictive condition. For the existence of dissipation mechanisms within the porous medium, an entropy inequality for all the constituents is both a necessary and sufficient condition, de Boer (2006)[^19].

For phase $$ \alpha $$,  let

$$
\begin{equation}
S^\alpha = \int_{V} \rho^\alpha s^\alpha \mathrm{d} V
\end{equation}
$$

be its entropy where $$ s^\alpha $$ is the specific entropy. With $$ T^\alpha $$ as the absolute temperature of phase $$ \alpha $$, the entropy inequality for all the constituents of the porous medium is expressed as

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \frac{\mathrm{D}_\alpha S^\alpha}{\mathrm{D} t} \geq \sum\limits_{\alpha=1}^{N} \int_{V} \frac{1}{T^\alpha} \rho^\alpha h^\alpha \mathrm{d} V - \sum\limits_{\alpha=1}^{N} \int_{\partial V} \frac{1}{T^\alpha} \mathbf q^\alpha \cdot \mathrm{d} A.
\end{equation}
$$

Performing the material time derivative in the above equation using the transport theorem, utilizing the mass balance equation and the divergence theorem, the local form of the entropy inequality becomes

$$
\begin{equation}
\sum\limits_{\alpha=1}^{N} \left[ \rho^\alpha \frac{\mathrm{D}_\alpha s^\alpha}{\mathrm{D} t} - \sum\limits_{\beta} M^{\beta \alpha} s^\alpha - \frac{1}{T^\alpha} \rho^\alpha h^\alpha + \nabla \cdot \left( \frac{1}{T^\alpha} \mathbf q^\alpha \right) \right] \geq 0.
\label{e:entropyineq}
\end{equation}
$$

The entropy inequality may also be written as a function of the Helmholtz free energy

$$
\begin{equation}
\psi^\alpha = e^\alpha - T^\alpha s^\alpha
\end{equation}
$$ 

together with the energy balance in \ref{e:enebal}. The inequality in \ref{e:entropyineq} considers a general case where the constituents have a different absolute temperature $$ T^\alpha $$. It may be simplified for the case when all the constituents have the same
absolute temperature $$ T = T^\alpha $$.

## Phase Transitions

The physical processes in a porous medium sometimes involve the transition of one phase into another such as phase change from liquid to vapor, liquid to solid or solid to liquid. These types of phase changes are referred to as first-order transitions, see de Boer and Bluhm (1999)[^20], whereas other transitions such as from a super fluid to ordinary fluid (e.g. helium) are called second-order transitions. The discussion here focuses on first-order transitions. We take a closer look here at the effect of phase transitions in a porous medium.

The balance equations in the [conservation laws](#conservation-laws) section are presented in a general form such that the effect of phase transition(s) on the conserved quantities can be considered. Consider a two-phase porous medium where phase transition from one phase to another occurs, e.g. freezing/melting. The exchange of quantities during phase change remains constrained. For instance, the mass balance equations for the individual constituents, according to \ref{e:masbalalpha}, are given by 

$$
\begin{equation}
\begin{aligned}
\frac{\mathrm{D}_\alpha \rho^\alpha}{\mathrm{D} t} + \rho^\alpha \nabla \cdot \mathbf v^\alpha + M^{\beta\alpha} &= 0 \\
\frac{\mathrm{D}_\beta \rho^\beta}{\mathrm{D} t} + \rho^\beta \nabla \cdot \mathbf v^\beta + M^{\alpha\beta} &= 0
\end{aligned}
\end{equation}
$$ 

wherein the sum on the mass exchange term is omitted since we have only one phase contributing to the mass of another. The constraint in \ref{e:massconstraint} implies

$$
\begin{equation}
M^{\alpha\beta} + M^{\beta\alpha} = 0.
\end{equation}
$$ 

Phase transitions in porous media have been studied in the past with several simplifying assumptions. The need for a rigorous mathematical and thermodynamical
treatment of such problems was clear. Phase change from liquid to gas was given a detailed thermodynamic treatment, for example, by de Boer and Kowalski (1995)[^21] and de Boer (1995)[^22], showing that the phase transition is governed by the difference of the chemical potentials of the constituents. A review of various phase change phenomena in porous media such as freezing/melting, boiling,
drying/evaporation and condensation was presented by Yortsos and Stubos (2001)[^23]. A detailed thermodynamic approach to various phase change problems can be found in Fremond (2012)[^24].

The thermodynamic equilibrium between the phases during phase change is described by the Clausius-Clapeyron equation. This equation can be derived based on the equilibrium requirement between the chemical potentials of the two phases; see Loch (1978)[^25] for the specific case of freezing and melting. For two phases $$ \alpha $$ and $$ \beta $$ undergoing phase transition, their chemical potentials are required to be in equilibrium, i.e. $$\mu^\alpha = \mu^\beta.$$ The
chemical potentials are a function of the specific entropies, the specific volumes, the pressures and the temperatures of the phases. In terms of these quantities, we have

$$
\begin{equation}
-(s^\alpha - s^\beta)\mathrm{d} T + v^\alpha \mathrm{d} p^\alpha - v^\beta \mathrm{d} p^\beta = 0
\end{equation}
$$

where $$ s^\alpha $$ and $$ s^\beta $$ are the specific entropies of the phases, $$ v^\alpha $$ and $$ v^\beta $$ their specific volumes, $$ p^\alpha $$ and $$ p^\beta $$ the pressures and $$ T $$ is the temperature, assuming the same temperature for both phases. The equation above may be rearranged to give

$$
\begin{equation}
\mathrm{d} p^\beta = \frac{v^\alpha}{v^\beta}\mathrm{d} p^\alpha - \frac{1}{v^\beta}(s^\alpha - s^\beta)\mathrm{d} T.
\end{equation}
$$

In terms of the densities $$ \rho^\alpha = 1/v^\alpha $$ and $$ \rho^\beta = 1/v^\beta $$, we have

$$
\begin{equation}
\mathrm{d} p^\beta = \frac{\rho^\beta}{\rho^\alpha}\mathrm{d} p^\alpha - \rho^\beta(s^\alpha - s^\beta)\mathrm{d} T.
\label{e:clausius1}
\end{equation}
$$ 

The change in entropy between the phases under constant pressure and temperature may be expressed as 

$$
\begin{equation}
s^\alpha - s^\beta = \frac{L}{T}
\end{equation}
$$ 

where $$ L $$ is the specific latent heat which depends on the type of phase change that occurs e.g. latent heat of fusion for melting. Using this in \ref{e:clausius1} gives

$$
\begin{equation}
\mathrm{d} p^\beta = \frac{\rho^\beta}{\rho^\alpha}\mathrm{d} p^\alpha - \frac{\rho^\beta L}{T}\mathrm{d} T.
\label{e:clausius2}
\end{equation}
$$

# Conduction Laws

The equations governing the flow of fluid and heat in a porous medium are given by Darcy’s law and Fourier’s law, respectively. We refer to these laws here as conduction laws, as used in Coussy (2004)[^13].

## Darcy’s Law

The specific discharge of fluid in a porous medium was shown to be proportional to the head loss based on experiments by Henry Darcy in 1857, Verruijt (2013)[^26]. Darcy’s law may be derived for fully saturated porous media from the fluid momentum balance equation, see for instance Whitaker (1986)[^27].

Darcy’s law relates the flow of fluid in a porous medium with respect to the solid phase as 

$$
\begin{equation}
\mathbf w = n^\mathrm{f} (\mathbf v^\mathrm{f} - \mathbf v^\mathrm{s})
\end{equation}
$$ 

where $$ n^\mathrm{f} $$ is the volume fraction of the fluid, $$ \mathbf v^\mathrm{f} $$ is the fluid velocity and $$ \mathbf v^\mathrm{s} $$ is the solid elocity. A more general form of Darcy’s law, considering the relative permeability of a phase in a medium where the permeability varies, is given by

$$
\begin{equation}
\mathbf w = \frac{k_\mathrm{r}}{\mu} \mathbf \kappa  \cdot (\nabla p^\mathrm{f} - \rho_\mathrm{f} \mathbf b - \rho_\mathrm{f} \mathbf a^\mathrm{s} - \rho_\mathrm{f} \mathbf a^{\mathrm{f} \mathrm{s}})
\end{equation}
$$

where $$ k_\mathrm{r} $$ is the relative permeability coefficient varying between 0 and 1, $$ \mu $$ is the viscosity of the fluid, $$ \mathbf \kappa $$ is the intrinsic permeability matrix of the material, $$ p^\mathrm{f} $$ is the fluid pressure, $$ \mathbf b $$ represents body forces, $$ \mathbf a^s $$ is the acceleration of the solid phase and $$ \mathbf a^{\mathrm{f} \mathrm{s}} $$ is the relative acceleration between the fluid and solid phases. The tortuosity of the pores is sometimes considered in the Darcy equation. If the inertia terms are neglected, Darcy’s law reduces to

$$
\begin{equation}
\mathbf w = \frac{k_\mathrm{r}}{\mu} \mathbf \kappa  \cdot (\nabla p^\mathrm{f} - \rho_\mathrm{f} \mathbf b).
\label{e:Darcyslaw0}
\end{equation}
$$ 

It is common to express Darcy’s law in terms of the hydraulic conductivity matrix $$ \mathbf k $$ instead of the intrinsic permeability matrix $$ \mathbf \kappa $$,  where the two are related by

$$
\begin{equation}
\mathbf k = \frac{\rho_\mathrm{f} g}{\mu} \mathbf \kappa
\label{e:permandhydcond}
\end{equation}
$$ 

in which $$ g $$ is the acceleration due to gravity. This results in

$$
\begin{equation}
\mathbf w = \frac{k_\mathrm{r}}{\rho_\mathrm{f} g} \mathbf k  \cdot (\nabla p^\mathrm{f} - \rho_\mathrm{f} \mathbf b)
\label{e:Darcyslaw}
\end{equation}
$$ 

wherein we have kept the same relative coefficient $$ k_\mathrm{r} $$ for hydraulic conductivity that varies with the porosity and degree of fluid saturation of the porous medium.

## Fourier’s Law

Thermal conduction in a porous medium is expressed using Fourier’s law which states that the rate of heat flow is proportional to the negative gradient of the temperature. Fourier’s law for the heat flux $$ \mathbf q $$ is given by 

$$
\begin{equation}
\mathbf q = -\mathbf \lambda \nabla T
\label{e:fourierslaw}
\end{equation}
$$ 

where $$ \mathbf \lambda $$ is the effective thermal conductivity matrix of the porous medium and $$ T $$ is the temperature. For isotropic thermal conductivity in a medium, the above equation becomes 

$$
\begin{equation}
\mathbf q = -\lambda \nabla T
\end{equation}
$$

where $$ \lambda $$ is the effective thermal conductivity coefficient which is a function of the individual thermal conductivities of the constituents of the porous medium and their volume fractions. Fourier’s law has a similar form both at the microscopic and macroscopic levels, Coussy (2004)[^13].

# Constitutive Laws

The balance equations presented in [Conservation Laws](#conservation-laws) are valid for any porous medium. To complete these balance equations for a specific material, a constitutive model needs to be introduced, de Souza Neto et al. (2011)[^28]. We first introduce the effective stress concept before discussing the constitutive equations required to complete the description.

## The Effective Stress Concept

The effective stress concept is widely used in porous media applications, especially in soil mechanics. The historical development of this concept is documented in de Boer and Ehlers (1990)[^29]. The concept was already conceived and studied by scientists by the end of the 19th century. A significant development with a mathematical background came later in early 20th century from the significant contributions of Paul Fillunger and especially Karl von Terzaghi; see Skempton (1960)[^30].

The main idea behind effective stress in a porous medium is separating the stress that effectively causes solid deformation, hence the name, from all other stresses in the mixture. If we consider a porous medium composed of two phases, solid (s) and fluid (f), the total stress as the sum of the partial stresses is given according to \ref{e:partialandtotalsums} by

$$
\begin{equation}
\mathbf \sigma = \mathbf \sigma^\mathrm{s} + \mathbf \sigma^\mathrm{f}.
\label{e:totalstress_sf}
\end{equation}
$$ 

The partial stresses corresponding to the fluid phase, using the volume fraction concept, can be written us 

$$
\begin{equation}
\mathbf \sigma^\mathrm{f} = n^\mathrm{f} \mathbf \sigma_\mathrm{f}
\end{equation}
$$ 

where $$ n^\mathrm{f} $$ is the volume fraction of the fluid and $$ \mathbf \sigma_\mathrm{f} $$ is the pore fluid stress. However, a distinction should be made between the partial stress of the solid phase $$ \mathbf \sigma^\mathrm{s} $$ and the effective stress $$ \mathbf \sigma^\mathrm{\prime} $$; this has been discussed, for example, by Prevost (1980)[^7]. The partial stress of the solid phase is given by 

$$
\begin{equation}
\mathbf \sigma^\mathrm{s} = \mathbf \sigma^\mathrm{\prime} + n^\mathrm{s} \mathbf \sigma_\mathrm{f}
\end{equation}
$$

where $$ n^\mathrm{s} \mathbf \sigma_\mathrm{f} $$ takes into account the effect of the pore fluid stress on the individual solid grains of the porous medium. It is assumed, in the above equation, that the contact areas between the solid grains are negligible such that the pore fluid surrounds each grain. Each solid grain is subjected to intergranular forces that are in
excess of the pore fluid stress and this is characterized by the effective stress $$ \mathbf \sigma^\mathrm{p}rime $$. The total stress for a fluid-saturated porous medium is then given by

$$
\begin{equation}
\mathbf \sigma = \mathbf \sigma^\mathrm{s} + \mathbf \sigma^\mathrm{f} = \mathbf \sigma^\mathrm{\prime} + \mathbf \sigma_\mathrm{f}.
\label{e:effstress}
\end{equation}
$$

## Stress-Strain Relations

A constitutive equation for the solid phase relates the effective stress and the strain. The constitutive stress-strain relation in a general form may be expressed as

$$
\begin{equation}
\mathrm{d} \mathbf \sigma^\prime = \mathbf D (\mathrm{d} \mathbf \varepsilon - \mathrm{d} \mathbf \varepsilon^\mathrm{c} - \mathrm{d} \mathbf \varepsilon^\mathrm{s}_\mathrm{v} - \mathrm{d} \mathbf \varepsilon^\mathrm{o})
\end{equation}
$$

where $$ \mathbf D = \mathbf D(\mathbf \sigma^\prime, \mathbf \varepsilon, \dot{\mathbf \varepsilon}) $$ is the constitutive tangent tensor, $$ \mathrm{d} \mathbf \varepsilon $$ is the total strain increment, $$ \mathrm{d} \mathbf \varepsilon^\mathrm{c} $$ is the creep strain increment, $$ \mathrm{d} \mathbf \varepsilon^\mathrm{s}_\mathrm{v} $$ is the volumetric strain increment and $$ \mathrm{d} \mathbf \varepsilon^\mathrm{o} $$ considers all other strain increments not directly associated with the effective stress. Let $$ p $$ represent the average fluid pressure from all the fluid phases in the porous medium. This pressure induces a hydrostatic stress distribution in the solid phase, thus causing a purely volumetric strain given in incremental form by

$$
\begin{equation}
\mathrm{d} \mathbf \varepsilon^\mathrm{s}_\mathrm{v} = - \mathbf I \frac{\mathrm{d} p}{3K_\mathrm{s}}
\label{e:volumetricstrain}
\end{equation}
$$ 

where $$ K_\mathrm{s} $$ is the bulk modulus of the solid skeleton. The effective stress relation in \ref{e:effstress} is usually modified by a corrective parameter known as Biot’s coefficient, $$ \alpha $$, Lewis and Schrefler (1998)[^17]. The modified effective stress equation (keeping the same notation for the modified effective stress) reads 

$$
\begin{equation}
\mathbf \sigma = \mathbf \sigma^\mathrm{\prime} + \alpha p \mathbf I
\label{e:effstress2}
\end{equation}
$$ 

where $$ \mathbf I $$ is the identity tensor. It can be shown that Biot’s coefficient takes the value

$$
\begin{equation}
\alpha = 1 - \frac{K_\mathrm{o}}{K_\mathrm{s}}
\label{e:Biotscoeff}
\end{equation}
$$ 

where $$ K_\mathrm{o} $$ is the overall bulk modulus of the porous medium. We can now simply write 

$$
\begin{equation}
\mathrm{d} \mathbf \sigma^\prime = \mathbf D (\mathrm{d} \mathbf \varepsilon - \mathrm{d} \mathbf \varepsilon^\mathrm{c} - \mathrm{d} \mathbf \varepsilon^\mathrm{o}).
\label{e:constitutive}
\end{equation}
$$ 

The constitutive tangent tensor takes various forms depending on the type of stress-strain relation employed. Some examples of constitutive laws include linear elasticity, thermoelasticity, elastoplasticity and viscoplasticity. In this thesis, we focus on linearly elastic and thermoelastic constitutive laws.

The tangent stiffness for linear elasticity (for stresses and strains in Voigt notation) is given by

$$
\begin{equation}
\mathbf D = 
\frac{E}{(1 + \nu)(1 - 2\nu)}
\left[ \begin{matrix}
\mathbf D_{11} & \mathbf 0 \\
\mathbf 0 & \mathbf D_{22}
\end{matrix} \right]
\end{equation}
$$ 

where

$$
\begin{equation}
\begin{aligned}
\mathbf D_{11} &= (1-2\nu) \mathbf I + \nu \boldsymbol{\mathit{1}}, \\
\mathbf D_{22} &= \frac{1-2\nu}{2} \mathbf I,
\end{aligned}
\end{equation}
$$ 

with $$ \boldsymbol{\mathit{1}} $$ being a matrix of ones, $$ E $$ is the Young’s modulus of the soil and $$ \nu $$ is the Poisson’s ratio. For thermoelastic material models, these parameters are usually defined as a function of temperature and/or other temperature dependent parameters.

## Compressibility of Phases

For compressible phases in a porous medium, the density of a phase may be a function of pressure, temperature and other factors. We look at the equations of state for water, the most common fluid in a porous medium, and solid skeleton. See Lewis and Schrefler (1998)[^17].

The equation of state for water is given by

$$
\begin{equation}
\rho_\mathrm{w} = \rho_{\mathrm{w}\mathrm{o}} \exp \left[ -\alpha_\mathrm{w} T + \frac{1}{K_\mathrm{w}} (p^\mathrm{w} - p^\mathrm{w}_\mathrm{o}) \right]
\label{e:eqofstatewater0}
\end{equation}
$$ 

where $$ \rho_\mathrm{w} $$ and $$ \rho_{\mathrm{w}\mathrm{o}} $$ are the current and initial densities, $$ \alpha_\mathrm{w} $$ is the thermal expansion coefficient, $$ K_\mathrm{w} $$ is the bulk modulus and $$ p^\mathrm{w} $$ and $$ p^\mathrm{w}_\mathrm{o} $$ are the current and initial pore water pressures. Performing Taylor series expansion of \ref{e:eqofstatewater0} and retaining first order terms gives

$$
\begin{equation}
\rho_\mathrm{w} = \rho_{\mathrm{w}\mathrm{o}} \left[1 -\alpha_\mathrm{w} T + \frac{1}{K_\mathrm{w}} (p^\mathrm{w} - p^\mathrm{w}_\mathrm{o}) \right]
\end{equation}
$$

which can then be used to derive

$$
\begin{equation}
\frac{1}{\rho_{\mathrm{w}\mathrm{o}}} \frac{\mathrm{D}_\mathrm{w} \rho_\mathrm{w}}{\mathrm{D} t} = \frac{1}{K_\mathrm{w}} \frac{\mathrm{D}_\mathrm{w} p^\mathrm{w}}{\mathrm{D} t} - \alpha_\mathrm{w} \frac{\mathrm{D}_\mathrm{w} T}{\mathrm{D} t}.
\label{e:eqofstatewater}
\end{equation}
$$ 

For a compressible solid phase, the material time derivative of the density may be derived from the mass balance of the solid:

$$
\begin{equation}
\frac{\mathrm{D}_\mathrm{s} (\rho^\mathrm{s} V^\mathrm{s})}{\mathrm{D} t} = 0.
\end{equation}
$$

The solid density is a function of the average pressure on the solid from all other phases $$ p^s $$, the temperature $$ T $$ and the first invariant of the effective stress $$ \text{tr}~\mathbf \sigma^\prime $$. The variation of the solid density may then be written as

$$
\begin{equation}
\frac{1}{\rho_\mathrm{s}} \frac{\mathrm{D}_\mathrm{s} \rho_\mathrm{s}}{\mathrm{D} t} = \frac{1}{K_\mathrm{s}} \frac{\mathrm{D}_\mathrm{s} p^\mathrm{s}}{\mathrm{D} t} - \alpha_\mathrm{s} \frac{\mathrm{D}_\mathrm{s} T}{\mathrm{D} t} - \frac{1}{3(n-1)K_\mathrm{s}} \frac{\mathrm{D}_\mathrm{s} (\text{tr}~\mathbf \sigma^\prime)}{\mathrm{D} t}
\end{equation}
$$

where $$ \alpha_\mathrm{s} $$ is the thermal expansion coefficient of the solid. The first term on the right hand side of the equation above represents the volumetric strain of the solid. This strain may be negligible for soils but significant for materials such as rock. Introducing a constitutive equation for the first invariant of the effective stress and using Biot’s coefficient from \ref{e:Biotscoeff}, an alternative form of the solid compressibility may be written as

$$
\begin{equation}
\frac{1}{\rho_\mathrm{s}} \frac{\mathrm{D}_\mathrm{s} \rho_\mathrm{s}}{\mathrm{D} t} = \frac{1}{1-n} \left[  \frac{\alpha-n}{K_\mathrm{s}} \frac{\mathrm{D}_\mathrm{s} p^\mathrm{s}}{\mathrm{D} t} - \alpha_\mathrm{s} (\alpha-n) \frac{\mathrm{D}_\mathrm{s} T}{\mathrm{D} t} - (1-\alpha) \nabla \cdot \mathbf v^\mathrm{s} \right].
\label{e:compressiblesolid}
\end{equation}
$$

# Coupled Problems

Different types of physical processes may occur in a porous medium depending on the type of the material and its application. Typical examples include hydraulic, mechanical, thermal and chemical processes. Two or more physical processes often occur in a porous medium leading to
what we refer to as coupled processes. We focus on hydraulic, hydro-mechanical and thermo-hydro-mechanical phenomena in soils. 

In the following sections, we discuss how the general conservation laws are used to derive the governing equations for the specific processes under consideration. To illustrate this, we assume a fluid-saturated biphasic porous medium with solid (s) and fluid (f) phases. Based on the volume fraction concept and \eqref{e:partialdensities}, the partial densities for the solid and fluid phases, $$ \rho^\mathrm{s} $$ and $$ \rho^\mathrm{f} $$, are given by

$$
\begin{equation}
\rho^\mathrm{s} = n^\mathrm{s} \rho_\mathrm{s} \quad \text{and} \quad
\rho^\mathrm{f} = n^\mathrm{f} \rho_\mathrm{f}
\label{e:partialdensities_sf}
\end{equation}
$$ 

where $$ n^\mathrm{s} $$ and $$ n^\mathrm{f} $$ are the volume fractions of the solid and fluid, respectively, and $$ \rho_\mathrm{s} $$ and $$ \rho_\mathrm{f} $$ are their real densities at the microscopic level. For a fluid-saturated porous medium, we have $$n^\mathrm{s} + n^\mathrm{f} = 1.$$ For simplicity in the following sections, we set $$ n^\mathrm{f} = n $$ and $$ n^\mathrm{s} = 1-n $$. We will refer to $$ n $$ as the porosity of the material.

### Hydraulic Processes ($$ p $$ or $$ p\text{-}v $$ Formulation)

Hydraulic processes in a porous medium are mainly described by the law of conservation of mass. The mass balance equation for the fluid phase according to \eqref{e:masbalalpha} is

$$
\begin{equation}
\frac{\mathrm{D}_\mathrm{f} \rho^\mathrm{f}}{\mathrm{D} t} + \rho^\mathrm{f} \nabla \cdot \mathbf v^\mathrm{f} = 0
\end{equation}
$$

in which we have ignored any mass exchange between the solid and fluid phases. Considering the flow of the fluid with respect to the solid phase, we write the material time derivative of $$ \rho^\mathrm{f} $$ according to \eqref{e:mtdwrtbetarel} as

$$
\begin{equation}
\frac{\mathrm{D}_\mathrm{s} \rho^\mathrm{f}}{\mathrm{D} t} - \nabla \rho^\mathrm{f} \cdot \mathbf v^{\mathrm{s} \mathrm{f}} + \rho^\mathrm{f} \nabla \cdot \mathbf v^\mathrm{f} = 0
\end{equation}
$$

which, according to \eqref{e:mtdwrtbeta}, becomes

$$
\begin{equation}
\frac{\partial \rho^\mathrm{f}}{\partial t} + \nabla \rho^\mathrm{f} \cdot \mathbf v^\mathrm{f} + \rho^\mathrm{f} \nabla \cdot \mathbf v^\mathrm{f} = 0.
\label{e:masbalfluid1}
\end{equation}
$$ 

wherein we have used $$ \mathbf v^{\mathrm{s} \mathrm{f}} = \mathbf v^\mathrm{s} - \mathbf v^\mathrm{f} $$. From \eqref{e:partialdensities_sf}, we have

$$
\begin{equation}
\frac{\partial \rho^\mathrm{f}}{\partial t} = \frac{\partial (n\rho_\mathrm{f})}{\partial t} = \frac{\partial n}{\partial t} \rho_\mathrm{f} + n\frac{\partial \rho_\mathrm{f}}{\partial t}.
\label{e:fluiddensitydt}
\end{equation}
$$ 

The porosity remains constant if there are no mechanical deformations i.e. $$ \frac{\partial n}{\partial t} = 0 $$. With this, and neglecting any spatial variations in the fluid density (i.e. $$ \nabla \rho^\mathrm{f} = 0 $$), \eqref{e:masbalfluid1} reduces to

$$
\begin{equation}
\frac{\partial \rho_\mathrm{f}}{\partial t} + \rho_\mathrm{f} \nabla \cdot \mathbf v^\mathrm{f} = 0.
\label{e:masbalfluid2}
\end{equation}
$$ 

If the fluid is assumed to be incompressible, \eqref{e:masbalfluid2} further reduces to 

$$
\begin{equation}
\nabla \cdot \mathbf v^\mathrm{f} = 0.
\end{equation}
$$ 

The fluid velocity according to Darcy’s law in this case is 

$$ 
\begin{equation}
\mathbf w = n (\mathbf v^\mathrm{f} - \mathbf v^\mathrm{s}) = n \mathbf v^\mathrm{f} 
\end{equation}
$$ 

with no mechanical deformations ($$ \mathbf v^\mathrm{s} = \mathbf 0 $$). Using \eqref{e:permandhydcond} and \eqref{e:Darcyslaw}, the fluid mass balance equation for a constant hydraulic conductivity ($$ k_\mathrm{r}=1 $$) can be written as

$$
\begin{equation}
\nabla \cdot \left[ -\frac{1}{\gamma_\mathrm{f}} \mathbf k  \cdot (\nabla p^\mathrm{f} - \rho_\mathrm{f} \mathbf b) \right]  = 0
\label{e:masbalfluidsteady}
\end{equation}
$$ 

where $$ \gamma_\mathrm{f} $$ is the unit weight of the fluid. The only flow driving forces considered here are the fluid pressure $$ p^\mathrm{f} $$ and the body forces $$ \mathbf b $$. The equation above governs the steady-state flow of fluid in a porous medium and may be
solved for the pressure as the unknown, resulting in the so called $$ p $$-formulation.

For a compressible fluid, the temporal variation of the fluid density needs to be taken into account. For instance, if our fluid is water, from the equation of state for water in \eqref{e:eqofstatewater} we may write

$$
\begin{equation}
\frac{\partial \rho_\mathrm{f}}{\partial t} = \frac{\rho_\mathrm{f}}{K_\mathrm{f}} \frac{\partial p^\mathrm{f}}{\partial t}
\label{e:compressiblefluid}
\end{equation}
$$ 

where $$ K_\mathrm{f} $$ is the bulk modulus of the fluid and isothermal conditions are assumed. Using \eqref{e:compressiblefluid} in \eqref{e:masbalfluid2}, we get

$$
\begin{equation}
\frac{n}{K_\mathrm{f}} \frac{\partial p^\mathrm{f}}{\partial t} + \nabla \cdot \mathbf w = 0
\label{e:masblafluidcompressible}
\end{equation}
$$ 

wherein we have used $$ \mathbf w = n \mathbf v^\mathrm{f} $$. Sometimes, the above equation is solved together with Darcy’s law for the pressure $$ p^\mathrm{f} $$ and Darcy’s velocity $$ \mathbf w $$ as the unknowns. The equations to be solved simultaneously in this case are

$$
\begin{equation}
\begin{aligned}
\frac{n}{K_\mathrm{f}} \frac{\partial p^\mathrm{f}}{\partial t} + \nabla \cdot \mathbf w &= 0 \\
\mathbf w + \frac{1}{\gamma_\mathrm{f}} \mathbf k  \cdot (\nabla p^\mathrm{f} - \rho_\mathrm{f} \mathbf b) &= 0
\end{aligned}
\end{equation}
$$ 

which results in the so called $$ p\text{-}v $$ formulation.

### Hydro-Mechanical Processes ($$ u\text{-}p $$ Formulation)

Hydro-mechanical processes couple the flow of fluid in a porous medium with solid deformation. The governing equations describing the coupling are derived by superposition of the individual linear momentum and mass balance equations of the solid and fluid phases.

From \eqref{e:masbalfluid1} and \eqref{e:fluiddensitydt}, with no spatial variations in fluid density, the mass balance equation for the fluid phase is given by

$$
\begin{equation}
\rho_\mathrm{f}\frac{\partial n}{\partial t} + n\frac{\partial \rho_\mathrm{f}}{\partial t} + n\rho_\mathrm{f} \nabla \cdot \mathbf v^\mathrm{f} = 0.
\label{e:masbalfluidHM}
\end{equation}
$$ 

The mass balance equation for the solid phase, based on , is given by

$$
\begin{equation}
\frac{\mathrm{D}_\mathrm{s} \rho^\mathrm{s}}{\mathrm{D} t} + \rho^\mathrm{s} \nabla \cdot \mathbf v^\mathrm{s} = 0.
\end{equation}
$$

From \eqref{e:partialdensities_sf} we have $$ \rho^\mathrm{s} = (1-n) \rho_\mathrm{s} $$. Using this in the above equation, and neglecting spatial variations in the porosity and the solid density, gives

$$
\begin{equation}
-\rho_\mathrm{s} \frac{\partial n}{\partial t} + (1-n) \frac{\partial \rho_\mathrm{s}}{\partial t} + (1-n) \rho_\mathrm{s} \nabla \cdot \mathbf v^\mathrm{s} = 0.
\label{e:masbalsolidHM}
\end{equation}
$$ 

Dividing \eqref{e:masbalfluidHM} by $$ \rho_\mathrm{f} $$ and \eqref{e:masbalsolidHM} by $$ \rho_\mathrm{s} $$ and adding the two equations gives the overall mass balance equation for the fluid-saturated porous medium as

$$
\begin{equation}
\frac{(1-n)}{\rho_\mathrm{s}} \frac{\partial \rho_\mathrm{s}}{\partial t} + (1-n) \nabla \cdot \mathbf v^\mathrm{s} + \frac{n}{\rho_\mathrm{f}} \frac{\partial \rho_\mathrm{f}}{\partial t} + n \nabla \cdot \mathbf v^\mathrm{f} = 0.
\label{e:masbalHM1}
\end{equation}
$$ 

Rearranging the above equation gives

$$
\begin{equation}
\nabla \cdot \mathbf v^\mathrm{s} + \frac{(1-n)}{\rho_\mathrm{s}} \frac{\partial \rho_\mathrm{s}}{\partial t} +  \frac{n}{\rho_\mathrm{f}} \frac{\partial \rho_\mathrm{f}}{\partial t} + \nabla \cdot \mathbf w = 0
\label{e:masbalHM2}
\end{equation}
$$ 

where $$ \mathbf w = n (\mathbf v^\mathrm{f} - \mathbf v^\mathrm{s}) $$ is Darcy’s velocity. Assuming isothermal conditions and water as the fluid, the compressibility of the fluid is given by \eqref{e:compressiblefluid} and from \eqref{e:compressiblesolid} we get for the solid phase

$$
\begin{equation}
\frac{1-n}{\rho_\mathrm{s}} \frac{\partial \rho_\mathrm{s}}{\partial t} = \frac{\alpha-n}{K_\mathrm{s}} \frac{\partial p^\mathrm{f}}{\partial t} - (1-\alpha) \nabla \cdot \mathbf v^\mathrm{s}
\label{e:compressiblesolidHM}
\end{equation}
$$ 

where for a single fluid phase we have set $$ p^\mathrm{s} = p^\mathrm{f} $$. Equation \eqref{e:masbalHM2}, based on \eqref{e:compressiblefluid} and \eqref{e:compressiblesolidHM}, can be rewritten as

$$
\begin{equation}
\alpha \nabla \cdot \mathbf v^\mathrm{s} + \left( \frac{\alpha-n}{K_\mathrm{s}} + \frac{n}{K_\mathrm{f}} \right)  \frac{\partial p^\mathrm{f}}{\partial t} + \nabla \cdot \mathbf w = 0.
\label{e:masbalHM}
\end{equation}
$$ 

For incompressible solid and fluid phases ($$ 1/K_\mathrm{s} = 1/K_\mathrm{f} = 0 $$ and $$ \alpha=1 $$), the mass balance equation reduces to 

$$
\begin{equation}
\nabla \cdot \mathbf v^\mathrm{s} + \nabla \cdot \mathbf w = 0.
\label{e:masbalHMincomp}
\end{equation}
$$ 

The linear momentum balance equations for the solid and fluid phases, according to \eqref{e:mombalalpha}, assuming a static condition and no momentum exchange between the phases, are given by 

$$
\begin{equation}
\begin{aligned}
\nabla \cdot \mathbf \sigma^\mathrm{s} + \rho^\mathrm{s} \mathbf b^\mathrm{s}  &= \mathbf 0 \\
\nabla \cdot \mathbf \sigma^\mathrm{f} + \rho^\mathrm{f} \mathbf b^\mathrm{f}  &= \mathbf 0.
\end{aligned}
\end{equation}
$$ 

Summation of the two equations above and use of \eqref{e:partialandtotalsums}, \eqref{e:totalstress_sf} and \eqref{e:effstress2}, gives the momentum balance equation for the whole medium as

$$
\begin{equation}
\nabla \cdot (\mathbf \sigma^\prime + \alpha p^\mathrm{f} \mathbf I) + \rho \mathbf b = \mathbf 0
\label{e:mombalHM}
\end{equation}
$$ 

wherein the total density of the porous medium is 

$$
\begin{equation}
\rho = \rho^\mathrm{s} + \rho^\mathrm{f} = (1-n)\rho_\mathrm{s} + n \rho_\mathrm{f}.
\end{equation}
$$ 

For coupled hydro-mechanical (HM) processes in a porous medium, the mass balance equation in \eqref{e:masbalHM} and the linear momentum balance equation in \eqref{e:mombalHM}  can be solved simultaneously for the displacement and pressure field variables. This results in what is known as a $$ u\text{-}p $$ formulation. Sometimes these equations are solved simultaneously with Darcy’s equation to obtain the displacement, pressure and Darcy’s velocity, leading to the so-called $$ u\text{-}p\text{-}v $$ formulation.

### Thermo-Hydro-Mechanical Processes ($$ u\text{-}p\text{-}T $$ Formulation)

Thermo-hydro-mechanical (THM) processes in a porous medium couple heat transfer and fluid flow with the deformation of solid. The governing equations describing the coupling are derived by superposition of the individual linear momentum, mass and energy balance equations of
constituent phases.

We consider a fluid-saturated porous medium again. The linear momentum balance equation in this case is the same as in \eqref{e:mombalHM}. The overall mass balance equation is derived from \eqref{e:masbalHM2} by considering non-isothermal conditions for the compressibilities of the solid and fluid phases. Based on \eqref{e:eqofstatewater} and \eqref{e:compressiblesolid}, we get 

$$
\begin{equation}
\begin{aligned}
\frac{1-n}{\rho_\mathrm{s}} \frac{\partial \rho_\mathrm{s}}{\partial t} &= \frac{\alpha-n}{K_\mathrm{s}} \frac{\partial p^\mathrm{f}}{\partial t} - (\alpha-n)\alpha_\mathrm{s} \frac{\partial T}{\partial t} - (1-\alpha) \nabla \cdot \mathbf v^\mathrm{s} \\
\frac{n}{\rho_\mathrm{f} }\frac{\partial \rho_\mathrm{f}}{\partial t} &= \frac{n}{K_\mathrm{f}} \frac{\partial p^\mathrm{f}}{\partial t} - n\alpha_\mathrm{w} \frac{\partial T}{\partial t}.
\end{aligned}
\label{e:compressibleTHM}
\end{equation}
$$ 

Using \eqref{e:compressibleTHM} in \eqref{e:masbalHM2} and simplifying gives the overall mass balance equation for a fluid-saturated porous
medium subjected to THM coupled processes as

$$
\begin{equation}
\alpha \nabla \cdot \mathbf v^\mathrm{s} + \left( \frac{\alpha-n}{K_\mathrm{s}} + \frac{n}{K_\mathrm{f}} \right) \frac{\partial p^\mathrm{f}}{\partial t} - \alpha_\mathrm{o} \frac{\partial T}{\partial t} + \nabla \cdot \mathbf w = 0
\label{e:masbalTHM}
\end{equation}
$$ 

where $$ \alpha_\mathrm{o} = n\alpha_\mathrm{w} + (\alpha-n)\alpha_\mathrm{s} $$ is the overall thermal expansion coefficient of the porous medium.

The energy balance equation for a single phase, neglecting any mass, momentum and energy exchanges between the solid and fluid phases, is obtained from \eqref{e:enebalalpha} as

$$
\begin{equation}
\rho^\alpha \frac{\mathrm{D}_\alpha e^\alpha}{\mathrm{D} t} - \mathbf \sigma^\alpha : \mathbf L^\alpha + \nabla \cdot \mathbf q^\alpha = Q^\alpha
\end{equation}
$$

The individual energy balance equations for the solid and fluid phases are then written as 

$$
\begin{equation}
\begin{aligned}
\rho^\mathrm{s} \frac{\mathrm{D}_\mathrm{s} e^\mathrm{s}}{\mathrm{D} t} - \mathbf \sigma^\mathrm{s} : \mathbf L^\mathrm{s} + \nabla \cdot \mathbf q^\mathrm{s} = Q^\mathrm{s} \\
\rho^\mathrm{f} \frac{\mathrm{D}_\mathrm{f} e^\mathrm{f}}{\mathrm{D} t} - \mathbf \sigma^\mathrm{f} : \mathbf L^\mathrm{f} + \nabla \cdot \mathbf q^\mathrm{f} = Q^\mathrm{f}.
\end{aligned}
\end{equation}
$$ 

Viscous dissipation may be significant in applications where the material flows at high rates e.g. due to injection or molding in polymer processing. For the applications of interest in this thesis, it may be neglected. With this assumption and taking all material time derivatives with respect to the solid phase, using \eqref{e:mtdwrtbetarel}, the individual balance equations become 

$$
\begin{equation}
\begin{aligned}
\rho^\mathrm{s} \frac{\mathrm{D}_\mathrm{s} e^\mathrm{s}}{\mathrm{D} t} + \nabla \cdot \mathbf q^\mathrm{s} = Q^\mathrm{s} \\
\rho^\mathrm{f} \frac{\mathrm{D}_\mathrm{s} e^\mathrm{f}}{\mathrm{D} t} + \rho^\mathrm{f} \nabla e^\mathrm{f} \cdot (\mathbf v^\mathrm{f} - \mathbf v^\mathrm{s}) + \nabla \cdot \mathbf q^\mathrm{f} = Q^\mathrm{f}
\end{aligned}
\label{e:enebalTHM0}
\end{equation}
$$ 

The specific internal energies for the solid and fluid phases as a function of temperature are given by 

$$
\begin{equation}
e^\mathrm{s} = c_\mathrm{s} T \quad \text{and} \quad e^\mathrm{f} = c_\mathrm{f} T
\end{equation}
$$ 

where $$ c_\mathrm{s} $$ and $$ c_\mathrm{f} $$ are their respective specific heat capacities.
Applying these to \eqref{e:enebalTHM0} gives 

$$
\begin{equation}
\begin{aligned}
\rho^\mathrm{s} c_\mathrm{s} \frac{\mathrm{D}_\mathrm{s} T}{\mathrm{D} t} + \nabla \cdot \mathbf q^\mathrm{s} = Q^\mathrm{s} \\
\rho^\mathrm{f} c_\mathrm{f} \frac{\mathrm{D}_\mathrm{s} T}{\mathrm{D} t} + \rho^\mathrm{f} c_\mathrm{f} \nabla T \cdot (\mathbf v^\mathrm{f} - \mathbf v^\mathrm{s}) + \nabla \cdot \mathbf q^\mathrm{f} = Q^\mathrm{f}.
\end{aligned}
\label{e:enebalTHM1}
\end{equation}
$$ 

Summation of the individual balance equations gives the overall energy balance equation for the porous medium as

$$
\begin{equation}
(\rho^\mathrm{s} c_\mathrm{s} + \rho^\mathrm{f} c_\mathrm{f}) \frac{\mathrm{D}_\mathrm{s} T}{\mathrm{D} t} + \rho^\mathrm{f} c_\mathrm{f} \nabla T \cdot (\mathbf v^\mathrm{f} - \mathbf v^\mathrm{s}) + \nabla \cdot \mathbf q = Q
\label{e:enebalTHM2}
\end{equation}
$$ 

wherein we have implied 

$$
\begin{equation}
\begin{aligned}
\mathbf q &= \mathbf q^\mathrm{s} + \mathbf q^\mathrm{f} \\
Q &= Q^\mathrm{s} + Q^\mathrm{f}
\end{aligned}
\end{equation}
$$ 

for the total heat flux and heat supply, respectively.

Defining the effective heat capacity of the medium as

$$
\begin{equation}
(\rho c)_\mathrm{eff} = \rho^\mathrm{s} c_\mathrm{s} + \rho^\mathrm{f} c_\mathrm{f} = (1-n)\rho_\mathrm{s} c_\mathrm{s} + n \rho_\mathrm{f} c_\mathrm{f}
\end{equation}
$$

and noting that $$ \mathbf w = n (\mathbf v^\mathrm{f} - \mathbf v^\mathrm{s}) $$ is Darcy’s
velocity, \eqref{e:enebalTHM2} is further simplified to obtain the energy balance equation for the medium as

$$
\begin{equation}
(\rho c)_\mathrm{eff} \frac{\mathrm{D}_\mathrm{s} T}{\mathrm{D} t} + \rho_\mathrm{f} c_\mathrm{f}  \mathbf w \cdot \nabla T + \nabla \cdot \mathbf q = Q.
\label{e:enebalTHM3}
\end{equation}
$$ 

The material time derivative of the temperature with respect to the solid phase is given by

$$
\begin{equation}
\frac{\mathrm{D}_\mathrm{s} T}{\mathrm{D} t} = \frac{\partial T}{\partial t} + \nabla T \cdot \mathbf v^\mathrm{s}.
\end{equation}
$$ 

For the applications of interest in this thesis, the convective heat flux in the solid phase is usually negligible i.e. $$ \nabla T \cdot \mathbf v^\mathrm{s} \approx $$ 0. With this assumption and using Fourier’s law, \eqref{e:fourierslaw}, in \eqref{e:enebalTHM3}, the energy balance equation for the medium becomes

$$
\begin{equation}
(\rho c)_\mathrm{eff} \frac{\partial T}{\partial t} + \rho_\mathrm{f} c_\mathrm{f}  \mathbf w \cdot \nabla T - \nabla \cdot (\mathbf \lambda \nabla T) = Q.
\label{e:enebalTHM}
\end{equation}
$$

For THM coupled processes in a porous medium, the linear momentum, mass and energy conservation laws in \eqref{e:mombalHM}, \eqref{e:masbalTHM} and \eqref{e:enebalTHM}, respectively, may be solved simultaneously for the displacement, pressure and temperature field variables. This results in what is usually referred to as a $$ u\text{-}p\text{-}T $$ formulation.

**References**

[^1]: de Boer, R. and Ehlers, W. A historical review of the formulation of porous media theories. *Acta Mechanica*, 74(1-4):1-8, 1988.
[^2]: de Boer, R. Reflections on the development of the theory of porous media. *Applied Mechanics Reviews*, 56(6):R27{R42, 2003.
[^3]: de Boer, R. Theory of porous media - past and present. *ZAMM-Journal of Applied Mathematics and Mechanics*/*Zeitschrift fur Angewandte Mathematik undMechanik*, 78(7):441-466, 1998.
[^4]: Green, A. E. and Naghdi, P. M. A theory of mixtures. *Archive for Rational Mechanics and Analysis*, 24(4):243-263, 1967.
[^5]: Whitaker, S. Advances in theory of fluid motion in porous media. *Industrial & Engineering Chemistry*, 61(12):14-28, 1969.
[^6]: Whitaker, S. Simultaneous heat, mass, and momentum transfer in porous media: a theory of drying. *Advances in Heat Transfer*, 13:119-203, 1977.
[^7]: Prevost, J. H. Mechanics of continuous porous media. *International Journal of Engineering Science*, 18(6):787-800, 1980.
[^8]: Bedford, A. and Drumheller, D. S. Theories of immiscible and structured mixtures. *International Journal of Engineering Science*, 21(8):863-960, 1983.
[^9]: Hassanizadeh, S. M. Derivation of basic equations of mass transport in porous media, part 1. macroscopic balance laws. *Advances in Water Resources*, 9(4):196-206, 1986.
[^10]: Bowen, R. M. Incompressible porous media models by use of the theory of mixtures. *International Journal of Engineering Science*, 18(9):1129-1148, 1980.
[^11]: Bowen, R. M. Compressible porous media models by use of the theory of mixtures. *International Journal of Engineering Science*, 20(6):697-735, 1982.
[^12]: Coussy, O., Dormieux, L., and Detournay, E. From mixture theory to Biot's approach for porous media. *International Journal of Solids and Structures*, 35(34):4619-4635, 1998.
[^13]: Coussy, O. *Poromechanics*. John Wiley & Sons, 2004.
[^14]: Vadasz, P. *Emerging Topics in Heat and Mass Transfer in Porous Media: From Bioengineering and Microelectronics to Nanotechnology*, Volume 22. Springer Science & Business Media, 2008.
[^15]: Ehlers, W. and Bluhm, J. *Porous Media: Theory, Experiments and Numerical Applications*. Springer Science & Business Media, 2013.
[^16]: Bluhm, J. and de Boer, R. The volume fraction concept in the porous media theory. *ZAMM-Journal of Applied Mathematics and Mechanics/Zeitschrift fur Angewandte Mathematik und Mechanik*, 77(8):563-577, 1997.
[^17]: Lewis, R. W. and Schrefler, B. A. *The Finite Element Method in the Static and Dynamic Deformation and Consolidation of Porous Media*. Wiley, 1998.
[^18]: Hassanizadeh, M. and Gray, W. G. General conservation equations for multiphase systems: 3. constitutive theory for porous media flow. *Advances in Water Resources*, 3(1):25-40, 1980.
[^19]: de Boer, R. *Trends in Continuum Mechanics of Porous Media*, Volume 18. Springer Science & Business Media, 2006.
[^20]: de Boer, R. and Bluhm, J. Phase transitions in gas-and liquid-saturated porous solids. *Transport in Porous Media*, 34(1-3):249-267, 1999.
[^21]: de Boer, R. and Kowalski, S. Thermodynamics of fluid-saturated porous media with a phase change. *Acta Mechanica*, 109(1-4):167-189, 1995.
[^22]: de Boer, R. Thermodynamics of phase transitions in porous media. *Applied Mechanics Reviews*, 48(10):613-622, 1995.
[^23]: Yortsos, Y. C. and Stubos, A. K. Phase change in porous media. *Current Opinion in Colloid & Interface Science*, 6(3):208-216, 2001.
[^24]: Fremond, M. *Phase Change in Mechanics*, Volume 13. Springer Science & Business Media, 2012.
[^25]: Loch, J. Thermodynamic equilibrium between ice and water in porous media. *Soil Science*, 126(2):77-80, 1978.
[^26]: Verruijt, A. *Theory and Problems of Poroelasticity*. Delft University of Technology, 2013.
[^27]: Whitaker, S. Flow in porous media I: A theoretical derivation of Darcy's law. *Transport in Porous Media*, 1(1):3-25, 1986.
[^28]: de Souza Neto, E. A., Peric, D., and Owen, D. R. J. *Computational Methods for Plasticity: Theory and Applications*. John Wiley & Sons, 2011.
[^29]: de Boer, R. and Ehlers, W. The development of the concept of effective stresses. *Acta Mechanica*, 83(1-2):77-92, 1990.
[^30]: Skempton, A. W. Terzaghi's discovery of effective stress. *From Theory to Practice in Soil Mechanics: Selections from the Writings of Karl Terzaghi*, pages 42-53, 1960.
