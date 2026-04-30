# Testathon 2026 – Working Group Notes 

**Theme:** <e.g., Energy Measurement and Energy-Related Testing / Applications / Node Health>

**Team name:** Team Planificateur (Schedulers)

**Participants:**
- Team consisting of 7 folks representing HPC centres in US, Europe, Australia as well as HPE


## 0. Existing Content

### a) Repositories

- **OLCF**: https://github.com/olcf/olcf-test-harness  
- **Pawsey**: https://github.com/PawseySC/Reframe-MPI-Stress-Tests  
- **LANL**:  
  - https://github.com/lanl/benchmarks/  
  - Documentation: https://lanl.github.io/benchmarks/index.html  
  - https://github.com/hpc/pavilion2  
- **Microsoft**:  
  - https://github.com/Azure/azurehpc-health-checks  
  - https://github.com/ireed/HPC-reframe  
- **HPE**: https://github.com/hpe/torch-hammer  
- **CSCS**: https://github.com/eth-cscs/cscs-reframe-tests  
- **LLNL**: https://github.com/LLNL/benchpark  
- **EPCC**: https://github.com/EPCCed/epcc-reframe  
- **CINES**: https://git.cines.fr/external/cines-reframe-tests  

### b) Insights from 2024

Worksheets from the 2024 Testathon can be found here *(Please contact Maciej Cytowski if you need access.)* :  
https://drive.google.com/drive/folders/1yRejWr6dwbB6a2WHUfEEdGUBWfOhaqei  

---

## 1. Scope and Objectives

Provide a brief overview of this testing area. What are the schedulers testing use cases?:
- Check if the scheduler is scheduling the job as intended
- Testing at the scale – 100,000 jobs, how quickly scheduler can handle
- Testing of how quick turnaround is to boot a job especially if you bring new image to the node
- Prolog and epilog testing
- Node sharing and cgroups; reserving enough memory for GPFS on the node with cgroups
- Testing the software itself, e.g. can we crash scheduler?

## 3. Guiding Questions

Questions to structure the discussion:

- What do we test currently?  
- What we do not test yet?  
- What are the biggest challenges we face?  

## 4. Discussion Notes

Capture key points raised during the discussion:

- **What do we test?:**
- Can you run the job?
- Can you launch application?
- Did you get resources you requested
- Affinity testing
- Accounting
- Scheduler overhead (LANL)
- Node health tests - some sites implementing it before and some after the job
- Testing new configurations with scheduler simulators (available for PBS)
- Node health test – Slingshot testing
- Monitoring data from the scheduler – post analysis of performance of the scheduler and issues
- **What we do not test yet?:**
- Epilog tests overhead
- Do we check if what we put into prolog and epilog actually works?
- Checking if the scheduler actually schedules things correctly – potentially on TDS; multiple accounts needed
- Testing how long the scheduling actually takes
- Do we test anything around user experience of using the scheduler
- Job priority testing e.g. in the context of support for larger jobs (simulator can help)
- Slinky discussion – not many centres are using it yet, but some are preparing for it and then testing might need to include things like Kubernetes  
- **Challenges:**
- More you test, more time you take away from users; what is bare minimum set of tests
- Heterogeneous system - harder to manage, thousand different things to test
- Heterogeneous jobs
- Configuration changes and testing - available in PBS but not so much in Slurm
- How do you size your infrastructure (cluster) based on workflow requirements
- Looking at things over time e.g. network fabric errors – do we see increasing number of errors? when do we need to panic? where do we test it?  


## 5. Key Takeaways (3–5 bullets max)

- Simulators are are very useful to avoid problems when you change configuration of schedulers
- We do test a lot of things already and there are useful examples that sites can share
