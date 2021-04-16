# Shape Deformation
In this exercise, I will implement an algorithm to interactively deform 3D models. 
I will construct a two-level multi-resolution surface representation and use naive Laplacian editing to deform it.
The steps to achieve this behavior are the following:
1. Removing high-frequency details
2. Deforming the smooth mesh, and
3. Transferring high-frequency details to the deformed surface.
