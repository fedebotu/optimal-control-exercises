# Optimal Control Exercises
[![made-with-latex](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)](https://www.latex-project.org/)

## 🗂 Contents
I uploaded this repository as Optimal Control coursework for KAIST.
This repo contains some exercise solutions for Daniel Liberzon's _Calculus of Variations and Optimal Control Theory: A Concise Introduction_ book and other problems.

## 🖼️ Examples
<p align="center">
  <img src="https://github.com/Juju-botu/optimal-control-exercises/blob/main/images/example_screenshot0.png" width=600 alt="Example screenshot0">
</p>

<p align="center">
  <img src="https://github.com/Juju-botu/optimal-control-exercises/blob/main/images/example_screenshot.png" width=600  alt="Example screenshot">
</p>

## 📬 Feedback
If you would like to contribute to this repository by improving, correcting solutions or adding new exercises, feel free to raise an `Issue` or to contribute with a `Pull Request`!

## 📜 Exercise List
Here is the list of exercises divided by lectures, so they can be more easily searched. Equations are left in Latex and will be hopefully displayed by Github in the future.
- [Lecture 1](#lecture-1): _Introduction_: path optimization vs. point optimization; basic analysis; basic facts from finite-dimensional optimization
- [Lecture 2](#lecture-2): _Calculus of variations_: examples of variational problems; Euler-Lagrange equation; Hamiltonial formalism and Legendre
transformation; mechanical interpretation; constraints; second variation and Legendre’s necessary condition; weak and strong extrema; conjugate points and sufficient conditions
- [Lecture 3](#lecture-3): _From Calculus of Variations to Optimal Control_ : statement of the optimal control problem; variational argument and preview of the maximum principle
- [Lecture 4](#lecture-4): _The Maximum Principle_: statement and proof of the maximum principle; relation to Lie brackets; bang-bang and singular optimal
controls; dynamic programming; sufficient conditions for optimality
- [Lecture 5](#lecture-5): _The Hamilton-Jacobi-Bellman equation_: HJB equations; viscosity solutions of the HJB equation
- [Lecture 6](#lecture-6): _The Linear Quadratic Regulator_: LQR problems

# Lecture 1

Exercise 1.13
-------------

*Prove the above lemma: \"If scalar sequence is monotonically
nondecreasing and bounded above, then it converges. Similarly, if a
scalar sequence is monotonically nonincreasing and bounded below, then
it converges.\"*


Exercise 1.15
-------------

*Devise a set X whose supremum exists and find its supremum. What is the
maximum of the set? Do the same for the infimum.*

Exercise 1.17
-------------

*Devise a sequence $(x_k)_{k=1}^{\infty}$ whose upper limit exists and
find its upper limit. Do the same for the infimum.*\

Exercise 1.24
-------------

*Devise examples of an open set and a closed set.*\


Exercise 1.68
-------------

*Prove the two following propositions.*\
\
**Proposition 1 (First-order necessary condition for constrained
optimality):** Suppose that $f$ is a $\mathcal{C}^1$ (continuously
differentiable) function and $x^*$ is its local minimum. Then,
$$\langle \nabla f (x^*), d  \rangle \geq 0$$ for all feasible
directions $d$.\
**Proposition 2 (Second-order necessary condition for constrained
optimality):** Suppose that $f$ is a $\mathcal{C}^2$ (continuously
differentiable) function and $x^*$ is its local minimum. Then,
$$d^T \nabla ^2 f(x^*) d \geq 0$$ for all feasible directions $d$ such
that $$\langle \nabla f (x^*), d \rangle = 0$$\

Exercise 1.69
-------------

*Suppose that $f$ is a $\mathcal{C}^2$ function and $x^*$ us a point of
its domain at which we have $\langle\nabla f(x^*),d \rangle \geq 0$ and
$d^T \nabla^2 f(x^*)d > 0$ for every nonzero feasible direction d. Is
$x^*$ necessarily a local minimum of f? Prove or give a
counterexample.*\

Exercise 1.78
-------------

*Give an example where a local minimum $x^*$ is not a regular point and
the above necessary condition (namely first-order necessary condition
for constrained optimality) is false (justify both of these claims).*\

Exercise 1.81
-------------

*Prove that the set of continuous functions
$f:[a,b] \to \mathbb{R}, f \in \mathcal{C}^0$ is a vector space with
typical addition and scalar multiplication.*\

Exercise 1.84
-------------

*For $y \in \mathcal{C}^0$, define:*
$$\mid\mid y \mid \mid _{\mathcal{L}_p} := \left( \int_a^b \mid y(x) \mid ^p dx \right) ^{1/p}$$
*where $p$ is a positive integer and $a, b \in \mathbb{R}$ with $a < b$.
Prove that it is an inner product on the vector space $\mathbb{C}^0$*\

Exercise 1.85
-------------

*For $x, y \in \mathcal{C}^0$, define*
$$\langle x, y \rangle = \int_a^b x(t)y(t) dt$$ *where
$a, b \in \mathbb{R}$ with $a < b$. Prove that it is an inner product on
the vector space $\mathcal{C}^0$.*\

Exercise 1.96
-------------

*Consider the space $\mathcal{C}^0([0,1]) \to \mathbb{R}$, let
$g : \mathbb{R} \to \mathbb{R}$ be a $\mathcal{C}^1$ function, and
define the functional $J$ on $V$ by $J(y) = \int_0^1 g'(y(x))dx$. Show
that its first variation exists and it is given by the formula*
$$\delta J\med_y (\eta) = \int_0^1 g'(y(x)) \eta (x) dx$$\

# Lecture 2

Exercise 2.4
------------

*Find another example of a variational problem. Describe it verbally
first, then formalize it by specifying admissible curves and giving an
expression for the functional to be minimized or maximized. You do not
need to solve it.*\

Exercise 2.21
-------------

*Find an extremal for the problem*
$$\min\limits_{y:[0,1] \to \mathbb{R}} J(y) = \int_0^1 y(x)^2 (y'(x))^2 dx \hspace{0.5cm} \text{subject to}\hspace{0.5cm} y(0) = 0, y(1) = 1$$\

Exercise 2.22
-------------

*Find an extremal for the problem*
$$\min\limits_{y:[0,1] \to \mathbb{R}} J(y) = \int_0^1 \{ (y'(x))^2 + 2y(x)e^x \} dx \hspace{0.5cm} \text{subject to} \hspace{0.5cm} y(0) = 0, y(1) = 1$$\

Exercise 2.27 (The Brachistochrone Problem)
-------------------------------------------

*Use the no $x$ result to show that extremals for the brachistochrone
problem are indeed given by*
$$x(\theta) = a +c (\theta - sin(\theta), \hspace{0.5cm} y(\theta) = c(1 - cos(\theta))$$
*where the parameter $\theta$ takes values between 0 and $2\pi$ and
$c > 0$ is constant.*

Exercise 2.30
-------------

*Confirm directly from the equations (2.10), (2.11), 2.12) (Hamilton's
canonical equations) that in the \"no y\" case $p$ is constant along
extremals and in the \"no x\" case $H$ is constant along extremals.*\

Exercise 2.36
-------------

*Find the curve $y^*$ that minimizes*
$$J(y) = \frac{1}{2} \int_0^1 y^' (x)^2 dx$$ *subject to the constraint*
$$\int_0^1 y(x)dx = \frac{1}{6}$$\

Exercise 2.37 (Dido's Problem)
------------------------------

*Show that optimal curves for Dido's problem are circular arcs.*\

Exercise 2.38 (The Catenary Problem)
------------------------------------

*Show that the optimal curves for the catenary problem satisfy*
$$y(x) = c \cosh{x/c}, \hspace{0.5cm} c>0$$\

Exercise 2.47
-------------

*Is Legendre's necessary condition satisfied by the admissible extremal
for the problem minimizing*
$$J(y) = \int_0^2 \sqrt{1 + y(x)^2 y'(x)^2} dx$$ *subject to $y(0) = 1$
and $y(2) = 3$? Find $L_{y'y'}(x,y(x),y'(x))$ explicitly.*\

# Lecture 3

Exercise 3.24
-------------

*Consider the problem*
$$u^* := \argmin_{u: [0,1] \to \mathbb{R}} J(u) := \frac{1}{2} \int_0^1 \left( x(t)^2 + Pu(t)^2 \right) dt$$

*subject to*
$$\dot{x}(t) = u(t), \hspace{0.5cm} x(0) = 1, \hspace{0.5cm} x(1) = \text{free}$$
*where $P>0$ us a weighting parameter. Find an optimal solution $u^*$
and $x^*$ using the Euler-Lagrange condition.*\
\
*Discuss how the solution changes as $P \to \infty$ and $P \to 0$.
Provide an intuitive explanation of the phenomenon.*\


# Lecture 4

Exercise 4.10
-------------

*Solve the problem*

$$\begin{aligned}
    &u^* := \argmin_{u:[0,t_f] \to [-1, 1]} J := t_f \\
    &\text{subject to} \\
    &\begin{cases}
        &\Dot{x}_1(t) = -4 x_1(t) + 2x_2(t) + 2u(t)\\
        &\Dot{x}_2(t) = 3x_1(t) -3x_2(t)
    \end{cases}
    \smallspace
    \begin{cases}
        &x_1(0) = x_0 \smallspace x_2(0) = 0 \\
        &x_1(t_f) = 0, \smallspace x_2(t_f) = 0
    \end{cases}\end{aligned}$$\


Exercise 4.11 (Linear-quadratic problem)
----------------------------------------

*Solve the problem*

$$\begin{aligned}
    &u^* := \argmin_{u:[0,T] \to \mathbb{R}} J(u) := \frac{1}{2}q \cdot x(T)^2 + \frac{1}{2} \int_0^T u(t) ^2 dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = ax(t) + bu(t), \smallspace x(0) = x_0\end{aligned}$$

*where a, b are given nonzero scalars, $x_0 \in \mathbb{R}$ is an
initial state, $T > 0$ is a fixed final time, and $q > 0$ is a given
positive scalar.*\

Exercise 4.12 (Control of production and consumption)
-----------------------------------------------------

*Suppose we own a factory whose output we can control. Let us begin to
construct a mathematical model by setting*

1.  *$x(t)$: amount of output produced at time $t \in [0,T]$*

2.  *$u(t)$: fraction of output reinvested at time $t \in [0,T]$*

*This will be our control, and is subject to the obvious constrain that*
$$u(t) \in [0,1]$$

*Given such a control, the corresponding dynamics are provided by the
ODE*

$$\begin{aligned}
    &\Dot{x}(t) = ku(t)x(t) \\
    &x(0) = x_0\end{aligned}$$

*where the constant $k >0$ modeling the growth rate of our reinvestment
and $u(t)x(t)$ is the amount of reinvested output. Let us take as a
payoff functional*

$$J(u) = \int_0^T (1 - u(t))x(t)dt$$

*where $(1-u(t))x(t)$ is our consumption. The meaning is that we want to
maximize our total consumption of the output.*\
*The overall problem is:* $$\begin{aligned}
    &u^* := \argmax_{u:[0,T] \to [0,1]} J(u) = \int_0^T (1-u(t))x(t)dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = ku(t)x(t)\\
    &x(0)=x_0\end{aligned}$$

*Find an optimal control policy for this problem.*\

Exercise 4.13
-------------

*A young investor has earned in the stock market a large amount of money
S and plans to spend it so as to maximize his enjoyment through the rest
of his life without working. He estimates that he will live exactly T
more years and that his capital $x(t)$ should be reduced to zero at time
T, i.e., $x(T) = 0$. Also he models the evolution of his capital by the
differential equation*

$$\Dot{x}(t) = \alpha x(t) - u(t)$$

*where $x(0) = S$ is his initial capital, $\alpha > 0$ is a given
interest rate, and $u(t) \geq 0$ is his rate of expenditure. The total
enjoyment he will obtain is given by*
$$\int_0^T e^{-\beta t} \sqrt{u(t)}dt$$

*Here $\beta$ is some positive scalar, which serves to discount the
future enjoyment. Find the optimal control $u^* (t), t \in [0, T]$.*\

*Solve the problem* $$\begin{aligned}
    &u^* := \argmin_{u:[0,T] \to \mathbb{R}} J(u) = \int_0^T \sqrt{1 + u(t)^2}dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = u(t), \smallspace x(0)=x_0\end{aligned}$$ *where
$x_0 \in \mathbb{R}$ is an initial state, $T>0$ is a fixed final time.*\

Exercise 4.14
-------------

*Solve the problem* $$\begin{aligned}
    &u^* := \argmin_{u:[0,T] \to \mathbb{R}} J(u) = \int_0^T \sqrt{1 + u(t)^2}dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = u(t), \smallspace x(0)=x_0\end{aligned}$$ *where
$x_0 \in \mathbb{R}$ is an initial state, $T>0$ is a fixed final time.*\


Exercise 4.15
-------------

*Solve the problem* $$\begin{aligned}
    &u^* := \argmin_{u:[0,T] \to \mathbb{R}} J(u) = \int_0^T \sqrt{1 + u(t)^2}dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = u(t), \smallspace x(0)=x_0, \smallspace x(T) = x_1\end{aligned}$$
*where $x_0 \in \mathbb{R}$ is an initial state, $T>0$ is a fixed final
time.*\

# Lecture 5
Exercise 5.4
------------

*Prove the lemma: if $a + \varepsilon \geq b$ for arbitrary
$\varepsilon > 0$ with $a, b \in \mathbb{R}$, then $a \geq b$.*\

Exercise 5.5
------------

*Complete the proof of the principle of optimality by showing the
reverse inequality $V(t,x) \leq \Bar{V}(t,x)$.*\

Exercise 5.15 (Linear quadratic optimal tracking)
-------------------------------------------------

*For completeness, we consider a slightly more general form of the
linear quadratic regulator. The standard LQR derivation attempts to
drive the system to zero. Consider now the problem:*

$$\begin{aligned}
    &u^* := \argmin_{u:[0,T] \to \mathbb{R}^m} J(u) \\
    &\text{subject to}\\
    &\Dot{x}(t) = Ax(t) + Bu(t), \smallspace x(0)=x_0\end{aligned}$$
*where* $$\begin{split}
        J(u) := &(x(T) - x_d (T)) ^T Q_f (x(T) - x_d (T) )  \\ 
        + &\int_0^T \left( (x(t) - x_d(t)) ^T Q(x(t) - x_d(t)) + (u(t) - u_d(t)) ^T R(u(t) - u_d(t)) \right) dt
    \end{split}$$

*$Q_f = Q_f^T \geq 0$ (positive semidefinite), $Q = Q^T \geq 0$
(positive semidefinite), $R = R^T >0$ (positive definite).*\
*Find a formulation of an optimal policy and the corresponding HJB
equation (similar to the Riccati equation) using the sufficient
condition.*\
*Hint: consider a candidate of value functions of the following form*
$$\hat{V}(x,t) = x^T S_2(t) x + s_1^T(t) x + s_0(t), \smallspace S_2(t) = S_2(t) ^T >0, \smallspace s_1(t) \in \mathbb{R}^n, \smallspace s_0(t) \in \mathbb{R}.$$\

Exercise 5.16 (Nonlinear system)
--------------------------------

*Given the optimal control problem for a scalar nonlinear system:*

$$\begin{aligned}
    &u^* := \argmin_{u:[0,1] \to \mathbb{R}} J(u) := \int_0^1 [x(t)u(t)]^2 dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = x(t)u(t), \smallspace t \in [0,1] \\
    &x(0) =1\end{aligned}$$

*Obtain the optimal feedback solution by solving the associated HJB
equation.*\
*Hint: First show that the HJB partial differential equation admits a
solution that is quadratic in x.*\

Exercise 5.19 (Linear quadratic regulator (LQR) problem)
--------------------------------------------------------

*Consider a cart with an inverted pendulum hinged on top of it. For simplicity, the cart and the pendulum are
assumed to move in only one plane, and the friction, the mass of the
stick, and the gust of wind are disregarded. The problem is to maintain
the pendulum at the vertical position. For example, if the inverted
pendulum is falling in the direction shown, the cart moves to the right
and exerts a force, through the hinge, to push the pendulum back to the
vertical position.*\
*Let's consider the linearized inverted pendulum system (assuming
$\theta(t)$ and $\Dot{\theta}(t)$ are very small)*

$$\begin{bmatrix}
    \Dot{x}_1(t) \\ \Dot{x}_3(t) \\ \Dot{x}_3(t) \\  \Dot{x}_4(t) \\ 
\end{bmatrix}=
\begin{bmatrix}
    0 & 1 & 0 & 0 \\
    0 & 0 & -\frac{mg}{M} & 0 \\
    0 & 0 & 0 & 1 \\
    0 & 0 & \frac{(M+m)g}{Ml} & 0 
\end{bmatrix}
\begin{bmatrix}
    x_1(t) \\ x_2(t) \\ x_3(t) \\ x_4(t)
\end{bmatrix}
+
\begin{bmatrix}
    0 \\ \frac{1}{M} \\ 0 \\ - \frac{1}{Ml}
\end{bmatrix}
u(t)$$ *where
$x_1(t) = x(t), \smallspace x_2(t) = \Dot{x}(t), \smallspace x_3(t) = \theta(t), \smallspace and \smallspace x_4(t) = \Dot{\theta}(t)$.*\
*Consider the LQR problem*

$$\begin{aligned}
    &u^* := \argmin_{u:[0,\infty) \to \mathbb{R}^m} J(u) := \int_0^\infty \left( x(t)^T Qx(t) + u(t)^T R u(t) \right) dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = Ax(t) + Bu(t), \smallspace x(0) = x_0\end{aligned}$$

*where A and B are appropriate system matrices with m=1, M=2, l=3 and
g=9.8.*\
*Tasks:*

1.  *Appropriately choose the weighting $Q \geq 0$ and $R > 0$ to
    maintain the pendulum at the vertical position, i.e.,
    $\theta(t) = 0$ and $\Dot{\theta}(t) = 0$ as much as possible.*

2.  *Find an optimal policy for the LQR problem using Python or Matlab
    functions.*

3.  *Plot trajectories of the system x(t) and the control input u(t)
    over certain time interval to demonstrate the performance of your
    optimal control policy.*

4.  *In the answer, please include your Python or Matlab codes.*

5.  *Change the weight and see how the performance changes and discuss
    about the results.*


# Lecture 6

Exercise 6.15
-------------

*Consider the double integrator* $$\begin{aligned}
    &\Dot{x}_1(t) = x_2(t), \\
    &\Dot{x}_2(t) = u(t)\end{aligned}$$ *and the cost*
$$J(u) = \int_{t_0}^\infty \left( x_1(t)^2 + x_2(t)^2 + u(t) ^2 \right) dt$$
*Find P by solving the ARE. Verify (either analytically or numerically)
that it is indeed the steady-state solution of the RDE.*\



Exercise 6.24
-------------

*Consider the infinite-horizon LQR problem* $$\begin{aligned}
    &u^* := \argmin_{u:[0,\infty) \to \mathbb{R}} J(u) := \int_0^\infty \left( qx(t)^2 + ru(t)^2  \right) dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = ax(t) + bu(t), \smallspace t \in [t_0, \infty) \\
    &x(t_0) = x_0\end{aligned}$$

*where $a, q, r > 0$ and $b \in \mathbb{R}$ is arbitrary. Find the
optimal control law. Moreover, show that for $r \to 0$, the eigenvalue
of the optimal closed-loop system moves off to $- \infty$, while for
$r \to \infty$, the eigenvalue of the optimal closed-loop system tends
to $−a$*\


Exercise 6.25 (Boeing 747 Lateral Model)
-------------

*The complete lateral model of a Boeing 747 is* $$\begin{aligned}
    &\Dot{x}(t) = Ax(t) + Bu(t) \\
    &y(t) = Cx(t) + Du(t)\end{aligned}$$ *where* $$A = 
    \begin{bmatrix}
        -10 & 0 & 0 & 0 & 0 & 0 \\
        0.0729 & -0.0558 & -0.997 & 0.0802 & 0.0415 & 0 \\
        -4.75 & 0.598 & -0.115 & -0.0318 & 0 & 0 \\
        1.53 & -3.05 & 0.388 & -0.465 & 0 & 0 \\
        0 & 0 & 0.0805 & 1 & 0 & 0 \\
        0 & 0 & 1 & 0 & 0 & -0.3333 \\
    \end{bmatrix}
    , \smallspace B =
    \begin{bmatrix}
        1\\ 0\\ 0\\ 0\\ 0\\ 0\\
    \end{bmatrix}$$ *and* $$C =
    \begin{bmatrix}
        0 & 0 & 1 & 0 & 0 & -0.3333
    \end{bmatrix}
    , \smallspace D=0$$

*Minimize the sum of the energy of the output y and the energy of the
control u. The main effort is to minimize the energy of y which is
supposed to be zero in a steady state condition. So we put a weight
$q = 9.527 > 1$ on the energy of y. The problem now is as follows.*

$$\begin{aligned}
    &u^* := \argmin_{u:[0,\infty) \to \mathbb{R}} J(u) := \int_0^\infty [qy(t)^Ty(t) + u(t)^2] dt \\
    &\text{subject to}\\
    &\Dot{x}(t) = Ax(t) + Bu(t), \smallspace t \in [t_0, \infty) \\
    &y(t) = Cx(t) + Du(t), \smallspace t \in [t_0, \infty) \\
    &x(t_0) = x_0\end{aligned}$$ *Tasks:*

1.  *Find an optimal policy for the LQR problem by solving ARE using
    Python or Matlab functions.*

2.  *Plot trajectories of $y(t)$ and $u(t)$.*

3.  *In the answer, please include your Python or Matlab codes.*

