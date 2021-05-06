# Cray User Group 2021 Birds of a Feather

## HPC System Test: Building a cross-center collaboration for system testing

### Description

This session builds upon an effort started at CUG 2019 and continued at SC19 in which several HPC centers gathered to discuss acceptance and regression testing procedures and frameworks. From that session, we learned there are many commonalities in the procedures and tools utilized for system testing. CSCS, KAUST, and NERSC use the ReFrame framework for regression testing. While other centers, like NCSA and OLCF, have built in-house tools for acceptance testing. From the experiences shared, we see there are many benchmarks and applications that are widely run which often become part of a local test suite. These common elements are a strong indication that a tighter collaboration between centers would be beneficial. Furthermore, as systems become more complex, leveraging the HPC community to develop and maintain the growing number of tests needed to assess a system is key. 

The BOF will include lightning presentations from HPC centers that are using different testing frameworks for regression and acceptance. These will be followed by discussions around these topics: 
* What challenges are centers currently facing in this area? 
* What role should the vendors play in testing? 
* How can we leverage testing efforts across centers to develop a maintainable collection of tests?
 
This BOF invites attendees participation to form the HPC System Test working group. The group will collaborate to define a set of guidelines and methodologies that can be used to build and maintain a collection of HPC system tests. All products from the session will be publicly available at: https://olcf.github.io/hpc-system-test-wg/

### When & Where

- *Date:* Thursday, May 6, 2021 from 9:00am to 11am (US Pacific Time).
- *Location:* Virtual.

### Speakers & Panelists

#### Reuben Budiardja (ORNL)
<img src="images/reuben_picture_70.jpeg" width="180" align="right"> Reuben Budiardja is a computational scientist in the National Center for Computational Sciences at Oak Ridge National Laboratory. He earned his doctorate degree from the University of Tennessee in Knoxville, Tennessee in computational astrophysics. He has broad research interests ranging from the development of large-scale astrophysics simulation code to investigate the mechanism of core-collapse supernovae to developing system tools to understand application motifs, usage, and performance on supercomputers. Throughout his career, he has collaborated with application scientists from various disciplines helping them to achieve their scientific objectives by exploiting supercomputing capabilities.

#### Ben Casses (LLNL)

#### Todd Gamblin (LLNL)
<img src="images/" width="180" align="right"> Todd Gamblin is a computer scientist in the Center for Applied Scientific Computing at Lawrence Livermore National Laboratory. His research focuses on scalable tools for measuring, analyzing, and visualizing parallel performance data. In addition to his research, Todd leads LLNL's DevRAMP (Reproducibility, Analysis, Monitoring, and Performance) team. He is the creator of Spack, a popular HPC package management tool, and he leads the Software Packaging Technologies area in the U.S. Exascale Computing Project. Todd has been at LLNL since 2008. He received the Early Career Research Award from the U.S. Department of Energy in 2014. He received Ph.D. and M.S. degrees in Computer Science from the University of North Carolina at Chapel Hill in 2009 and 2005, and his B.A. in Computer Science and Japanese from Williams College in 2002.

#### Jennifer Green (LANL)
<img src="images/" width="180" align="right"> Jennifer Green is an R&D Scientist IV in the High Performance Computing Environments Group at Los Alamos National Laboratory. She serves as the Team Leader of the Programming & Runtime Environments Team. The team is tasked with the installation, maintenance and support of scientific software on HPC resources as well as supporting production HPC system testing. Additionally, the team is heavily involved in acceptance testing of new procurements at LANL in HPC and develops the Pavilion test harness.

#### Joe Heaton (University of Bristol)

#### Vasileios Karakasis (CSCS)
<img src="images/" width="180" align="right"> Since November 2018, Vasileios has been leading the Scientific Computing Support Group after working for three  years as an HPC Application Specialist in the same group. As group lead, Vasileios manages the activities of the team to enable the CSCS user community to make the best use of the HPC environment that CSCS is providing. Vasileios specializes in performance engineering and regression testing. He has mentored teams in GPU Hackathons organized by the center and acted as the lead developer of a framework for regression testing and continuous integration of HPC applications. Furthermore, he is involved in directive-based GPU programming, representing the center in the OpenACC technical committee. Vasileios received a Ph.D. in high performance computing from the National Technical University of Athens.

#### George Markomanolis (CSC)
<img src="images/" width="180" align="right"> George Markomanolis is a Lead HPC Scientist at CSC - IT For Science Ltd in Finland. George holds a Ph.D. from INRIA/ENS de Lyon on computer science with topic "Performance Evaluation and Prediction of Parallel Applications", a M.Sc. in Computational Science from National & Kapodistrian University of Athens, and a B.Sx. in Mathematics from University of Ioannina. Prior to CSC, George was a HPC engineer at the Oak Ridge Leadership Computing Facility at ORNL. George is also a member of the IO-500 Commitee.

#### Shahzeb Siddiqui (LBNL)
<img src="images/" width="180" align="right"> Shahzeb Siddiqui is a HPC Consultant/Software Integration Specialist at Lawrence Berkeley National Laboratory/NERSC. Shahzeb spends 50% of his time on Consulting where he helps address any incoming issues reported by NERSC users and dedicates the rest of his time to the Exascale Computing Project (ECP)'s Software Deployment (SD) group where he is responsible for building Spack E4S CI pipeline for NERSC. Shahzeb is involved in several open-source projects including easybuild, spack, singularity, and creator of open-source project buildtest and lmodule. Shahzeb has experience with installing scientific software, cluster administration (configuration management and cluster manager tools), user support tickets, and scheduler configuration. Shahzeb holds a M.S. degree in Computer Science from KAUST and a B.S. in Computer Engineering from Penn State University.

### Moderators

#### Bilel Hadri (KAUST)
<img src="https://www.hpc.kaust.edu.sa/sites/default/files/files/public/GPU_Workshop/2017/bilel3.png" width="180" align="right">
Bilel Hadri is a Computational Scientist at the Supercomputing Core Lab at KAUST since July 2013. He contributes in benchmarking and performance optimization, helps in systems procurements, upgrades, and provides regular training to users. He received his Masters in Applied Mathematics and his PhD in Computer Science from the University of Houston in 2008. He joined the National Institute for Computational Science at Oak Ridge National Laboratory as a computational scientist in December 2009 following a Postdoctoral Position in June 2008 at the University of Tennessee Innovative Computing Laboratory led by Dr. Jack Dongarra. His expertise areas include performance analysis, tuning and optimization, System Utilization Analysis, Monitoring and Library Tracking Usage, Porting and Optimizing Scientific Applications on Accelerator Architectures (NVIDIA GPUs, Intel Xeon Phi), Linear Algebra, Numerical Analysis and Multicore Algorithms.

#### Verónica G. Melesse Vergara (ORNL)
<img src="images/vergara_picture_56.jpeg" width="180" align="right">
Verónica G. Melesse Vergara (Vergara Larrea) is originally from Quito, Ecuador. Verónica earned a B.A. in Mathematics/Physics at Reed College and a M.S. in Computational Science at Florida State University. Verónica has over a decade of experience in the high performance computing field and is currently Group Leader of the User Assistance — Pre-production Systems Group at the Oak Ridge Leadership Computing Facility. In addition to providing assistance to OLCF users, Verónica is part of the systems testing team, led acceptance for Summit, and is leading acceptance for Frontier, ORNL’s exascale supercomputer. Her research interests include high performance computing, large-scale system testing, and performance evaluation and optimization of scientific applications. Verónica is a member of both IEEE and ACM and serves in the ACM SIGHPC Executive Committee and the SC Steering Committee.

### Agenda

* Audience live survey: 3 mins
* Lightning talks: 10 minutes each
  * CSC: George Markomanolis
  * LANL: Jennifer Green
  * LLNL: Todd Gamblin, Ben Casses
  * University of Bristol: Joe Heaton 
* User Facility Panel: 45 mins
  * CSC, CSCS, KAUST, NERSC, LANL, LLNL, OLCF, University of Bristol.
* Open Forum:
  * Everyone welcome to chime in!
* Wrap up: 2 mins
  * Invitation to join HPC System Test Working Group
  * Next steps
  
* Q & A log
TBD
