Andreas Mützel
==============

This is my personal page

:email: amuetzel (at) uni-koblenz.de
:project: KdTrees on GPU using CUDA
:mentor: **Marius Muja** (Stéphane Magnenat [Radu B. Rusu, Michael Dixon])

About me
--------

I'm a master's student  at the `University of Koblenz-Landau <http://www.uni-koblenz-landau.de>`_ in the Computational Visualistics program.
There, my main interests are image processing and robotics, and this is my first serious GPU programming project.

Apart from computer stuff, such as programming and games, my hobbies include playing the guitar, listening to heavy metal music and (recently) rock climbing.

Roadmap
-------

Here is a brief outline of my GSoC project milestones:

  * Get familiar with FLANN - http://www.cs.ubc.ca/~mariusm/index.php/FLANN/FLANN

    - is currently used in PCL for k-nn search and for radius-search
    - contains several index types, of special interest is the low dimensionality kd-tree index (KDTreeSingleIndex)
    - have a look at the FLANN public interface (flann::Index class), we would like the GPU implementation to use the same interface. If you think we need to change this interface in some way to allow better performance, we can discuss about it and come up with the best solution

  * KDTree on GPU

    - Get familiar with an existing kd-tree implementation on GPU: http://www.cs.unc.edu/~shawndb/
    - Benchmark against the CPU implementation and FLANN's KDTreeSingleIndex

  * 3D/4D kdtree GPU implementation in FLANN

    - Create GPU kd-tree implementation (may use lessons learned from Shanw's implementation and from the CPU implementation in FLANN)
    - Analise trade-offs and changes that a GPU implementation requires vs a CPU implementation
    - Profile the GPU implementation and the CPU implementation to understand the bottlenecks in each case
    - Document and write a tutorial on how to use the GPU implementation

  * High dimensional GPU implementation of existing FLANN algorithms

    - Is it feasible to implement any of the higher dimensional approximate nearest neighbor search algorithms from FLANN on GPU?
    - If yes, implement it and benchmark it against the CPU implementation.
    - Document and write a tutorial on how to use the GPU implementation


Click :ref:`here <amuetzel_roadmap>` for a more detailed roadmap


Recent status updates
---------------------

.. blogbody::
   :author: amuetzel
   :nr_posts: 5



.. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. .. 

.. toctree::
   :hidden:

   roadmap
   status
