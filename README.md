# The Lane Emden Chandrasekhar Equation
The Lane Emden Chandrasekhar Equation was found in 1869 by astrophysicists Jonathan Homer Lane and Robert Emden. It is of enormous applications in field of astrophysics. It is essentially a mixture of various equations combined to give a single equation whose solutions help us derive all important parameters involved to understand the dynamics of a star. To understand this needs elementary knowledge and bit of numerical solving of differential equations. I use Mathematica to solve this equation. My aim is to understand this equation. 

We will derive the Lane Emden Equation, and in that manner get to know the assumptions as well as between the lines implications. We will together explore the solutions for n = 1 ( well known solution ) , then for general n. We will also compare the solution and parameters for various n. 
Once equipped with all the knowledge we need, we will together rediscover all the parameter values for our sun sitting at the center of our solar system, which will be shocking to us while first reading but completely understandable and valid so. 

Along the way we will ask ourselves and answer multiple what if questions, so it should be engaging to the reader if you ask yourself what could be the answer to the thought question prior to watching the answer yourself. This equation can be a salad of symbols. Your brain doesn’t have to be. So take your sweet time with it.

Whatever is stated in this webpage is checked multiple times and 100% legit information. Even then, there are possibilities of mistake is being made, so please mention them, so that I can rectify them.
I am myself learning, and always hungry for knowing more, so feel free to ask me questions on my [gmail](omshah0405@gmail.com). If I know, I will surely respond, and if I don't nevertheless will learn something new!

Let us begin understanding the Lane Emden Chandrasekhar Equation.

The gravitational Gauss law states that $\textit{The gravitational flux through any closed surface is proportional to the enclosed mass.}$
Differential form is $\vec{\nabla}\cdot \vec{g} = - 4 \pi G \rho$.
Integral form is $\iint \vec{g}\cdot \vec{\mathrm{d}A} =-4 \pi G M_{enc}$.

Suppose in an empty space I add a source. A source is a aggregate body of mass localised in a finite volume. Newton tells us the source will create a gravitational potential field around the source $\displaystyle \propto -\frac{1}{r}$. This is _considered_ a conservative field, that itself creates a force field around the source given by $\vec{F}=-\nabla V$. The force field is also given by $\vec{F}=m\vec{g}=\vec{g}$, (assume m=1).

<!-- If we are allowed write some vector as a gradient of a scalar then $\vec{\nabla} × \vec{g}=0$. -->

Substitute in gauss law, $\vec{g}=-\nabla V$ becomes $\vec{\nabla} \cdot -\nabla V = - 4 \pi G \rho$, or $\nabla^{2} V = 4 \pi G \rho$ which is the poisson's equation of gravitational gauss law.

The laplacian of f(x,y) is divergence of a gradient of f(x,y). The gradient of f(x,y) indicates the steepest path to reach uphill in the curve. The divergence of any curve shows how the fluid will flow in that small region. The laplacian shows curvature. That means the laplacian will display convergence (laplacian is -ve valued) at maxima and (laplacian is +ve valued) divergence at minima. At maxima, the second derivative is negative and at minima, is positive. Thus laplacian of any curve can be understood by behavior of its second derivative. 

Now, suppose the shape of the massive object in 3 dimensional space is **_spherically symmetric_**. The polar angle and azimuthal angle components are a constant. We primarily consider the density profile of the object given by 
$\rho = \rho (r)$.
The density profile is strictly related to radial distance. The mass profile of the object is given by
$ \mathrm{d}M= \int \rho \mathrm{d}V$. 
Intuitively, we can state that potential field $V=V(r)$ created due to presence of mass is also strictly related to radial distance. This is because 









