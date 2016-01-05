Particle Swarm Optimization is a [Stochastic](https://en.wikipedia.org/wiki/Stochastic#Artificial_Intelligence, "Stochastic") [Optimization Techniqe](https://en.wikipedia.org/wiki/Mathematical_optimization) developed in 1995 by Dr. Eberhart & Dr. Kennedy. It is used to retrieve optimal or near-optimal results for continuous, non-linear functions.

**Inspiration**

PSO has its roots in Natural Phenomenon (Bird Flocking, Fish Schooling) and Evolutionary Programming & Genetic Algorithms.
As an Analogy, consider a 1000 birds flying in the sky over a region. If a lot of Bird food is dumped in a very small place on the ground and left undisturbed, something interesting begins to happen. Initially, one or two (or maybe more) birds may arrive at the spot and begin to eat the food. As time progresses, more and more birds, which were previously randomly spread out in the sky, begin to "converge" toward this spot where the food lies. Eventually, they all end up at or very near to that spot, trying to get some food!

**The Basics**

A PSO maintains a swarm of Particles. This Swarm is what the algorithms operates upon during each iteration of it. A Particle represents a potential solution to the described problem. The aim is to end up with a particle that represents the optimal or near-optimal (if contraints are tighter) particle.

More precisely, a particle is a N-Dimensional Vector of values, in which each dimension represents an input feature in the problem. For example, if the problem was to fill 5 blanks with numbers such that their sum = 100, possible particles for this problem might look like:

1. 20 + 5 + -13 + 19 + 21

2. 37 + 11.56 + -50 + 92 + 3

Particle #1 has 5 dimensions where the 1st Dimension holds value 20, the second holds 5 and so on.
Note that both these are valid particles, but Particle #2 is better because its value is closer to our goal, i.e., 93.56 (goal being 100). Hence, Particle #2 is a more optimal solution out of the 2.

(Of course, the most optimal particle is something like 20 + 20 + 20 + 20 + 20 or even 100 + 0 + 0 + 0 + 0)

The idea behind PSO is to start with a set of Particles (The Initial Swarm), and change the values of these particles during each iteration, thereby flying them through a multi-dimensional search space. In each iteration, every particle's position is adjusted according to its personal experience and that of other particles.

What is specific to a given problem is its [Objective Function](https://en.wikipedia.org/wiki/Test_functions_for_optimization). Once a problem (which is suitable for PSO) is analyzed, its solutions space, particle dimensions, constraints and Objective Function are determined. The goal of the PSO algorithm then becomes to minimize or maximize this objective function.

The particle which yields the most suitable value from the objective function under the given constraints becomes the optimal solution retrieved from PSO.
