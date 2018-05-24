#### Gram-Schmidt Orthonormalization

@div[left]

__Abstract__<br>
Gram-Schmidt Orthonormalization is a method for orthonormalizing a set of vectors in an inner product space, most commonly the Euclidean space `$ \mathbb{R}^n $` equipped with the standard inner product. The Gram-Schmidt Orthonormalization takes a finite, linearly independent set `$S = \left\{ v_1, \cdots, v_k \right\}$` for `$ k \leq n $` and generates a orthogonal set `$ S' = \left\{ u_1, \cdots, u_k \right\} $` that spans the same k-dimensional subspace of `$k$`-dimensional subspace of `$\mathbb{R}^n$` as `$S$`.

@divend

@div[right]

__Method__<br>
Define the projection operator as follows:<br>
`\begin{align} {\rm proj}_{{\bf u}} ({\bf v}) = \frac{\langle {\bf u}, {\bf v} \rangle}{\langle {\bf u}, {\bf v} \rangle} {\bf u} \end{align}`
where `$\langle {\bf u}, {\bf v} \rangle$` denotes the inner product of the vectors `${\bf u}$` and `${\bf v}$`.<br>
The Gram-Schmidt Orthogonalization then works as follows:<br>
`\begin{align} {\bf u}_1 &= {\bf v}_1 & {\bf e}_1 &= \frac{{\bf u}_1}{\|{\bf u}\|_1} \\ {\bf u}_2 &= {\bf v}_2 - {\rm proj}_{{\bf u}_1} ({\bf v}_2) & {\bf e}_2 &= \frac{{\bf u}_2}{\|{\bf u}\|_2} \\ {\bf u}_3 &= {\bf v}_3 - {\rm proj}_{{\bf u}_1} ({\bf v}_3) - {\rm proj}_{{\bf u}_2} ({\bf v}_3) & {\bf e}_3 &= \frac{{\bf u}_3}{\|{\bf u}\|_3} \\ & \vdots & & \vdots \\ {\bf u}_k &= {\bf v}_k - \sum_{j=1}^{k-1} {\rm proj}_{{\bf u}_j} ({\bf v}_k) & {\bf e}_{k} &= \frac{{\bf u}_k}{\| {\bf u}_k \|} \end{align}`

@divend