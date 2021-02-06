# HPC System Test Collection -- Scratch pad.

## Questions to answer?
- What applications are centers running to test systems?
- What tools does each center use?
- Are the tests publicly available?
  - If not, could they be made available?
- How do we centralize this information? Possible ideas:
  - Keep a site that points to center-specific pages/repos (easy ask)
  - Come up with a standard format to submit tests depending on minimum requirements needed? (harder ask)

This collection includes tests for specific scientific applications and benchmarks that are used at various centers to validate functionality, performance, and stability of HPC systems. 

## Sites 

### Minimum info needed per test - W.I.P.

The `README.md` file should include the following information:
- Brief description of the application and links to source code
- Brief description of target system where the tests have been executed
- Build instructions on target system (include build script under `Scripts` if applicable)
- Instructions on how to verify correctness for each test case (include check script under `Scripts` if applicable)
- Description of test cases included
