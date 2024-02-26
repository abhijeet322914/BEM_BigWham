# BEM_BigWham

In this repository, some engineering problems are solved using the Boundary Element Method (BEM). For the BEM formulation, BigWHam library is used, which is developed under Prof. Brice Lecampion's Geo-Energy Lab (GEL) at École Polytechnique Fédérale de Lausanne (EPFL), Switzerland. For further details on BigWham: https://github.com/GeoEnergyLab-EPFL/BigWham. 

Filename and their descriptions:

griffith_mesh_convergence_study.ipynb: In this problem, an infinitesimal crack of width 2a (also called Griffith’s crack) is subjected to
far-field uniaxial tension σy as shown in part(i) of file _griffith.png_. Using the superposition principle, the problem in part(i) of file _griffith.png_ can be split into two parts, as shown in part (ii) and part (iii) of file _griffith.png_. Part (ii) corresponds to an infinite medium with no cracks subjected to far-field uniaxial tension. Part (iii) corresponds to an infinitesimal crack of width 2a subjected to tensile stress σy at the crack faces. As the problem in part (ii) can be easily solved, the solution of part (iii) is needed.

hirsch_unidirection_tension.ipynb: In this problem, a circular hole of radius a in an infinite medium is subjected to far-field uniaxial tension σy, as shown in part (i) of file _circular_hole.png_. By again using the superposition principle, the problem in part(i) of file _circular_hole.png_ can be split into two parts, as shown in part (ii) and part (iii) of file _circular_hole.png_. Part (ii) corresponds to an infinite medium with no cracks subjected to far-field uniaxial tension. Part (iii) corresponds to a circular hole of radius 2a subjected to tensile stress σy (values adjust with surface normal direction) at the circular face. As the problem in part (ii) can be easily solved, the solution of part (iii) is needed. The aim is to find the displacement field at the hole surface.

combined_problem_mesh_convergence_study.ipynb: In this problem, a circular hole in an infinite medium is subjected to internal pressure p
as shown in part (i) of file _combined_problem.png_. As demonstrated in the previous problem, it is currently not possible to solve the problem as the code is unable to obtain the correct T matrix. Hence, a combination of two problems is solved to get around the issue: a) a circular hole of radius r in an infinite medium subjected to internal pressure p, and b) a circular plate of radius r subjected to external pressure p. By keeping the internal radius and internal pressure of problem a) the same as the external radius and external pressure of problem
b), a displacement discontinuity problem is obtained, as shown in part (ii) of file _combined_problem.png_.

combined_problem_crack_pressure_area.ipynb: In this problem, a circular hole of radius r in an infinite medium is subjected to internal
pressure p with infinitesimal cracks of width a at diametrically opposite ends as shown in part (i) of file _combined_crack.png_. Again, the problem cannot be solved due to the unavailability of the correct T matrix. Therefore, a combination of two problems is solved to get around the issue: a) a circular hole of radius r in an infinite medium subjected to internal pressure p with cracks of width a at diametrically opposite ends, and b) a circular plate of radius r subjected to external pressure p. By keeping the internal radius and internal pressure of problem a) the same as the external radius and external pressure of problem b), a displacement discontinuity problem is obtained as shown in part (ii) of file _combined_crack.png_,

