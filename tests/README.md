# HPC System Test Collection -- W.I.P.

This collection includes tests for specific scientific applications and benchmarks that are used at various centers to validate functionality, performance, and stability of HPC systems. 

For each test added the following format is used:
```
<Application 1>/README.md
<Application 1>/Scripts/<build script>
<Application 1>/Scripts/<check script>
<Application 1>/<Test Name 1>/<test inputs>
<Application 1>/<Test Name 2>/<test inputs>
```

The `README.md` file should include the following information:
- Brief description of the application and links to source code
- Brief description of target system where the tests have been executed
- Build instructions on target system (include build script under `Scripts` if applicable)
- Instructions on how to verify correctness for each test case (include check script under `Scripts` if applicable)
- Description of test cases included
