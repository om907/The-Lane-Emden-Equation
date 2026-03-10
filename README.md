# The Lane Emden Chandrasekhar Equation
The Lane Emden Chandrasekhar Equation was found in 1869 by astrophysicists Jonathan Homer Lane and Robert Emden. It is of enormous applications in field of astrophysics. It is essentially a mixture of various equations combined to give a single equation whose solutions help us derive all important parameters involved to understand the dynamics of a star. To understand this needs elementary knowledge and bit of numerical solving of differential equations. I use Mathematica to solve this equation. My aim is to understand this equation. 

We will derive the Lane Emden Equation, and in that manner get to know the assumptions as well as between the lines implications. We will together explore the solutions for n = 1 ( well known solution ) , then for general n. We will also compare the solution and parameters for various n. 
Once equipped with all the knowledge we need, we will together rediscover all the parameter values for our sun sitting at the center of our solar system, which will be shocking to us while first reading but completely understandable and valid so. 

Along the way we will ask ourselves and answer multiple what if questions, so it should be engaging to the reader if you ask yourself what could be the answer to the thought question prior to watching the answer yourself.
<!--  This equation can be a salad of symbols. So take your sweet time with it. -->

Whatever is stated in this webpage is checked multiple times and 100% legit information. Even then, there are possibilities of mistake is being made, so please mention on my [email](mailto:omshah0405@gmail.com) so that I can rectify them.

Let us begin understanding the Lane Emden Chandrasekhar Equation.

The gravitational Gauss law states that $\textit{The gravitational flux through any closed surface is proportional to the enclosed mass.}$
Differential form is $\vec{\nabla}\cdot \vec{g} = - 4 \pi G \rho$.
Integral form is $\iint \vec{g}\cdot \vec{\mathrm{d}A} =-4 \pi G M_{enc}$.

Suppose in an empty space I add a source. A source is a aggregate body of mass localised in a finite volume. Newton tells us the source will create a gravitational potential field around the source $\displaystyle \propto -\frac{1}{r}$. This is considered a **_conservative field_**, that itself creates a force field around the source given by $\vec{F}=-\nabla V$. The force field is also given by $\vec{F}=m\vec{g}=\vec{g}$, (assume m=1).

<!-- If we are allowed write some vector as a gradient of a scalar then $\vec{\nabla} × \vec{g}=0$. -->

Substitute in gauss law, $\vec{g}=-\nabla V$ becomes $\vec{\nabla} \cdot -\nabla V = - 4 \pi G \rho$, or $\nabla^{2} V = 4 \pi G \rho$ which is the poisson's equation of gravitational gauss law.

The laplacian of f(x,y) is divergence of a gradient of f(x,y). The gradient of f(x,y) indicates the steepest path to reach uphill in the curve. The divergence of any curve shows how the fluid will flow in that small region. The laplacian shows curvature. That means the laplacian will display convergence (laplacian is -ve valued) at maxima and (laplacian is +ve valued) divergence at minima. At maxima, the second derivative is negative and at minima, is positive. Thus laplacian of any curve can be understood by behavior of its second derivative. 

Now, suppose the shape of the massive object in 3 dimensional space is **_spherically symmetric_**. The polar angle and azimuthal angle components are a constant. We primarily consider the density profile of the object given by 
$\rho = \rho (r)$.
The density profile is strictly related to radial distance. The mass profile of the object is given by
① $\mathrm{d}M= \int \rho \mathrm{d}V$. 
Intuitively, we can state that potential field $V=V(r)$ created due to presence of mass is also strictly related to radial distance. This is because of gravitational field $\vec{g} = \vec{g} (r)$. 

So the laplacian of V can be rewritten as, 
② $\nabla^{2} V = \frac{1}{r^2}\frac{\partial}{\partial r}\big( r^2 \frac{\partial V}{\partial r}\big)  = 4 \pi G \rho(r)$

<!--    ⑥ ⑦ ⑧ ⑨ ⑩ -->

Let suppose body is a **_star_** and it is in **_hydrostatic equilibrium_**, this means that the star at each point is in _inertial equilibrium_ (_assumes perfect balance_) between the two forces: 1. star expansion due to nuclear reaction, 2. contraction due to increase in gravitational field as nuclear reactions happen, mass is increased in endproduct resulting in increased gravitational field. The equation is given by $F = \frac{\mathrm{d}P}{\mathrm{d}r}\mathrm{d}r\mathrm{d}A = -\frac{G M(r) \rho (r)}{r^2}\mathrm{d}r\mathrm{d}A$.

On simplification, this equation becomes, 
③ $\frac{\mathrm{d}P}{\mathrm{d}r} = -\frac{G M(r) \rho (r)}{r^2}$.

$\vec{F}=-\nabla V$ and $F=\frac{G M(r)}{r^{2}}$ allows us to rewrite the hydrostatic equilibrium equation as 
$\frac{\partial V}{\partial r} = - \frac{1}{\rho} \frac{\partial P}{\partial r}$.

Therefore, one can write the laplacian of $V$ (Eq.②) as simple combination of mass profile equation and hydrostatic equilibrium.  

Now we use the **_ideal gas polytropic equation_** which states that for any polytropic index $n$, the ideal gas equation is 
$P V^{1+\frac{1}{n}}=\text{constant}$.
$V = \frac{M}{\rho}$ implies that 
④ $P =K \rho^{1+\frac{1}{n}}$ where $K$ is a dimensional constant. 
This equation can be understood by understanding $n$, that is when $n=0$ process is isothermal, $n=\frac{1}{\gamma-1}$ process is adiabatic. 

Here we introduce a **_parametrization of density profile_** of the form 
⑤ $\rho(r) = \rho_{c} \theta(r)^{n}$ where $\rho_{c}$ is the central density, $n$ is the polytropic index of ideal gas equation and $\theta(r)$ is a dimensionless variable, which we are interested in. Density at any point can be related to the central density by this new function. The essence of this equation lies in $n$, which connects the density profile to polytropic ideal gas equation. 

Introducing ④ and ⑤ to the laplacian of $V$ we do the following steps to achieve the Lane Emden equation. 

$\frac{1}{r^2}\frac{\partial}{\partial r}\big( \frac{r^2}{\rho} \frac{\partial P}{\partial r}\big)  = -4 \pi G \rho(r)$

$P = K\rho_c^{1+\frac{1}{n}}\theta^{n+1}$

First compute the pressure derivative

$\frac{\partial P}{\partial r} = K\rho_c^{1+\frac{1}{n}}(n+1)\theta^n \frac{\partial\theta}{\partial r}$

Now divide by $\rho$

$\frac{1}{\rho}\frac{\partial P}{\partial r}=\frac{K\rho_c^{1+\frac{1}{n}}(n+1)\theta^n}{\rho_c\theta^n}\frac{\partial\theta}{\partial r}=K(n+1)\rho_c^{\frac{1}{n}}\frac{\partial\theta}{\partial r}$

Substitute into the main equation

$\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2 K(n+1)\rho_c^{\frac{1}{n}}\frac{\partial\theta}{\partial r}\right)=-4\pi G\rho_c\theta^n$

Since the constant factors can be taken outside,

$K(n+1)\rho_c^{\frac{1}{n}}\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial\theta}{\partial r}\right)=-4\pi G\rho_c\theta^n$

Divide by $K(n+1)\rho_c^{1/n}$

$\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial\theta}{\partial r}\right)=-\frac{4\pi G\rho_c}{K(n+1)\rho_c^{1/n}}\theta^n$

Introduce the dimensionless variable $\xi$ such that

$r = a \xi$

where
$a^2 =\frac{(n+1)K\rho_c^{\frac{1}{n}-1}}{4\pi G}$. Note that $[a]=[L]$. So $a$ is a length dimension constant. Now onwards we operate in the in a scaled axis $\xi$ which is equivalent to $\frac{r}{a}$. 

After substitution and simplification we obtain the $\textbf{Lane Emden equation}$

$\frac{1}{\xi^2}\frac{d}{d\xi}\left(\xi^2\frac{d\theta}{d\xi}\right)+\theta^n=0$

