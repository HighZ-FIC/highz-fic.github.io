## Parthenon 
[Parthenon](https://github.com/parthenon-hpc-lab/parthenon) is a DOE-funded performance portable block-structured adaptive mesh refinement framework. This framework uses Kokkos for performance portability, and uses a device-first/device-resident approach as well as device-to-device communication and a task-based parallelism model to maximize computational performance and minimize node-device communication. The excellent scalability of Parthenon has been demonstrated on the largest CPU
and GPU-based machines available. Most notably, the PARTHENON-HYDRO app on Frontier reaches a total of 1.7×1013 zone-cycles/s on 9,216 nodes (73,728 logical GPUs) at ∼92% weak scaling parallel efficiency from 1 to 9,216 nodes. This Parthenon scaling work has been done with second order finite volume methods, but Parthenon can handle arbitrary ghost zones and on-cell-centered quantities (i.e., node-, face-, and edge-centered fields in addition to cell-centered) as well as multi-stage integrators which together can support high order finite difference, finite volume, and discontinuous Galerkin (DG) algorithms.
High-order DG schemes are known to be advantageous on GPUs due to their high arithmetic intensity. In addition, Parthenon is designed with abstraction layers that make it easy to implement new algorithms in a performance portable way. 


## MFEM 
MFEM is a DOE-funded scalable C++ libarary for adaptive finite elements. The algorithms in this project, using DG and novel WENO bases with positivity-preserving, will be directly deployed on MFEM. In particular, the novel WENO algorithm will be deployed as a new basis using the current DG interface of MFEM. Such a deployment only requires one to provide the shape functions on desired elements, which is very feasible and low-risk. Note that a similar approach using Galerkin difference, a type of finite difference scheme, has been successfully deployed on MFEM by an external team. In addition, we will rely on MFEM’s GPU interface for a scalable implementation on exascale computers. 


## libROM
libROM is a DOE-funded scalable C++ library for data-driven physical simulation methods. It is the main toolbox that the reduced order modeling team at LLNL uses to develop efficient model order reduction techniques and physics-constrained data-driven methods. The particularly attractive features related to this project include its direct support for MFEM’s high-order finite element data, its modular interface to develop new features, its existing support of WSINDy, and its scalable implementation for DD ROMs. In addition, libROM supports several plasma-related examples such as 1D1V Vlasov-Poisson. However, to the best of our knowledge, libROM has not been tested on MHD. We will thus use libROM and the proposed ROM algorithms with practical MHD data. Note that libROM is not limited to high order finite element, and therefore training it
with the Parathenon data set is feasible.



<script type="text/x-mathjax-config">MathJax.Hub.Config({TeX: {equationNumbers: {autoNumber: "all"}}, tex2jax: {inlineMath: [['$','$']]}});</script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.2/MathJax.js?config=TeX-AMS_HTML"></script>
