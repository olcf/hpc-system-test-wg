# Testathon 2026 – Working Group Notes 

**Theme:** Interconnect / Filesystem tests

**Team name:** [be creative]

**Participants:**
- Cedric Jourdain (CINES)
- Name (Institution)

*Suggested Timeline*
- 10 min: Review existing content (repo and insight from 2024)
- 80 min: Discussion
- 20 min: Define recommendations
- 10 min: Prepare wrap-up

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

Provide a brief overview of this testing area:
- **Description of the category** : This category focuses on testing the performance, reliability, and stability of HPC interconnects (e.g. InfiniBand, Slingshot) and parallel filesystems (e.g. Lustre, GPFS, BeeGFS).  
- **Groupe focus/Session objective:** What is the main focus/goal of this group?  *(this can be refined during the session)*
    1. Evaluating how storage systems are tested and monitored, and where current practices fall short.
    2. Identify a **minimal and reusable set of interconnect and filesystem tests** that can be: run during acceptance, maintenance, and continuous validation
    3. Share **practical methods to detect performance regressions**
    4. Compare **real-world practices across sites** (e.g. I/O benchmarks

## 2. Detailed Tests

Links to repositories containing tests in that category  

*Please try to include only tests that could be useful for the broader community. Avoid tests that are specific to a single HPC site.*

| Test Name | Link to Sources | Type (e.g. regression, validation) | Testing Environment (e.g. ReFrame, Pavilion) | Description (what it does, when useful) | Maturity (Experimental / Used in production) |
|----------|----------------|------------------------------------|---------------------------------------------|-----------------------------------------|-----------------------------------------|
|          |                |                                    |                                             |                                         |                                          |
|          |                |                                    |                                             |                                         |                                          |
|          |                |                                    |                                             |                                         |                                          |

## 3. Guiding Questions

Questions to structure the discussion:

- How do we **detect interconnect or filesystem performance regressions** in practice?
- What are the relevant metrics? Do we have the tools to collect them? 
- Which I/O tests provide the most operational value today? 
- What signals or metrics are missing when diagnosing file system issues? 

## 4. Discussion Notes

Capture key points raised during the discussion:

- **Observations:**  
- **Challenges:**  
- **Differences between sites:**  
- **Tools / methodologies mentioned:**  

## 5. Recommendations

Summarize practical recommendations emerging from the discussion:

- Recommendation 1 [target (who?), effort ( Low/Med/High), Impact]
- Recommendation 2  


## 6. Key Takeaways (3–5 bullets max)

-
-
-
