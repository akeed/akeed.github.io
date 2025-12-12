# Work life so far: from quantum simulation to enterprise AI

**Åke Edlund, PhD**

If there’s a single thread through my working life, it’s this: I’ve spent three decades helping ambitious ideas survive contact with reality — by turning hard computation into systems people can trust, operate, and scale.

That journey has moved with the major shifts in computing itself. I started in the world of numerical simulation and high-performance computing, where performance and correctness are unforgiving. I then spent years inside large industrial systems, where reliability, security, and ownership matter more than elegant theory. From there I ended up at the heart of Europe’s grid and cloud efforts, building federated infrastructures across countries and institutions. And in the last decade, I’ve brought those lessons into enterprise analytics and AI — now including GenAI and agentic patterns—within a large telco operating across multiple countries and regulatory contexts.

I don’t think of this as “three careers.” It’s one work life, shaped by the same questions in different environments:

- How do we make the complex operational?
- How do we scale without losing control?
- How do we build systems that people can rely on—technically, economically, and organizationally?

---

## Learning to respect reality: numerical methods and quantum physics

I began in Engineering Physics at Uppsala University and quickly gravitated toward numerical methods and scientific computing. Early on, I learned what it means to be accountable to physics: if the method is wrong, the result is wrong — no amount of storytelling fixes it.

My master’s work explored transport-corrected numerical models for nuclear reactor simulations at ABB Atom. That opened the door to time-dependent quantum dynamics and the computational demands that come with it: large, stiff, high-dimensional problems that push both algorithms and machines.

My Licentiate (1996) focused on quantum time evolution in time-dependent fields using Krylov subspace methods. I completed my PhD at Technion (1999), working on parallel preconditioned Krylov methods for multidimensional quantum scattering—essentially building scalable solvers for problems that were too large, too expensive, and too important to treat casually.

What stayed with me from this period wasn’t just “HPC skills.” It was a mindset:

- correctness and performance are not negotiable  
- modelling choices and numerical choices are inseparable  
- scaling is as much about architecture as it is about algorithms  

---

## Trading elegance for responsibility: industrial systems and telecom

After the PhD, I moved into industrial roles—seven years that taught me a different form of discipline. Here, the customer is not a paper reviewer. Systems have users, outages, budgets, and real consequences.

I worked on mission-critical telecom systems, including core development of MySQL Cluster (NDB) at Ericsson. Later, at Sony Ericsson, I served as Chief Architect for multiple global IT systems. These were environments where the definition of “done” includes operability, security, migration paths, and long-term ownership.

This period deeply shaped how I think about architecture:

- “distributed” isn’t a buzzword — it’s a failure mode factory  
- security is a property of the whole system, not a component  
- governance, interfaces, and operational practice are part of the design  

---

## Federated computing at continental scale: building Europe’s grid backbone

In 2004, I returned to academia—but not to retreat from reality. I joined KTH and became Security Head for EGEE (Enabling Grids for eScience), at the time Europe’s largest distributed research infrastructure, led by CERN and supporting workloads around the Large Hadron Collider.

This was a formative chapter: multi-institution, multi-country, federated trust, heterogeneous operations. The technical challenges were real, but the governance challenges were just as decisive.

My work included leading security architecture and operations, establishing the Middleware Security Group together with Stanford, coordinating security development across federated infrastructures, and participating in executive management. In practice, it meant helping turn grid computing from an ambitious idea into something that could be run as a production scientific backbone.

What I took from EGEE was a clear lesson that keeps repeating in enterprise AI today:

> Federation is not a technical pattern. It’s a social contract, enforced by architecture and operations.

---

## From grid to cloud: turning federation into a platform era

Building on EGEE, I coordinated BalticGrid and BalticGrid-II, extending infrastructure and capability into the Baltic region. Along the way I helped initiate early cloud efforts such as BalticCloud, and created the BalticGrid Innovation Lab to connect startups and emerging needs to scalable infrastructure.

From 2009 onward I led or co-initiated major Nordic and Swedish cloud efforts (including SNIC Cloud, Nordic Cloud / NeIC, and related initiatives), and participated in shaping broader European direction. In 2010, I was appointed to the EU Cloud Expert Group, contributing to strategic work that influenced European cloud priorities and later Horizon 2020 investments.

This period sits at an interesting hinge in my work life: the moment when “distributed computing for science” began to look like “platform thinking.” It also reinforced a pragmatic truth:

- infrastructure only matters if people can adopt it  
- adoption requires usability, training, and clear responsibility boundaries  

---

## Entrepreneurship as a parallel track: making ideas survive outside the lab

Alongside infrastructure work, I stayed close to entrepreneurship and innovation ecosystems — startup coaching, accelerator work, advisory roles, and a few ventures of my own. I’ve always been interested in what happens when technical possibility meets market reality.

Those experiences trained another useful instinct: to think in terms of product, not just project. That doesn’t mean “sales pitch.” It means clarity about who benefits, how value is created, and what must be true operationally for a solution to be sustainable.

---

## Discovering the fourth paradigm: data-intensive computing

Around 2012, I founded the Data-Intensive Computing Group at KTH (within the HPCViz environment). The motivation was simple: we were moving from compute-centric workloads to data-centric ones, and the toolchains and architectural assumptions needed to change.

We became early adopters of Apache Spark, shaped by direct contact with the Berkeley AMPLab, Microsoft Cloud Futures, and the early Spark community. The practical win was the ability to run iterative analytics and machine learning workloads far more efficiently than the MapReduce-era stacks.

The applied work touched areas like bioinformatics, anomaly detection, streaming analytics, and security/intrusion detection—domains where the combination of data volume, iteration, and time-to-insight changes the entire architecture.

This chapter also reinforced something I still lean on:

- performance isn’t only about speed; it’s about feedback loops  
- the best architecture enables learning at scale  

---

## Moving into Telia: bringing platform thinking to enterprise analytics and AI

In 2015, I joined Telia Company. The move felt natural: a large, data-rich organization facing exactly the kinds of scale, governance, and reliability questions I’d seen in scientific infrastructures—now with commercial and regulatory constraints layered on top.

What changed wasn’t the nature of the challenge. It was the setting.

---

### Building foundations: Telia Analytics

In the early years, I worked as a mix of architect, data scientist, and technical lead while Telia Analytics took shape. The work was hands-on and foundational: shaping the architecture and ways of working, helping establish a shared data lake direction, and building platforms and use cases that proved the model could work.

A memorable part of this period was bridging communities: helping data scientists and engineers move from “traditional analytics” toward large-scale data processing and modern ML. Another was coordinating deep learning efforts—partly technical, partly educational—because capability only becomes real when enough people can use it responsibly.

---

### From building to steering: enterprise architecture for AI & Analytics

From 2019 onward, my role shifted toward defining and governing the overall analytics and AI architecture for Telia Group, spanning multiple countries and platforms. I lead a network of chief analytics architects and chair an architecture board covering AI, ML, deep learning, MLOps, GenAI, and now emerging agentic patterns.

The core of this work is not picking tools. It’s setting direction and guardrails:

- how we evolve platforms without breaking delivery  
- how we enable autonomy while maintaining cohesion  
- how we keep security, compliance, and operability built-in  
- how we move from pilots to sustainable capabilities  

Over time, the technical arc has been a staged evolution—BI to big data, to ML and deep learning, to MLOps, to GenAI—and now into agentic architectures. Each step adds power, and each step increases the need for strong interfaces, governance, and observability.

---

## What I’m focused on now: GenAI, agentic patterns, and sovereign hybrid reality

Today, the most interesting problems I work on sit at the boundary between “what’s possible” and “what’s permissible”:

- GenAI and LLM usage under real enterprise constraints  
- RAG and knowledge-centric architecture that can be governed  
- agentic patterns that remain secure, observable, and maintainable  
- hybrid and sovereign infrastructure where “just use the cloud” is not the answer  

In a way, it feels like coming full circle: high ambition, high complexity, and the need to make systems dependable at scale—except now the systems must also be explainable, auditable, and safe to operate.

---

## Closing perspective

My work life started with parallel quantum simulations, where every mistake shows up in the math. It continues today in enterprise AI, where mistakes show up in operations, compliance, and trust.

The through-line has stayed stable:

> Build systems that scale, stay understandable, and earn trust over time.

---

## References and selected writings

I’ve kept this section as pointers rather than a full publication list. If you want a complete academic bibliography and community participation list, I maintain that separately.

### Data-intensive computing

1. A. Gholami, A.-S. Lind, J. Reichel, J.-E. Litton, Å. Edlund, E. Laure,  
   *Platform-as-a-Service (PaaS) Privacy Threat Modeling for Emerging Biobank Clouds*, submitted to DBSEC 2014, 2014.

2. Å. Edlund,  
   *Data-Intensive Computing and the Future of Research*, in *Time to Think: Policy and Measurement in Internationalization and Competitiveness*, Springer, 2014.

3. L. Ahmed, Å. Edlund, E. Laure, O. Spjuth,  
   *Using Iterative MapReduce for Parallel Virtual Screening*, CloudCom 2013, 2013.

### Cloud computing and federated infrastructure

4. A. Gholami, Å. Edlund, E. Laure,  
   *Cloud Privacy Threat Modeling*, IFIP Summer School on Privacy and Identity Management, 2013.

5. L. Schubert, K. Jeffery, B. Neidecker-Lutz (eds.),  
   *A Roadmap for Advanced Cloud Technologies under H2020*, EU Cloud Expert Group Report, 2012. (Co-author: Å. Edlund)

6. Å. Edlund,  
   *Cloud Computing – Challenges and Opportunities for Swedish Entrepreneurs*, Swedish Entrepreneurship Forum, 2012. Book.

7. Å. Edlund et al.,  
   *Practical Cloud Evaluation from a Nordic eScience User Perspective*, VTDC’11, 2011.

8. E. Laure, Å. Edlund,  
   *The eInfrastructure Ecosystem: Providing Local Support to Global Science*, Wiley, 2011.

9. A. Gholami, Å. Edlund, E. Laure,
   *Cloud Privacy Threat Modeling*, 8th IFIP International Summer School on Privacy and Identity Management, Nijmegen, Netherlands, 2013.

10. Å. Edlund, I. Livenson,
    *Cloud Computing and Startups*, in *Cloud Computing: Methodology, Systems, and Applications*, CRC Press, 2011.

11. Å. Edlund,
    *Innovative Companies and Cloud Computing*, BELIEF Zero-In eMagazine, Issue 4, 2010.

12. L. Schubert, K. Jeffery (eds.),
    *The Future of Cloud Computing – Opportunities for European Cloud Computing Beyond 2010*, EU Cloud Expert Group Report, 2010. (Contributor: Å. Edlund)

13. Contribution to:
    *SIENA Roadmap on Distributed Computing Infrastructure for e-Science and Beyond in Europe*, released February 23, 2012.

### Scientific computing and quantum physics

14. U. Peskin, Å. Edlund, I. Bar-On,
    *Parallel Wave-Packet Simulations of Electron Transmission Through Water*, Journal of Chemical Physics, 112, 3220–3226 (2000).

15. I. Bar-On, Å. Edlund, U. Peskin,
    *Parallel Solution of the Multidimensional Helmholtz/Schrödinger Equation Using High-Order Methods*, Applied Numerical Mathematics, 33, 95–104 (2000).

16. U. Peskin, Å. Edlund, I. Bar-On, M. Galperin, A. Nitzan,
    *Transient Resonance Structures in Electron Tunneling Through Water*, Journal of Chemical Physics, 111, 7558–7566 (1999).

17. Å. Edlund,
    *Multidimensional Quantum Scattering Calculations by a Parallel Preconditioned Krylov Subspace Method*, PhD Thesis, Technion – Israel Institute of Technology, 1999.

18. Å. Edlund, U. Peskin,
    *A Parallel Green’s Operator for Multidimensional Quantum Scattering Calculations*, International Journal of Quantum Chemistry, 69, 167–173 (1998).

19. Å. Edlund, I. Bar-On, U. Peskin,
    *Parallel Computation of Multidimensional Scattering Wavefunctions for Helmholtz/Schrödinger Equations*, PARA98 – Applied Parallel Computing Conference, 1998.

20. Å. Edlund, I. Vorobeichik, U. Peskin,
    *High-Order Perturbation Theory for Helmholtz/Schrödinger Equations via a Separable Preconditioner*, Journal of Computational Physics, 138, 788–800 (1997).

21. U. Peskin, Å. Edlund, W. H. Miller,
    *Quantum Time Evolution in Time-Dependent Fields and Time-Independent Reactive-Scattering Calculations via an Efficient Fourier Grid Preconditioner*, Journal of Chemical Physics, 103(23), 1995.

### Popular science and media (selected)

22. Ny Teknik (Dec 19, 2012),
    *"Molnet ger Sverige nya jobb"*, with Per Adolfsson (Microsoft Sweden).

23. Sveriges Radio P1 – Vetandets Värld (Nov 2011),
    *"Datahallarna växer i takt med sociala medierna"*, interview.

24. Naturvetarna (May 2011),
    *"Datormoln med kraft att förändra IT-världen"*, interview.

25. SVT Web (Jan 2011),
    *"Inte förvånad att datorn vann"*, interview on IBM Watson.

26. KTH Press (Feb 2011),
    *"Vetenskapsmoln hjälper företag med hemläxan"*, interview.

27. Ny Teknik (June 2004),
    *“Han ska göra industrin sugen på supernätet”*, interview.
```
