Survey Questions related to the data model in this markdown file. The file will evolve based on the github issue (https://github.com/physnerds/dune-accelerator-integration/issues/1).

#  DUNE Accelerator Integration Survey

This survey aims to gather information on how **data models** and **memory management** impact accelerator performance in the DUNE workflow. Your input will help improve accelerator integration strategies in the DUNE data reconstruction workflow.


1. **What Project do you work on the DUNE experiment?**
    - Proto-DUNE
    - DUNE-FD
    - NDLAr
    - Anything else


2. **What type of resource do you use for your workflow?** *Check all that applies*
    - SuperComputer Facility (NERSC, ANL, FNAL, CERN resources)
    - Cloud Computing (AWS, Google Cloud)
    - Institutional Computing Resources (University clusters, local HPC)

3. **Accelerator types used in your workflow?** *Check all that applies*
    - GPU
    - FPGA
    - Other (Please Specify)

4. **Percentage of the total compute time in the GPU?** *Give your best estimation if such studies are not done yet*
    - <10%
    - 10-20%
    - 20-40%
    - >40%

5. **What are the data formats used in your workflow**?
    - ROOT
    - HDF5
    - Others (Please specify)

6. **What is the structure of the data-model used in GPU targeted tasks of your workflow**
    - Flat arrays
    - Structure of Arrays
    - Arrays of Structure of Arrays
    - Arrays of Structures
    - Sparse Data representations
    - Custom format
    - Others (please specify)

7. **What is the typical size of the input data product(s)?**
    - < 1 GB
    - 1-10 GB
    - 10 - 100 GB

8. **Does the data goes through tranformation before and after offloading?** 
    - Yes
    - No
    - Depends on the workflow algorithm

9. **What is/are the GPU targeted languages used in your workflow? Example (CUDA, KoKKOS, SyCL, OpenMP, Rajja etc)**
    - CUDA
    - Kokkos
    - SyCL
    - OpenMP
    - RAJA
    - HIP
    - Others (please specify)


10. **What are the primary performance bottlenecks you experience?** *(Select all that apply.)*  
    - I/O bottlenecks (slow reading and writing of data)
    - High Memory usage
    - Computationally intensive tasks 
    - Poor parallel scaling of tasks
    - Inefficient data transformation before CPU to GPU (and vice versa) transfer of data

11. **Do you compress your data before offloading into the GPUs?**
    - Yes
    - No, but would like to
    - No, and compression would not provide benefits

12. **Have you encountered issues with memory fragmentation in large datasets?**  
    - Yes, frequently  
    - Occasionally  
    - No  


13. **Do you encounter memory leaks or excessive memory consumption in your current data processing framework?**  
    - Yes, frequently  
    - Occasionally  
    - No  

14. **Which of the following memory allocation strategies do you use?** *(Select all that apply.)*  
    - Pre-allocated fixed size device buffers to reduce runtime memory allocation overhead
    - Dynamic memory allocation inside Kernels
    - Shared memory inside GPU kernels to reduce global memory access overhead
    - Unified Memory (Eg: cudaMallocManaged) for automatic access of memory between CPU and GPU
    - Others (please specify)

15. **What are the challenges you face with your current data model?** *(Select all that apply.)*
    - Data format (in ROOT,HDF5) is not GPU-friendly, needs to go through tranformation
    - GPU to CPU memory (and vice versa) data transfer bottlenecks
    - Poor scaling in different GPU environments (example works well in Nvidia, poor in AMD GPUs)
    - Other (please specify) 
 

16. **Would a cookbook and/or test framework to validate data models and algorithms in GPUs within a standalone environment be helpful?**  
    - Yes 
    - Maybe 
    - No 

17. **Any additional comments or feedback?** *(Please share any other issues not covered by the survey)*  
