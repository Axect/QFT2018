---
title: "Path Integral Study Note"
author: [Tae Geun Kim]
date: 2018-07-27
subject: "Markdown"
keywords: [Markdown, Example]
subtitle: "Refer to U.Mosel, Path Integrals in Field Theory"
titlepage: true
titlepage-color: 06386e
titlepage-text-color: ffffff
titlepage-rule-color: ffffff
titlepage-rule-height: 2
...

\newcommand{\OOD}[2]{\dfrac{d^2 #1}{d #2^2}}
\newcommand{\PD}[2]{\dfrac{\partial #1}{\partial #2}}
\newcommand{\PPD}[2]{\dfrac{\partial^2 #1}{\partial #2^2}}

\newcommand{\Sbk}[1]{\left( #1 \right)}
\newcommand{\Mbk}[1]{\left\{ #1 \right\}}
\newcommand{\Bbk}[1]{\left[ #1 \right]}

\newcommand{\Real}{\mathbb{R}}
\newcommand{\Complex}{\mathbb{C}}
\newcommand{\Rational}{\mathbb{Q}}
\newcommand{\Integer}{\mathbb{Z}}
\newcommand{\Natural}{\mathbb{N}}

\renewcommand{\O}{\mathcal{O}}
\newcommand{\HOT}[1]{\O\Sbk{#1}}
\newcommand{\eps}{\epsilon}
\newcommand{\Exist}[2]{\tensor[^\exists]{#1}{#2}}

\newcommand{\Commutator}[2]{\left[ #1, #2 \right]}
\newcommand{\ACommutator}[2]{\left\{ #1, #2 \right\}}
\newcommand{\PB}[2]{\left\{ #1, #2 \right\}}
\newcommand{\IntX}{\int{d^3x}\hs}
\newcommand{\IntP}{\int{d^3p}\hs}


\newpage\null\thispagestyle{empty}\newpage

# The Path Integral in Quantum Theory

## 1.1 Propagator of the Schrödinger Equation

The non-relativistic Schrödinger equation with one dimensional potential $V(x)$ :

\begin{equation}
  H\psi(x,t) = - \frac{\hbar^2}{2m} \frac{\partial^2 \psi(x,t)}{\partial x^2} + V(x)\psi(x,t) = i\hbar \frac{\partial \psi(x,t)}{\partial t}
\end{equation}

What can obtain from schrödinger equation?

* the wave function $\psi(x,t)$ if we know $\psi(x,t_0)$ at the earlier time $t_0 < t$.

Rewrite Schrödinger eq :

\begin{equation}
  \left(i\hbar \frac{\partial}{\partial t} - H \right) \psi(x,t) = 0
\end{equation}

Next, we consider the function $K(x,t;x_i,t_i)$ which is defined as a solution of the equation :

\begin{equation}
  \left(i\hbar \PD{}{t} - H \right) K(x,t;x_i,t_i) = i\hbar \delta(x - x_i)\delta(t - t_i)
\end{equation}

What is $K$?

* the **Green's function** of the Schrödinger equation 
* or often called the **propagator**

Initial condition of $K$ :

\begin{equation}
  K(x,t_i + 0; x_i, t_i) = \delta(x - x_i)
\end{equation}

The solution for $t > t_i$ (Huygen's principle) of the Schrödinger equation :

\begin{equation}
  \psi(x,t) = \int K(x,t; x_i,t_i) \psi(x_i, t_i) dx_i
\end{equation}

