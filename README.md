# Python MIP (Mixed-Integer Linear Programming) Tools

Python MIP is a collection of Python tools for the modeling and solution
of Mixed-Integer Linear programs (MIPs). MIP syntax was inspired by
[Pulp](https://github.com/coin-or/pulp). Just like
[CyLP](https://github.com/coin-or/CyLP) it also provides access to
advanced solver features like cut generation, MIPstarts and solution
Pools. Porting Pulp and Gurobi models should be quite easy.

Some of the main features of MIP are:

* high level modeling: write your MIP models in Python as easily as in
  high level languages such as
  [MathProg](https://en.wikibooks.org/wiki/GLPK/GMPL_(MathProg)): 
  operator overloading makes it easy to write linear expressions in Python;

* full featured:
    - cut generators and lazy constraints: work with strong formulations with a
    large number of constraints by generating only the required inequalities
    during the branch and cut search;
    - solution pool: query the elite set of solutions found during the search;
    - MIPStart: use a problem dependent heuristic to generate initial feasible
    solutions for the MIP search.

* fast: the Python MIP package calls directly the native dynamic loadable
  library of the installed solver using the modern python
  [CFFI](https://cffi.readthedocs.io) module; models
  are efficiently stored and optimized by the solver and MIP transparently
  handles all communication with your Python code; it is also compatible
  with the [Pypy](https://pypy.org/) just in time compiler, meaning that
  you can have a much better performance, up to 25 times faster for the 
  creation of large MIPs, than the official Gurobi python interface 
  which only runs on CPython;

* multi solver: Python MIP was written to be deeply integrated with the
  C libraries of the open-source COIN-OR Branch-&-Cut
  [CBC](https://projects.coin-or.org/Cbc) solver and the commercial solver
  [Gurobi](http://www.gurobi.com/); all details of communicating with 
  different solvers are handled by Python-MIP and you write only one
  solver independent code;

* written in modern statically typed Python 3 (requires Python
  3.5 or newer).
  
## Documentation
 
The Documentation for Python-MIP is available at:
https://python-mip.readthedocs.io/en/latest/

A PDF version is also available:
https://media.readthedocs.org/pdf/python-mip/latest/python-mip.pdf
 

