# 2024 HPCTESTATHON
## HPC System Testing Workshop (with hands-on)

## Details
* **When**: 3-4 May, 2024, held in conjunction with [CUG 2024](https://cug.org/cug-2024/).
* **Where**: Pawsey Supercomputing Research Centre, 1 Bryce Avenue, Kensington 6151, Western Australia

## Description

This workshop brings together HPC experts and vendors from around the globe to share state-of-the-art HPC system testing methodologies, tools, benchmarks, tests, procedures, and best practices. The increasing complexity of HPC architectures requires a larger number of tests in order to thoroughly evaluate the status of the system after its installation or before a software upgrade is applied to production systems. Therefore, HPC centers and vendors use different methodologies to evaluate their systems during its lifetime, not only at the beginning during the installation and acceptance time, but also regularly during maintenance windows.

### Goal

The overall goal of this event is to establish a common and open HPC system test suite based on recommendations from the participants.

### Focus

The focus of the event will be on hands-on experience with open source tests shared by supercomputing sites (more information in "Data and code sharing" section below). Access to Pawsey's Setonix supercomputer will be made available for the participants to experiment with various tests to review their scope, usefullness and readiness for including in the HPC test suite.

Workshop will be focusing on:
* Basic scheduler and programming environment tests,
* Node health tests,
* Application-based regression tests,
* Various isolated system components tests, including interconnect, filesystem, memory, CPUs and GPUs.

### Program (tentative)

Note: each talk is 10+5min (10min presentation, 5min Q&A)

#### Friday, May 3, 2024

##### 9:00 - 9:15 Welcome

##### 9:15 - 10:00 Repositories and Tools Session 1

|Time|Speaker|Title|Short description|
|---|---|---|---|
|9:15 - 9:30|Paul Ferrell (LANL)|Crossroads Acceptance Testing with Pavilion|This talk will cover the library of acceptance tests we built in Pavilion for testing Crossroads, our new 6000 node Cray Shasta system.|
|9:30 - 9:45|Veronica Vergara Larrea, Nick Hagerty, John Holmen (OLCF)|HPC System Testing at the Oak Ridge Leadership Computing Facility|This talk will discuss the OLCF Test Harness, our test monitoring capabilities, and test suite.|
|9:45 - 10:00|Isayah Reed (Microsoft)|Cloud validation challenges: why current frameworks are inadequate|Cloud validation requires additional considerations that are not addressed by existing frameworks such as Pavillion, NHC, and Reframe - which assume on-site and mostly static clusters.|

##### 10:00 - 10:30 Morning Tea

##### 10:30 - 12:00 Repositories and Tools Session 2

|Time|Speaker|Title|Short description|
|---|---|---|---|
|10:30 - 10:45|Juan Herrera (EPCC)|EPCC's ReFrame testing strategies for ARCHER2 and Cirrus|This talk will cover the tests that EPCC carries out using ReFrame on ARCHER2 (HPE Cray EX with 5,860 CPU nodes) and Cirrus (HPE SGI 8600 with 280 CPU nodes and 38 GPU nodes).|
|10:45 - 11:00|Harold Longley, Jason Sollom (HPE)|Existing HPE Test Infrastructure|Explain the existing test infrastructure that ships with the CSM software including available system health tests. Goss servers run on worker nodes and new Goss tests could be launched with them.|
|11:00 - 11:15|Pascal Elahi, Craig Meyer (Pawsey)|HPC Testing using reframe at Pawsey|We will discuss our suite of MPI, GPU and SLURM tests implemented using the Reframe framework and a suite of unit tests, with particular focus on extracting diagnostic information when tests fail.|
|11:15 - 11:30|Benjamin Cumming (CSCS)|ReFrame - regression tests and benchmarks||
|11:30 - 11:45|TBC|||
|11:45 - 12:00|Gabriel Hautreux (CINES)|Stack deployment and tests at CINES|CINES implements an integrated solution to deploy versioned software stacks using gitlab CI, those stacks are deployed using Spack, and tested using reframe.|

##### 12:00 - 13:00 Lunch

##### 13:00 - 16:00 Working in groups: different aspects of HPC testing environment (afternoon tea available throughout)

##### 16:00 - 17:00 Conclusions and Results: each group presents results of their investigations

#### Saturday, May 4, 2024

##### 9:00 - 9:30 Welcome and wrap up of Friday results

##### 9:30 - 10:00 Talks Session 1

|Time|Speaker|Title|Short description|
|---|---|---|---|
|9:30 - 9:45|Jared Baker (NCAR/UCAR)|Complimenting Ansible Configuration with Ansible-based Testing|We have been leveraging Ansible to do configuration management on our solution with help of a scale-out runner system, Clushible. We have been working on creating a test suite runnable via Ansible.|
|9:45 - 10:00|Shivam Mehta (LANL)|An Approach to Continuous Testing|LANL's approach to test, monitor, and characterize the functionality and performance of HPC Clusters using Pavilion2 and Splunk with minimal user impact and no dedicated system time.|

##### 10:00 - 10:30 Morning Tea

##### 10:30 - 12:00 Talks Session 2

|Time|Speaker|Title|Short description|
|---|---|---|---|
|10:30 - 10:45|Craig West (BOM)|Acceptance testing and on-going benchmarking at BOM|This talk will provide information regarding how the Bureau of Meteorology uses Acceptance testing methods and the on-going reuse of these over the life of the systems.|
|10:45 - 11:00|Bilel Hadri (KAUST)|Lesson learned on acceptance and testing on KAUST EX HPC systems||

##### 11:00 - 12:00 Wrap Up and Future Work

##### 12:00 - 13:00 Lunch

### Data and code sharing
Supercomputing centres willing to share their open source tests are encouraged to submit them as part of the registration. Supercomputing centres using closed source testing procedures are welcome to participate in the event to experiment with tests presented by other sites. Providing links to open repositories and their descriptions is optional during registration.

### Connect with the HPC System Test Community
This workshop is organised as part of the HPC System Test working group. To join the HPC System Test working group Slack, please visit:
http://tinyurl.com/hpcsystemtest-slack

## Workshop registration

* Event is in-person only.
* Participation is limited to 45 individuals.
* Registration is open to all HPC professionals, with priority given to CUG 2024 attendees and individuals willing to share their open-source tests,
* Registration is required, please register [here](https://pawsey.org.au/event/2024-hpc-system-test-workshop-with-hands-on/).

## 2024 HPCTESTATHON General Chairs
* Verónica G. Melesse Vergara (ORNL, USA)
* Bilel Hadri (KAUST, Saudi Arabia)
* David Schibeci (Pawsey Supercomputing Research Centre, Australia)
* Sam Yates (Pawsey Supercomputing Research Centre, Australia)
* Maciej Cytowski (Pawsey Supercomputing Research Centre, Australia)
