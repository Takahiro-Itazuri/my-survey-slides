#### Gram-Schmidt Orthonormalization

@div[left]

__Abstract__<br>
Gram-Schmidt Orthonormalization is a method for orthonormalizing a set of vectors in an inner product space, most commonly the Euclidean space `$ \mathbb{R}^n $` equipped with the standard inner product. The Gram-Schmidt Orthonormalization takes a finite, linearly independent set `$S = \left\{ v_1, \cdots, v_k \right\}$` for `$ k \leq n $` and generates a orthogonal set `$ S' = \left\{ u_1, \cdots, u_k \right\} $` that spans the same k-dimensional subspace of `$k$`-dimensional subspace of `$\mathbb{R}^n$` as `$S$`.

@divend

@div[right]

__Method__<br>
Define the projection operator as follows:<br>
`\begin{align} {\rm proj}_{\boldsymbol{ u}} (\boldsymbol{ v}) = \frac{\langle \boldsymbol{ u}, \boldsymbol{ v} \rangle}{\langle \boldsymbol{ u}, \boldsymbol{ v} \rangle} \boldsymbol{ u} \end{align}`
where `$\langle \boldsymbol{ u}, \boldsymbol{ v} \rangle$` denotes the inner product of the vectors `$\boldsymbol{ u}$` and `$\boldsymbol{ v}$`.<br>
The Gram-Schmidt Orthogonalization then works as follows:<br>
`\begin{align} \boldsymbol{ u}_1 &= \boldsymbol{ v}_1 & \boldsymbol{ e}_1 &= \frac{\boldsymbol{ u}_1}{\|\boldsymbol{ u}\|_1} \\ \boldsymbol{ u}_2 &= \boldsymbol{ v}_2 - {\rm proj}_{\boldsymbol{ u}_1} (\boldsymbol{ v}_2) & \boldsymbol{ e}_2 &= \frac{\boldsymbol{ u}_2}{\|\boldsymbol{ u}\|_2} \\ \boldsymbol{ u}_3 &= \boldsymbol{ v}_3 - {\rm proj}_{\boldsymbol{ u}_1} (\boldsymbol{ v}_3) - {\rm proj}_{\boldsymbol{ u}_2} (\boldsymbol{ v}_3) & \boldsymbol{ e}_3 &= \frac{\boldsymbol{ u}_3}{\|\boldsymbol{ u}\|_3} \\ & \vdots & & \vdots \\ \boldsymbol{ u}_k &= \boldsymbol{ v}_k - \sum_{j=1}^{k-1} {\rm proj}_{\boldsymbol{ u}_j} (\boldsymbol{ v}_k) & \boldsymbol{ e}_{k} &= \frac{\boldsymbol{ u}_k}{\| \boldsymbol{ u}_k \|} \end{align}`

@divend