# Midterm Practicum

## Introduction
One of the challenges of constructing stoichiometric models of large reaction networks is quality assurance of the proposed chemical reactions, i.e., all the reactions we include in the model must be chemically balanced. If we have only a few reactions, we can check the correctness of the reactions by hand. However, this is not possible when we have models with hundreds or thousands of reactions (which are common when dealing with biochemical models). Thus, we need a method to identify when a reaction is not balanced that can be used for many reactions.

### Atom matrix
One way to check many reactions is to construct the atom matrix $\mathbf{A}$ whose rows are compounds, and the columns correspond to elements, e.g., $C,H,N,\dots$. Once we have the atom matrix $\mathbf{A}$, we can compute the difference matrix $\mathbf{\Delta}$:

$$
\mathbf{\Delta} = \mathbf{A}^{T}\mathbf{S}
$$

where $\mathbf{A}^{T}$ denotes the tranpose of the atom matrix, and $\mathbf{S}$ denotes the stoichiometric matrix. Non-zero values in the columns of the $\mathbf{\Delta}$ matrix indicate unbalanced reactions. 