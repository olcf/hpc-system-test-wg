# Testathon 2026 – Working Group Notes

**Theme:** AI/ML testing

**Team name:** AIdiots

**Participants:**
- Nick Hagerty (ORNL)
- Cedric Jourdain (CINES)
- Ryan Adamson (ORNL)
- Andy Warner (HPE)

*Timeline*
- 60 min: Discussion
- 15 min: Define recommendations/prepare wrap-up

## 0. Existing Content

### a) Repositories

- https://github.com/karpathy/nanogpt - after 1 year, this was deprecated with a note that it is "very old"
- https://github.com/karpathy/nanochat
- https://github.com/jasonacox/TinyLLM -- often used as a precursor to vLLM
- [MINERVA test-suite](https://github.com/minerva4ai-eu/minerva-benchmarks)  collection of reproducible performance benchmarks for large language models on EuroHPC systems.
-  [MLPerf](https://www.nvidia.com/fr-fr/data-center/resources/mlperf-benchmarks/) From NVidia : "provide unbiased evaluations of training and inference performance for hardware, software, and services"
### b) Insights from 2024

Not a working group in 2024.

---

## 1. Scope and Objectives

Provide a brief overview of this testing area:
- **Description of the category:** discussions surrounding the testing and validation of AI and ML-based frameworks on HPCs.
- **Groupe focus/Session objective:** Open discussions around how we evaluate HPCs' capability to run AI/ML model training and inference.

## 2. Guiding Questions

Questions to structure the discussion:

- What should we be testing for AI users as Sites, Vendors, App Developers?
- What does "testing" AI/ML frameworks look like? Full static data-intensive models (e.g., OLCF-6 FORGE), micro transformer models, CCL microbenchmarks, something else?
- In a fast-moving AI landscape that changes by the hour, how can we try to implement regression testing (e.g., relatively static known-good workload)?
- How can we be handling correctness checking in testing?

## 3. Discussion Notes

Capture key points raised during the discussion:

- **Observations:**
    - Ryan A: do our current tests have enough in common with AI tests?
        - Somewhat, but there's specific parts of the AI stack that wouldn't be
        - e.g., PyTorch has a very large codebase
        - RCCL for communicaiton
        - Perhaps only 10% of our current set of tests would apply
    - Andy W: [MERbench] (https://proxyapps.exascaleproject.org/app/merbench/) as a proxy for inference workloads? Upcoming CUG paper this week.
    - How are we evaluating correctness in test training runs?
        - An SC'25 paper used loss function smoothness, and showed that memory corruption could cause the loss function to spike.
    - How much PyTorch software testing falls to the sites?
        - e.g., PyTorch 2.11 crashes intermittently with ROCm/7.2.
        - Transparency is desired from what tests are being run
            - These tests are likely developed by AI, and there would be thousands that may or may not be realistic.
    - Nick: Okay, we saw torch-hammer today from Isa. Does that play a role as a static PyTorch test? It tests torch.matmul, so does it do enough testing of the foundational parts of PyTorch?
        - Andy: (paraphrased) yes.
        - So +RCCL would maybe be good coverage?
    - Ryan: (after more discussion): this class of users seems to have different expectations than our typical mod-sim workloads.
        - Some of these things have never been run at scale before.
        - So should we be trying to proactively cover this case?
            - Maybe the starting point for AI/ML testing is focusing on hardware and network health, and making sure documentation is available.

- **Challenges:**
    - How can we test AI/ML applications without having to load large models

## 4. Key Takeaways (3–5 bullets max)

- Zeroeth order of business is ensuring that site hardware is capable of correctly running PyTorch intrinsics (torch.matmul)
    - i.e. using TorchHammer and/or FORGE or other models
    - Includes RCCL
- Sites should be involved in PyTorch validation, both from a how-did-the-vendor-test-this and a submit-tests-we-care-about-to-vendors perspective
    - Vendors give test environments (i.e. containers) to sites
    - Sites give tests or test enviornments to vendors
- Monitoring loss function of a relatively-known model across multiple independent training runs is a decent start to evaluating hardware correctness

## 5. Recommendations

Summarize practical recommendations emerging from the discussion:

- Recommendation 1: sites should consider implementing a torch-hammer-like hardware screening process.
    - Effort: Medium (Low if site has hardware screening today)
    - Impact: Low-to-medium
    - Note: adding correctness/comparison checks would raise impact 
- Recommendation 2: provide vendors with test cases of great importance.
    - Effort: Medium
    - Impact: Medium (dependent on vendor engagement)
    - Note: also benefits the site to have these tests as a check-out in new software versions

