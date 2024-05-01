K-Nearest Neighbors and Rapidly-exploring Random Trees

By: Stephen Connelly, Kyle Chen, Sophia Liu

This repository contains our group's optimized implementations of two robot planning algorithms: K-Nearest Neighbors (KNN) and Rapidly-exploring Random Trees (RRT). Both algorithms are provided in both serial and parallel versions to demonstrate performance differences.

K-Nearest Neighbors - both involve first computing distances between the query point and other sampled points, then performing merge sort to obtain the k nearest neighbors (closest to the query point)

RRT - the parallel implementation only parallelizes the "finding the nearest neighbor" step; both implementations are largely the same as a naive RRT otherwise

├── KNN

│   ├── k-NearestNeighborsParallel    # Serial implementation of KNN

│   └── k-NearestNeighborsSerial      # Parallel CUDA implementation of KNN

├── RRT

│   ├── RRTSerial    # Serial implementation of RRT

│   └── RRTParallel  # Parallel CUDA implementation of RRT

└── README.md

For both algorithms, either serial or parallel, there is an option to run the algorithm once verbosely, and a second option (currently commented) to calculate the average execution time over any number of trials.

All files are .ipynb Jupyber Notebooks and can be run in Google Collab, GCP Virtual Machines, or Jupyer Lab (needs access to GPU for Parallel implementations).
