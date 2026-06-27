# The Lane Emden Chandrasekhar Equation
The Lane Emden Chandrasekhar Equation was found in 1869 by astrophysicists Jonathan Homer Lane [1] and Robert Emden [2]. The theory of polytropic stellar structure was subsequently placed on a rigorous theoretical foundation by Subrahmanyan Chandrasekhar [3] in his 1939 monograph _An Introduction to the Study of Stellar Structure_. It has enormous applications in field of astrophysics. It is essentially a mixture of various equations combined to give a single equation whose solutions help us derive all important parameters involved to understand the dynamics of a star. To understand this needs elementary knowledge and bit of numerical solving of differential equations. I use Mathematica to solve this equation. My aim is to understand this equation. 

For a non-physics student, reading this README page will help in following manner-
1. How do we create a model by cumulating many "very basic ideas" in physics. We must start from something right?
2. Develop a kind of smartness which is to combine many equations into one simple equation. 
3. Techniques to solving non-linear differential equations numerically.  
4. This concept is considered basic in all astrophysics courses.

We will derive the Lane Emden Equation, and in that manner get to know the assumptions. We will then explore the solutions for general $n$. <!-- We deal more with the overall picture rather than the plots involved in this, so it is better to ignore the tiny details in each graph unless specified. This kind of idea is ubiquitous to all fields.--> Once equipped with all the information we need, We will use the model to reproduce all the parameter values for our sun sitting at the center of our solar system.

<!--  This equation can be a salad of symbols. So take your sweet time with it. -->

<!--Whatever is stated in this webpage is checked multiple times and 100% legit information. Even then, there are possibilities of mistake is being made, so please mention on my [email](mailto:omshah0405@gmail.com) so that I can rectify them.-->
Possible corrections can be mailed to me at my [email](mailto:omshah0405@gmail.com).

Let us begin understanding the Lane Emden Chandrasekhar Equation. 
The gravitational Gauss law states that $\textit{The gravitational flux through any closed surface is proportional to the enclosed mass.}$
Differential form is $\vec{\nabla}\cdot \vec{g} = - 4 \pi G \rho$.
Integral form is $\iint \vec{g}\cdot \vec{\mathrm{d}A} =-4 \pi G M_{enc}$.

<details>
<summary><strong>Assumptions</strong></summary>

Suppose in an empty space I add a source. A source is a aggregate body of mass localised in a finite volume. Newton tells us the source will create a gravitational potential field around the source $\displaystyle \propto -\frac{1}{r}$. This is considered a **_conservative field_**, that itself creates a force field around the source given by $\vec{F}=-\nabla V$. The force field is also given by $\vec{F}=m\vec{g}=\vec{g}$, (assume m=1).

Substitute in gauss law, $\vec{g}=-\nabla V$ becomes $\vec{\nabla} \cdot -\nabla V = - 4 \pi G \rho$, or $\nabla^{2} V = 4 \pi G \rho$ which is the poisson's equation of gravitational gauss law.

The Laplacian of f(x,y) is divergence of a gradient of f(x,y). The gradient points in the direction of greatest increase. The divergence of any curve shows how the fluid will flow in that small region. The laplacian is related to the local curvature of a scalar field. That means the laplacian will display convergence (laplacian is -ve valued) at maxima and (laplacian is +ve valued) divergence at minima. At maxima, the second derivative is negative and at minima, is positive. <!--Thus laplacian of any curve can be understood by behavior of its second derivative. -->

Now, suppose the shape of the massive object in 3 dimensional space is **_spherically symmetric_**. The polar angle and azimuthal angle components are a constant. 

</details>

<details>
<summary><strong>Derivation</strong></summary>

We primarily consider the density profile of the object given by 
$\rho = \rho (r)$.
The density profile is strictly related to radial distance. The mass profile of the object is given by
① $\mathrm{d}M= \int \rho \mathrm{d}V$. 
We can state that potential field $V=V(r)$ created due to presence of mass is also strictly related to radial distance because of gravitational field $\vec{g} = \vec{g} (r)$. 

So the Laplacian of V can be rewritten as, 
② $\nabla^{2} V = \frac{1}{r^2}\frac{\partial}{\partial r}\big( r^2 \frac{\partial V}{\partial r}\big)  = 4 \pi G \rho(r)$.

<!-- ⑦ ⑧ ⑨ ⑩ -->

Let suppose body is a **_star_** and it is in **_hydrostatic equilibrium_**, this means that the star at each point is in _inertial equilibrium_ (_assumes perfect balance_) between the two forces, 
1. star expansion due to nuclear reaction
2. contraction due to increase in gravitational field as nuclear reactions happen, mass is increased in endproduct resulting in increased gravitational field.

The equation is given by $F = \frac{\mathrm{d}P}{\mathrm{d}r}\mathrm{d}r\mathrm{d}A = -\frac{G M(r) \rho (r)}{r^2}\mathrm{d}r\mathrm{d}A$.
On simplification, this equation becomes, 
③ $\frac{\mathrm{d}P}{\mathrm{d}r} = -\frac{G M(r) \rho (r)}{r^2}$.

$\vec{F}=-\nabla V$ and $F=\frac{G M(r)}{r^{2}}$ allows us to rewrite the hydrostatic equilibrium equation as 
$\frac{\partial V}{\partial r} = - \frac{1}{\rho} \frac{\partial P}{\partial r}$.

Therefore, one can write the Laplacian of $V$ (Eq.②) as simple combination of mass profile equation and hydrostatic equilibrium.  

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

**_Introduce the dimensionless variable_** $\xi$ such that

⑥ $r = a \xi$

where
$a^2 =\frac{(n+1)K\rho_c^{\frac{1}{n}-1}}{4\pi G}$. Note that $[a]=[L]$ so $a$ is a length dimension constant. We work in terms of the dimensionless radial coordinate $\xi$ defined by $\xi=\frac{r}{a}$ which represents the scaled version of the physical radius $r$. The logic of doing this lies in extreme simplication of the equation.

After substitution and simplification we obtain the our equation,
| Lane Emden Equation |
|---------------------|
| $$\frac{1}{\xi^2}\frac{d}{d\xi}\left(\xi^2\frac{d\theta}{d\xi}\right)+\theta^n=0$$ |
</details>
 
<details>
<summary><strong>Numerical Method</strong></summary>

Below is the Mathematica code for solving the Lane Emden Equation;
```Mathematica
Clear[LaneEmdenSolve]

LaneEmdenSolve[n_, \[Xi]max_ : 10, rhoC_ : 1, K_ : 1, G_ : 1, C_ : 1] :=
 Module[
  {eps = 10^-10,
   sol,
   a,
   theta, deltheta,
   r, rmax,
   rho, delrho,
   P, delP,
   m,
   g,
   rat, arat,
   B,
   T, delT,
   \[Sigma], \[CapitalPhi], L,
   kb, ma, mu
   },
  
  sol =
   NDSolve[{
      \[Theta]''[\[Xi]] + (2/\[Xi]) \[Theta]'[\[Xi]] + \
\[Theta][\[Xi]]^n == 0,
      \[Theta][eps] == 1 - eps^2/6,
      \[Theta]'[eps] == -eps/3
      }, \[Theta], {\[Xi], eps, \[Xi]max}, MaxStepSize -> 0.05][[1]];
  
  a = If[
    n == 0, Sqrt[K /(4 Pi G rhoC)](*constant-density sphere*),
    Sqrt[(K (n + 1) rhoC^(1/n - 1))/(4 Pi G)]
    ];
  
  theta[\[Xi]_] := Evaluate[\[Theta][\[Xi]] /. sol];
  deltheta[\[Xi]_] := theta'[\[Xi]];
  r[\[Xi]_] := a \[Xi];
  rmax = a \[Xi]max;

  (* xi = r/a *)
  rho[r_] := rhoC theta[r/a]^n;
  delrho[r_] := (rhoC n/a) theta[r/a]^(n - 1) deltheta[r/a];
  
  (*mass equation*)
  m =
   NDSolveValue[{
     M'[r] == 4 Pi a^3 (r/a)^2 rho[r],
     M[0] == 0
     }, M, {r, 0, rmax}];
  
  (*Hydrostatic equilibrium*)
  P[r_] := If[
    n == 0, K*rho[r],
    K*rho[r]^(1 + 1/n)
    ];
  delP[r_] := P'[r];
  
  (*g(r)*)
  g[r_] := (G m[r])/r^2 ;
  
  (* ratio functions *)
  rat[r_] := Abs[delP[r]]/(rho[r] g[r] );
  B[r_] := Abs[delP[r]]/(rho[r] g[r] ) + 1;
  
  (*T curve and Eddington Emden Chandrasekhar Equation *)
  kb = 1;
  ma = 1;
  mu = 1;
  T[r_] := (kb ma)/mu  P[r] /rho[r];
  delT[r_] := T'[r];

  \[Sigma] = 1; (*stefan bolzmann constant \[Sigma] *)

  (*Flux*)
  \[CapitalPhi][r_] := -((delT[r] 4 \[Sigma] (T[r])^3)/(C rho[r]));   (*some constant C *)

  (*Luminosity*)
  L[r_] := \[CapitalPhi][r]/(4 Pi r^2);
  
  <|
   "n" -> n, "Solution" -> sol, "Theta" -> theta, "a" -> a,
   "r" -> r, "rmax" -> rmax,
   "Rho" -> rho, "Mass" -> m,
   "P" -> P, "dP" -> delP,
   "g" -> g,
   "r1" -> rat,
   "B" -> B,
   "T" -> T,
   "F" -> \[CapitalPhi],(*Flux*)
   "L" -> L
   |>]
   ```

We solve the equations in radial coordinate $r$ because everything is representable in $r$ not in $\xi$.

Numerical solving involves using NDSolve where you first write your equation and boundary conditions. The boundary conditions are derived from solutions of n = 0. Analytical boundary conditions are $\theta(0)=1$ and $\theta'(0)=0$. Instead of evaluating at $\xi=0, we evaluate at $eps=10^{-10}$. This approximation is done to avoid issues like ComplexInfinity solutions.  Thus numerical boundary conditions are slightly modified version of analytical boundary conditions.

To avoid ComplexInfinity, I have modified $a$ and $P$ also. 

</details>

<details>
<summary><strong>Results</strong></summary>

For $n$ integer values ranging from 0 to 6, the solutions are displayed below;

The values of $a$ for increasing $n$ integer values from 0 to 6; As the polytropic index ($n$) increases, the scaling length changes because the relationship between pressure and density changes. This changes the physical size represented by one unit of the dimensionless coordinate.
![Diagram](./figures/a.png)

The values of $r_max$ for increasing $n$ integer values from 0 to 6; The quantity $r_max =a ξ_max$ represents the physical radius of the numerical solution. Since it depends directly on the scaling length $a$, its value changes with the polytropic index. This illustrates how the characteristic size of the stellar model varies for different polytropic equations of state.
![Diagram](./figures/rmax.png)

The values of $\theta(\xi)$; The function  $\theta(\xi)$ describes the normalized density distribution inside the star. Larger values of $n$ produce solutions that decrease more gradually near the center, indicating greater central concentration of matter.
![Diagram](./figures/theta.png)

The values of $r(\xi)$; The dimensionless coordinate is converted back to the physical radius using $r=aξ$. This transformation allows all physical quantities such as density, pressure, and mass to be expressed in SI units
![Diagram](./figures/r.png)

Now we shift to r-axis for understanding the further plots;
Note that you cannot achieve $M(\xi)$, so you have to shift back to physical radial coordinate. 

Density profile; The density profile is obtained from $\rho(r)=\rho_c\theta(r)^n.$ Density reaches its maximum at the stellar center and decreases monotonically toward the surface. Increasing the polytropic index results in a stronger concentration of mass near the core.
![Diagram](./figures/rho.png)

Mass profile; The enclosed mass is calculated from $ \frac{dM}{dr}=4\pi r^2\rho(r).$ The enclosed mass increases continuously with radius because each spherical shell contributes additional matter. The slope gradually decreases near the stellar surface as the density approaches zero.
![Diagram](./figures/mass.png)

Pressure profile; The pressure follows the polytropic equation of state, $ P=K\rho^{1+\frac{1}{n}}. $ Pressure is largest at the center and decreases outward. It supplies the outward force necessary to balance gravitational collapse.
![Diagram](./figures/pressure.png)

Pressure derivative $\frac{\partial P}{\partial r} (r)$; The pressure gradient is always negative because pressure decreases with increasing radius. According to hydrostatic equilibrium, $\frac{dP}{dr}=-\rho(r)g(r),$ the pressure gradient exactly balances the inward gravitational force.
![Diagram](./figures/pressurederivative.png)

Absolute Value of Pressure derivative $|\frac{\partial P}{\partial r} (r)|$; The magnitude of the pressure gradient is $\left|\frac{dP}{dr}\right|.$ It measures the strength of the supporting pressure force without regard to direction. It is largest near the stellar center where both pressure and density are highest and gradually decreases outward.
![Diagram](./figures/absolutepressurederivative.png)

Gravitational field $g(r)$; The gravitational acceleration is computed from $ g(r)=\frac{GM(r)}{r^2}.$ It is zero at the center because the enclosed mass vanishes there. The field increases with radius as enclosed mass accumulates, reaches a maximum, and may decrease toward the surface because of the inverse-square dependence.
![Diagram](./figures/gravitationalfield.png)

Product $\rho(r) g(r)$;
![Diagram](./figures/productrhogravitationalfield.png)
The quantity

$$
\frac{\dfrac{dP}{dr}}{\rho(r)g(r)}
$$

compares the pressure gradient with the gravitational force per unit volume.

Hydrostatic equilibrium predicts

$$
\frac{dP}{dr}=-\rho(r)g(r),
$$

so this ratio should remain close to

$$
-1.
$$

Any deviation from this value is primarily due to numerical discretization errors and provides a measure of the numerical accuracy.

Quantity $\frac{\frac{\partial P}{\partial r}}{\rho(r) g(r)}$;
![Diagram](./figures/ratio.png)

We _assumed_ hydrostatic equilibrium, which is essentially a competition between the forces due to pressure expansion and gravitational contraction. 
To compare these forces, we take their ratios and study that (just like we define reynold's number for comparing inertial and viscous forces for understanding turbulence in flow). 
We define $\beta(r) = \left|\frac{\frac{\partial P}{\partial r}}{\rho(r) g(r)}\right| + 1$. The $+ 1$ is considered for a specific reason, $\beta(r) = \rho(r) A(r)$ where $A$ is non-inertial acceleration of the frame. Thus, $\beta$ corresponds to the deviation parameter from the hydrostatic equilibrium where small $\beta$ means less deviation. 

The parameter

$$
\beta(r)=\left|\frac{\dfrac{dP}{dr}}{\rho(r)g(r)}\right|+1
$$

is introduced as a measure of the deviation from hydrostatic equilibrium. When the pressure gradient exactly balances gravity,

$$
\beta(r)=2.
$$

If your intended equilibrium value is instead 1, define it as

$$
\beta(r)=\left|\frac{\dfrac{dP}{dr}}{\rho(r)g(r)}+1\right|,
$$

which satisfies

$$
\beta(r)=0
$$

for perfect hydrostatic equilibrium. (This latter definition is generally a more natural error measure.)

$\beta$ parameter;
![Diagram](./figures/beta.png)

The temperature profile can be obtained from a simple ideal gas equation $P\mu = \rho k_{b} T$. 
Temperature profile; Temperature is highest at the stellar center where both pressure and density attain their maximum values and decreases smoothly toward the stellar surface.
![Diagram](./figures/T.png)

</details>

<details>
<summary><strong>Extension of the Lane–Emden Model: Radiative Flux and Luminosity</strong></summary>

Now we connect the Lane Emden Equation further to the new Eddington Emden Chandrasekhar Equation which states that, 

For a spherically symmetric massive body, the gravitational flux $\Phi(r)$ passing through a shell (ring shaped) of thickness $\mathrm{d} r$ located at radial distance $r$ from the center of body (origin is at the center of body) is given by 

Note : This formula was found by human experience and logic, just how coulomb's law is defined. Therefore 

$\Phi( r + \mathrm{d}r ) - \Phi(r) \propto \rho(r)$

$\Phi( r + \mathrm{d}r ) - \Phi(r) \propto \Phi_{0}(r)$

$\Phi( r + \mathrm{d}r ) - \Phi(r) \propto \mathrm{d} r$

$\Phi( r + \mathrm{d}r ) - \Phi(r) = - C \rho(r) \Phi_{0}(r) \mathrm{d} r$ where $C$ is a constant of proportionality and $\Phi_{0}(r)$ is the incident flux at radial distance $r$. 

By stefan boltzmann law $\Phi(r) = \sigma T(r)^4$ where $\sigma$ is a stefan boltzmann constant and $T(r)$ is temperature profile of the body. 

$\Phi( r + \mathrm{d}r ) - \Phi(r) = 4 \sigma T^3 \mathrm{d} T$

Therefore, 
$\frac{\mathrm{d} T}{\mathrm{d} r} = -\frac{C \rho(r) \Phi_{0}(r)}{4 \sigma T^3}$ we can further substitute $\Phi(r) = \frac{L(r)}{4 \pi r^2}$ to obtain the luminosity relation. 

Flux profile; The radiative flux is estimated from the temperature gradient using the proposed extension of the Lane–Emden model. Regions possessing larger temperature gradients transport energy more efficiently, resulting in larger radiative flux.
![Diagram](./figures/flux.png)

Luminosity profile; The luminosity represents the total energy transported through a spherical surface of radius (r). It is computed from the radiative flux and illustrates how energy transport varies throughout the stellar interior. In a realistic stellar model, luminosity generally increases outward as progressively larger amounts of energy generated within the interior pass through spherical shells of increasing radius.
![Diagram](./figures/L.png)

The essence of combining these equations is that **_for star containing ideal gas, which has spherical symmetry, we can now find for any thermodynamic process (polytropic index $n$), we can find the quantities_** $\rho(r), M(r), P(r), g(r), β, T(r), L(r)$ **_provided the central density_** $\rho_{c}$  **_,the polytropic constant_** $K$ **_,the flux constant_** $C$ **_, and the mean molecular weight_** $\mu$.
Knowing this, now its just fitting the observed information of stars to this equation's results in different $r$ regions. If we are lucky, there could be some star which is completely expressed by a single lane emden equation. <!--(particular $n, \rho_{c}, K, C, \mu$ value). -->
</details>

<details>
<summary><strong>Solar Model</strong></summary>

This mini project develops a **single polytropic model of the Sun** based on the work of Archibald W. Henry [4] in his paper, _A Polytropic Model of the Sun_.

Using the initial parameters and methodology proposed in the paper, we construct a numerical model that reproduces the fundamental physical properties and internal structure of the Sun. The model yields a solar mass of 2.01 × 10³⁰ kg, a central temperature of 1.45 × 10⁷ K, and a dimensionless parameter β of the order of 10⁻⁸. These results are in good agreement with the expected solar parameters, demonstrating the effectiveness of the single-polytrope approximation.
This results [ssm.pdf](./reports/ssm.pdf) and the corresponding codebase [ssm.nb](./notebooks/ssm.nb) is here.
</details>

<details>
<summary><strong>Summary</strong></summary>

To conclude, I hope you found this project informative and inspiring. Throughout this work, we explored the application of electrostatics, vector calculus, hydrostatic equilibrium, the mass profile equation, and the ideal-gas polytropic equation to develop a simple yet effective model of the Sun.

By introducing suitable dimensionless variables, we simplified the governing equations into a single differential equation. We then implemented the model in Mathematica, fitted the appropriate parameters, and successfully reproduced key solar properties, including the solar mass and central temperature.
I am leaving this project here in the hope that it may be useful to others. If you build upon this work, improve the model, or extend it further, I would be delighted to hear about your results and learn from your contributions.

</details>

 
<details>
<summary><strong>References</strong></summary>

1. Lane, J. H. (1870). *On the Theoretical Temperature of the Sun under the Hypothesis of a Gaseous Mass Maintaining Its Volume by Its Internal Heat*. American Journal of Science and Arts, 50, 57–74.

2. Emden, R. (1907). *Gaskugeln*. Leipzig: B. G. Teubner.

3. Chandrasekhar, S. (1939). *An Introduction to the Study of Stellar Structure*. University of Chicago Press.

4. Henry, A. W. *A Polytropic Model of the Sun*. The Astrophysical Journal.

</details>
