## Mesh Smoothing

Mesh smoothing is concerned with the design and computation of smooth functions $$f : S \rightarrow \mathbf{R}^d$$ on a triangle mesh. The function $f$ can flexibly be chosen to describe, for instance, vertex positions, texture coordinates, or vertex displacements. In this notebook, I will show how to perform mesh smoothing using several techniques based on denoising and fairing.

Denoising is used to remove high-frequency noise from the function $$f$$. In most cases, $$f$$ denotes the vertex positions, which might be corrupted by high frequency noise due to a physical scanning process. Removing the noise (the high frequencies) and keeping the overall shape (the low frequencies) requires generalizing the concepts of frequencies and low-pass filters to functions living on discrete triangle meshes. 

Mesh fairing does not just slightly smooth the function $$f$$ in order to remove the high frequency noise. It also smooths the function as much as possible in order to obtain, e.g., an as-smooth- as-possible surface patch or an as-smooth-as-possible shape deformation.

This notebook has three different methods of how to calculate smoothing
