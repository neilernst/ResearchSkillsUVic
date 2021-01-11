created 2007-12-18 22:45

Software-based systems are subject to change pressures (various papers). Adapting these systems requires more than updating source code or architectures: profound changes (of the types Harker mentions) can only be made with reference to the requirements that system is created to satisfy. We need requirements models throughout the lifecycle, but particularly at run-time. Run-time models provide the maintainer guidance for machine-level changes like refactoring. Persisting these models requires a configuration management system that will allow us to: 
    •   identify potential changes
    •   maintain separate versions
    •   report on changes
    •   maintain relationships between models and code
    •   control changes (from pressman). 
This thesis first describes the purpose of each component in the context of requirements models.  Having introduced the theory, I then describe my implementation of a requirements configuration management tool that supports these abstract operations. Specifically: 
    •   a version control system for i* models. Version control needs to be able to a) maintain system artifacts, b) record the changes made to them over time c) merge those changes when necessary. This system acts on the model elements directly, rather than their serialization (e.g. XMI). We keep the stakeholder in the problem domain (properly the domain of requirements). We show how this works with a case study (Trac).
    •   query support for understanding and reporting on models and model changes. Queries answer questions like "what changed from last time", "what is the impact of those changes", "what is the difference between modeler A and modeler B's version".
    •   visualizations for displaying our queries. This supports the cognitive work of the tool-user by relieving the burden of model comprehension.
    •   an empirical case study that validates the tool and methodology (methodology unclear as yet) on a real-world scenario, the ongoing maintenance of a medical informatics system (tentative).

Questions and objections
    •   what are your contributions? Who helped and how much? 
    •   industrial tool X does this. Why are you duplicating that effort? 
    •   traceability? 
    •   what are the phenomena involved? I can either do a case study that will highlight the phenomena (exploratory), or a case study/ies that will show how one can use my tool to improve a current process. I'm leaning to the 2nd one. I think there is already research into the problems, e.g. Kruchten's paper on transitioning to RUP and benefits of adapting legacy systems. One point in favour of an exploratory study is that we are also interested in specific questions that people have regarding the models, e.g. what queries/facets are they interested in.

