# Large Scale Data Processing: Project 2
- **1. Exact F2**
    - **Local Output:** Exact F2. Time elapsed:95s. Estimate: 8567966130
    - **GCP Output:** Exact F2. Time elapsed:113s. Estimate: 8567966130
- **2. Tug of War**
    - **Local Output:** Tug-of-War F2 Approximation. Width :10. Depth: 3. Time elapsed:1433s. Estimate: 42555593
    - **GCP Output:** Tug-of-War F2 Approximation. Width :10. Depth: 3. Time elapsed:1063s. Estimate: 36962002
- **3. BJKST**
    - **Local Output:** BJKST Algorithm. Bucket Size:20. Trials:5. Time elapsed:542s. Estimate: 5767168.0
    - **GCP Output:** BJKST Algorithm. Bucket Size:20. Trials:5. Time elapsed:645s. Estimate: 6815744.0
-**4. Comparison**
    - The Tug of War function, in comparison to the F2 function, was quite slow on the full dataset. However, when I tested multiple subsets of the large dataset, they were both relatively close to eachother in their frequency counts/estimations and speeds. The difference in the full ticket data-set was quite large, however, and the Tug of War estimate seemed to be slower, but seemed to process the data more accurately (at least in my expectation of the output). Thus, Tug of War may be the better choice for larger datasets if accuracy is the main goal. The BJKST function was much closer to the F0 function in all runs, the subsets and the full dataset. F0 was faster than BJKST in the full-size run ( 77s vs 542s+), and F0 had an output of 7,406,649. While BJKST had an estimate of 5,657,169 on my local Computer and and estimate of 6,815,744 on GCP, both with the same parameters. In the smaller subset trials, BJKST was roughly the same speed, if not faster. These results show that BJKST can be a reliable estimator for F0 within a relatively close range, and tends to get closer to the actual estimate with a larger bucket size. (For example, a bucket size of 5 did not give an estimate for me, while a bucket size of 100 gave me an estimate closer to F0, 20 tended to give estimates that were in the requested +/- 20% range, and often was more accurate than needed).

