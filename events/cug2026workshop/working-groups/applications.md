# Testathon 2026 – Working Group Notes 

**Theme:** Applications

**Team name:** Siesta All the Time

**Participants:**
- Verónica (ORNL)
- Jesse (ORNL)
- Mathieu (AMD)
- Victor (CSCS)
- Dustin (ORNL)
- Juan (EPCC)
- Asa (ORNL)

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
- **Description of the category**: Application-focused testing
- **Group focus/Session objective:** This group will focus on regression and acceptance testing done utilizing real applications and representative test cases.

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

- How do you currently gather application tests from your user community?  
- Do you find that these tests are difficult to maintain? 
- How do you engage with the vendor on support for these tests?  

## 4. Discussion Notes

Capture key points raised during the discussion:

- **Observations:**  
    - Vendors more comfortable with public benchmarks and applications. 
    - Issues with compilers if it is not a current compiler. 
    - If applications are older, they will roll off. If there is a requirement to erase them, the vendor removes it. Vendor can ask author to keep them for longer.
    - 
- **Challenges:**  
    - How do you do knowledge management at the vendor?
        - Good scripting helps more than documentation in some cases
        - Confluence page, internal Gitlab, external Github for a limited set of tests
    - Turnover of application specialists
    - Sharing is a challenge
        - Even internally, knowledge about existing tests has to be transferred 
    - How many versions of a given application do you keep?
        - CSCS: provide two versions (e.g., LAMMPS)
        - EPCC: IO tests are available but not run frequently
        - ORNL: IO benchmarks weren't sufficient, so we had built an IO harness using real applications
    - Testing slingshot is very difficult due to automatic rerouting 
    - Profiling applications to detect issues
        - Performance hit adding profiling
    - How do you identify the best options to compile a given code?
    - Do you have experts assigned to specific domains?
        - CSCS had but moved to a different model
    - Is there value in developing application proxies?
    - Do you share configurations externally?
        - EPCC: repository with recipes for UK
        - All: Point users to how to build an application rather than build applications 
        - CSCS: invest in containers and user environments (squashfs that is mounted every time you run a job)
        - CSCS: enable CI/CD
    - Procurements include a list of contractual applications that are supported
        - CSCS/ORNL: no contractual list of apps that have to be supported as workloads evolved
        - EPCC: support a set of applications for the life of the system. Smaller set for procurements
            - Asked CSC for CP2k test cases
- **Differences between sites:**  
    - CSCS: average 1500 users with average of one application per user
    - EPCC: have more applications than microbenchmarks
    - AMD: partners with integrators for IO, spends most of the time on the real applications than synthetic
    - AMD: use the right tool for the job. Needs hands-on direct access to the versions of dependencies vs. relying on a tool like Spack
        - KISS: keep it simple, stupid
    - In one case, ran all possible combinations of a build to find the right combination of flags for your system
    - Spack brings in a lot of dependencies by default, though this is configurable
    - OFI and UCX performance differences. Complex to find the same recipe that is best
    - Compiler, libraries, test is targeting specific hardware
    - Users get a small allocation first and then apply for time
        - What if we offered more allocation to allow for "by default" instrumentation?
        - Allocations may be reduced, if performance improvements are offered to the user teams
    - CSCS: requires having run on a CSCS system
    - ORNL: requires showing that the code can run on AMD GPUs but not necessarily Frontier
    - EPCC: applications for a code that is known to run in the hardware you have, then it is ok
    - What happens if users are not using the full node?
        - CSCS: monitored and reported
        - EPCC/ORNL: do not automatically track as it is up to the user
    - What is the return of investment?
    - What levels of user support?
        - Some centers focus on all levels of users
        - Some centers focus on users that have experience on the system
- **Tools / methodologies mentioned:**  
    - Reframe
    - OLCF Test Harness
    - LDMS
    - Spack, CMake, EasyBuild

## 5. Recommendations

Summarize practical recommendations emerging from the discussion:

- Implement knowledge management and transfer system 
- Collect pointers to optimized configurations and test cases for commonly used applications


## 6. Key Takeaways (3–5 bullets max)

- Application tests are hard to maintain over time with some centers having dedicated support/application teams while others do not
- Optimized configurations are available but not easily findable/shareable
- Vendors interested in continuing to run applications from procurements with preference to open source ones
- Enabling users to build optimized applications is key 
- Ensuring users are fully utilizing nodes came up as a concern
- Knowledge management also came up as a concern
