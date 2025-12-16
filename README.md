# Simplify complex sytems of physics furmulas and chemical reactions.
1. In chemistry
The __steady-state pproximation__ is widely used in chemical kinetics to calculations and help determine the overal reactions rate without considering the detailed time-dependent changes in intermediates concentrations.

2. In Physics
The __steady-state approximation__ is used in physics problems, such as semiconductors and Quantum optics, used in rate equations for excited states.

__The Pyhton Function Basics:__
- `def`: defines a function
- `return`: sends a result back from the function
- `for` loop: repeats code for each item in a list
- `fig`: the whole figure
- `ax`: the plotting area
- `ax.set_x or y ticks(ticks)`: sets the position of ticks on the x-axis or y-axis)
- `assert`: used for debugging
- `except`: used in try/except blocks for error handling.

Reference:
- [Cornell Chemical Engineering Lecture 7](https://duncan.cbe.cornell.edu/cheme2200/KINETICSLECTURES/ChemE_2200_lecture_K7.pdf)

# P7.1 - Particle Accelerator
An electric filed of strength _E_ will apply a force $F=qE$ onto a particle with electric charge _q_. In one dimension, with an initial velocity $v_{0}$, the particle's velocity and position will be given as 

$x(t)=v_{0}t + 0.5 \frac{qE}{m} t^{2}$, and

$v(t)=v_{0} + \frac{qE}{m}t$

a) Consider an electron, which has a mass $m\approx 9.1 \times 10^{-31}$ kg and electric charge $q\approx -1.6 \times 10^{-19}$ C, caught in an electric field of strength $E = 0.02 N/C$.
Make a program that asks the user for values for $v_{0}$ and $t$, and prints the position and velocity pf the electron.
Test your program by checking the electrons position and velocity at _t = 15 s_ with $v_{0} = 220$ m/s.

b) Rewrite your program to take $v_{0}$ and _t_, as well as _q_ and _m_ from the command line. Use a try/except block to initialize the variables, in case the user provides too few, or they cannot be converted to floats. In that case, ask the user for the parameters as input, like in excercise b).

Protons have mass $m\approx 1.67 \times 10^{-27}$ kg and electric charge $q\approx 1.6 \times 10^{-19}$ C. Neutrons have virtually the same mass as protons, and no electric charge.
check the position and velocity of these two particles with the same parameters as in exercise.

![Particle Accelerator](https://github.com/dindagustiayu/The-Steady-State-Approximation-for-Solve-Physics-Problems-/blob/main/SSA%20svg/Particle%20Accelerator.svg)


# P7.2 -Capacitor discharge
__Physical introduction__: A caoacitor is simply two metals plates set up parallel to each other. We can charge up each plate with positive and negative electic charges by connection them to a battery. If we remove the battery and connect the two plates together, the charges will flow from the negative plate to the positive plate, and the capacitor will discahrge. To avoid the electrical current becoming infinite, we connect a resistor between the plates. We now have an RC-circuit.
The cahrge _Q_ of a capacitor that discharge in a RC-circuit, is given as.

$Q(t) = CVe^{-t/RC}$

The following program calculates this discharge for _n_ = 1000 time-steps over an interval _t_ = 10 s. The capacitor has a capacitance of _C_ = 0.007 F, an initial coltage $V_{0}$= 50 V, and the resistor has a resistance $R=35 \Omega$. 

a) RC-circuit discharge program and vectorize with Python list and loo[.

b) RC-circuit discharge program  and vectorize it with NumPy

![a) RC Circuit discharge with Python list and loop](https://github.com/dindagustiayu/The-Steady-State-Approximation-for-Solve-Physics-Problems-/blob/main/SSA%20svg/Capacitor%20Discharge%20(loop).svg).
![b) RC Circuit discharge with NumPy](https://github.com/dindagustiayu/The-Steady-State-Approximation-for-Solve-Physics-Problems-/blob/main/SSA%20svg/Capacitor%20Discharger%20(NumPy).svg).

# P7.3 - Kinetic Friction Wooden Block
In this exercise, you are supposed to create a program which finds out hoe far a wooden block with initial velocity $v_{0}$ m/s will slide across surfaces of different materials. The material of the surfaces will affect the frictional force acting on the wooden block.

The position of the block can be expressed as such:

$x(t)=v_{0}t - \frac{1}{2}\mu gt^{2}$

where $\mu$ is a coefficient of friction and g = 9.81 $m/s^{2}$.

One can find  by some calculations at which time _T_ the block will stop moving. The time _T_ is found to be

$T=\frac{v_{0}}{\mu g}$

Define a function which takes a list of different coefficients of friction as parameter, calculates the position at time _T_, that is $x(T)$, and then stories the results in a list. The list of the calculated positions must then be returned by the function. Distance before stopping.

$x(T)=\frac{v_{0}^{2}}{2 \mu g}$

Let $v_{0}=5$ m/s and the list of coefficient of friction be [0.62, 0.3, 0.45, 0.2]. Call the function and write out every position along with corresponding coefficient of friction.

![Kinetic Friction](https://github.com/dindagustiayu/The-Steady-State-Approximation-for-Solve-Physics-Problems-/blob/main/SSA%20svg/Kinetic%20Friction.svg).


# P7.4 - Heisenberg's uncertainty relation
Heisenberg proved in 1972 that we cannot exactly know the velocity of an article and its position _at the same time_. This means that if we know precisely the velocity of a particle, we will not be able to have a precise mesurement of the position of the particle, and vice versa.
This can be written mathematically as:

$\Delta x \Delta p \geq \frac{h}{4\pi}$

where,
- $\Delta x$ is the uncertainty (a measurement of how precise a mesurement is) of the position of the particle
- $\Delta p$ is the uncertainty of the momentum of the particle.

we will use that Vi bruker at $h \approx 6.626 \times 10^{-34}$

writhe the program and use the function `assert` to test the relation.
Test your program where,

$\Delta x_{1} = 3.10165 \times 10^{-9}$ m, $\Delta p_{1} = 1.7 \times 10^{-26}$ kgm/s

$\Delta x_{2} = 5.2 \times 10^{-32}$ m, $\Delta p_{2} = 1 \times 10^{-3}$ kgm/s.

The uncertainties $\Delta x_{1}$ and $\Delta p_{1}$ does not violate the principle. However, the uncertainties $\Delta x_{2}$ and $\Delta p_{2}$ will violate with the principle (and your program should therefore display an error massage for this case).

reference: 
- [Heisenberg Equation](https://www.bing.com/videos/riverview/relatedvideo?q=Heisenberg+Quantum+Mechanics&mid=0C1F3C05C6A16C1995FF0C1F3C05C6A16C1995FF&FORM=VIRE)


# P7.5 - Reflectivity
Crown glass has a refractive index of 1.51 in the visible spectral region. Calculate the reflectivity of the air-glass interface and the transmission of a typical glass window.

Solution:
The medium of glass is transparent, so that $\alpha=0$. 

1. The reflectivity

   $R=\frac{(n-1)^{2} + k^{2}}{(n+1)^{2} + k^{2}}$

2. Transmission

    $T=\frac{1-R}{1+R}$

