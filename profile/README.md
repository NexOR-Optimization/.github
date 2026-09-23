## NexOR Optimization

**We turn hard optimisation problems into plans you can run.**

NexOR is an optimisation company for industry, based in Court-Saint-Étienne, Belgium. We
write the mathematics that turns constraints, costs and capacity into a schedule, an
allocation or a plan that holds up in production, and we maintain the solvers behind it.

This organisation holds the open part of that work: the bridges between the
[JuMP](https://jump.dev) modelling language and the solvers underneath it, the modelling
layers on top of them, and the client that reaches our servers. One of our founders is a
JuMP core developer; the team ships pull requests against the core packages and presents
at JuMP-dev.

### What we maintain here

| Package | What it does |
| --- | --- |
| [NexOR.jl](https://github.com/NexOR-Optimization/NexOR.jl) | Julia client for our solve API. A JuMP model solves on our servers instead of the local machine, and the results come back into the same session. |
| [JuMPy](https://github.com/NexOR-Optimization/JuMPy) | Python interface to MathOptInterface. Models are written once as templates and expanded in compiled Julia, so building a large model stops costing more than solving it. |
| [MathOptVRP.jl](https://github.com/NexOR-Optimization/MathOptVRP.jl) | JuMP extension for vehicle routing. Stops, capacities and time windows expressed as a routing model JuMP can hand to any backend. |
| [ContractionHierarchies.jl](https://github.com/NexOR-Optimization/ContractionHierarchies.jl) | Shortest paths on OpenStreetMap graphs by contraction hierarchies. Builds the distance and travel-time matrices a routing model takes as input. |
| [Vroom.jl](https://github.com/NexOR-Optimization/Vroom.jl) | JuMP interface to VROOM, the widely used open source vehicle routing solver. |
| [MaxiCP.jl](https://github.com/NexOR-Optimization/MaxiCP.jl) | JuMP interface to MaxiCP, the constraint programming solver maintained at UCLouvain. |
| [OscaRCBLS.jl](https://github.com/NexOR-Optimization/OscaRCBLS.jl) | JuMP interface to OscaR.cbls, the constraint-based local search library from CETIC. Local search behind the same modelling language as the exact solvers. |
| [Hexaly.jl](https://github.com/NexOR-Optimization/Hexaly.jl) | JuMP interface to Hexaly, a commercial constraint programming and metaheuristics solver. |

Each keeps its own licence. They are bridges rather than lock-in: a model written against
them runs wherever you point it, on your machine or on ours.

### What we build on top

**[Optimization as a Service](https://nexoropt.com/products/solve).** Send any optimisation
problem as one model and call our solvers over HTTP. Every engine has a published price,
every run carries a cost cap you set, and you pay for the seconds you use. Name an engine,
or name a meta-solver and let it choose.
[Documentation](https://nexoropt.com/products/solve/documentation), or
[run a real model in your browser](https://nexoropt.com/products/solve/studio) with no
account and no card.

**[Transport Management System](https://nexoropt.com/products/tms).** Everything between the
order and the invoice: optimise the day's routes, dispatch them to the NexGo driver app,
follow the vehicles live on the map, invoice the finished work. Built as Odoo modules, on
your own database, with no per-driver fees.

### Why it is open

The bridges are code anyone can read, and so are most of the solvers they reach. The maths
is not a black box you have to take on trust, and the models you write stay yours.

### Elsewhere

- Website: [nexoropt.com](https://nexoropt.com)
- Research and open source: [nexoropt.com/research](https://nexoropt.com/research)
- LinkedIn: [linkedin.com/company/nexor-optimization](https://www.linkedin.com/company/nexor-optimization/)
- Contact: [contact@nexoropt.com](mailto:contact@nexoropt.com)
