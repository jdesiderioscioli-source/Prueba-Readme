# Prueba-Readme


$$
\text{IsEmpty}: \Sigma^* \to \text{N} \quad / \quad \text{IsEmpty}(s) = 
\begin{cases} 
      0 &  \text{GetLength}(s) > 0 \\
      1 &  \text{GetLength}(s) = 0 
\end{cases}
$$

$$
\text{GetLength}: \Sigma^* \to \text{N} \quad / \quad \text{GetLength}(s) = 
\begin{cases} 
      0 &  \s \text{=} \varepsilon \\
      1 &  \text{1 + GetLength}(t) h . t, h \in \Sigma
\end{cases}
$$
