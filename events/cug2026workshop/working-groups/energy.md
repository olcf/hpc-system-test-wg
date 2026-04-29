# Testathon 2026 – Working Group Notes 

**Theme:** Energy Measurement and Energy-Related Testing

**Team name:** Energy

**Participants:**

- Wael Elwasif [ORNL]
- Markus Mickael Muller [LRZ]
- Azita Sadri [HPE]
- Jeff Hanson [HPE]
- Mathieu Cloirec [Cines]

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

- **Description of the category**

This working group focuses on energy-related matters. This applies to tests that measure the energy consumption of a set of devices or a single device, a set of applications or a single application, or a set of jobs or a single jobs.

It also focuses on tests that can or could be used to verify the accuracy of energy measurements.

Finally, it addresses possible correlations or links between the tests studied in other working groups and energy.


- **Groupe focus/Session objective:** 

The main focus of this group is to find energy tests or tests related to energy characterisation, 
determine energy criteria, check whether there are any tests available to verify the accuracy of energy measurement tools and to determine the status of these tests (exist : Yes/No, in development: Yes/No, in production : Yes/No)

## 2. Detailed Tests

Links to repositories containing tests in that category  

*Please try to include only tests that could be useful for the broader community. Avoid tests that are specific to a single HPC site.*

| Test Name | Link to Sources | Type (e.g. regression, validation) | Testing Environment (e.g. ReFrame, Pavilion) | Description (what it does, when useful) | Maturity (Experimental / Used in production) |
|----------|----------------|------------------------------------|---------------------------------------------|-----------------------------------------|-----------------------------------------|
| olcf-test-harness          |     https://github.com/olcf/olcf-test-harness        |   node health                                |                                             | potentially interesting when node health test returning  "power default or failure"                                     |                                          |
| Reframe-MPI-Stress-Tests         |   https://github.com/PawseySC/Reframe-MPI-Stress-Tests    |   regession test    |  reframe |  potentially get back GPU/CPU power during mpi test and send it to python metrics’ dictionnary                                     | 
HPE torch-hammer | https://github.com/hpe/torch-hammer  | kind of node health :   tests hardware power/thermal  - hardware performance and identify slow components | | Telemetry Back-ends, Key Features : Live telemetry |
hpctestlib microbenchmarks gpu burn | https://github.com/eth-cscs/cscs-reframe-tests | node health | reframe | get back Temperature |
AI benchmark initiative :  MLPerf with neuralwatt, zeus,ecologist and codecarbon | https://pypi.org/project/ai-energy-benchmarks, https://www.neuralwatt.com, https://mlco2.github.io/codecarbon/, https://github.com/mlco2/codecarbon/tree/7e2676aea57aa67c5768e69e442e1d6479a150e4/codecarbon/core| energy test| | Power Measurement : metrics such as energy consumed per inference and inferences per joule, energy from CPU and GPU,carbon emissions and abiotic resource consumption / units used over all the tests : watt-hours, Joules, MJ / kWh measure : Primary Energy (PE, total amount of primary energy required to produce one kWh)|

- adds : Article Site SIte • Networking and Storage : Exploring the sustainable scaling of AI dilemma: A projective study of corporations’ AI environmental impacts”
              

## 3. Guiding Questions

Questions to structure the discussion:

- Question 1  
  - What are the relevant metrics for energy ?
    It depends on which sensors are available -> Joules, watt, flops/watt, temperature, 

- Question 2
  - Do we have tools to collect them, what might we be missing, what is the current status of these tools ?
  - yes, at different level : support team (ex: rocm-smi), sys-admin (hpcm), hpc center, vendor
but how to have acces to all those data ?

- Question 3  
  - Are there any tests to check energy measurement tools—calibration standards ?




## 4. Discussion Notes


- **Observations:** 
  - User are not really interested with energy measure but user support and sys-admin a lot as HPC center as a whole
  - Different levels :
    - HPC center, : cdu cabinet, rack, cooling
    - Admin level : node, switch, ...
    - User or support level
  - For node health reason capturing throttling is very important
  - How to choose the interval when capturing value or measuring
    - interval size depends of sensors and device we monitor
    - how to choose interval size function of amount of data produced    
  - tools : user level (rocm-smi, pm_counters, admin level (hpcm, cray_pm), HPC center level)
  - accuracy of measure depends of number of components implied  

- **Challenges:** 
  - From a sys admin or support team point of view : have access to all measures :  CDU, switch, ssd, filesystem, cooling ...
  - Accuracy of measure to diagnosis. For example the distribution of jobs, apps can be very different ; the workload is not regular and identical day to day 
  - The granularity is one a point we have to deal with

## 5. Recommendations

- Recommendation 1 
  - Choose suite of different tests (mini-apps, synthetics, real applications)
- Recommendation 2
  - Find a way to have acces to all collected data.

