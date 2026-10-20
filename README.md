# econ3916-lab08-hypothesis-testing

Objective
I tested whether the LaLonde NSW job training program raised 1978 earnings, and whether any effect was large enough to matter and not just statistically significant.

Methodology
Loaded the LaLonde NSW job training experiment: 445 people, 185 trainees and 260 controls.

Ran a one-sample t-test and a two-sample Welch's t-test on 1978 earnings.

Wrote Welch's t-statistic as my own function, welch_t(), and checked it against scipy on the full sample and on five subgroups.

Computed Cohen's d to measure the size of the effect, not only its significance.

Ran a power analysis to find the power of this study and the sample size needed to detect d = 0.3.

Tested the treatment effect in 5 overlapping demographic subgroups, then applied Bonferroni and Benjamini-Hochberg corrections for multiple testing.

Simulated p-value distributions when the null is true and when it is false.

Key Findings
Trainees earned $1,794.34 more than controls in 1978 (Welch's t = 2.6741, p = 0.0079).

Cohen's d was 0.2727, which tells me how large the difference is relative to the spread in earnings.

The power of this study was 0.808 (80.8%), and detecting d = 0.3 would need a sample size of 351 total participants (175 per group).

2 of the 5 subgroup effects were significant before correction, and 1 after Bonferroni.

The simulations showed how p-value behave under a true null and a false null, which helped me see why running many subgroup tests makes false positives more likely.
