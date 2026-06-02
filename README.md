# Prueba-Readme


$$
\text{IsEmpty}: \Sigma^* \to \lbrace 0, 1 \rbrace  /  \text{IsEmpty}(s) = 
\begin{cases} 
      0 &  \text{GetLength}(s) > 0 \\
      1 &  \text{GetLength}(s) = 0 
\end{cases}
$$

$$
\text{GetLength}: \Sigma^* \to \text{N}_0  /  \text{GetLength}(s) = 
\begin{cases} 
      0 &  s \text{=} \varepsilon \\
      \text{1 + GetLength}(t) &   h . t,  h \in \Sigma
\end{cases}
$$
$$
\text{AreEqual}: \Sigma^* \to \Sigma^* \to \lbrace 0, 1 \rbrace / \text{AreEqual}(s, n) = 
\begin{cases} 
      0 &  (s \neq \varepsilon \land n = \varepsilon) \lor (s = \varepsilon \land n \neq \varepsilon) \\
      0 & h_1 \neq h_2 \quad  s=h_1 . t_1,  h_1 \in \Sigma \quad \land\ n=h_2 . t_2,  h_2 \in \Sigma\\
      \text{AreEqual}(t_1, t_2) &  h_1 = h_2 \quad  s=h_1 . t_1,  h_1 \in \Sigma \quad \land\ n=h_2 . t_2,  h_2 \in \Sigma\\
      1 &  s = \varepsilon \land n = \varepsilon
\end{cases}
$$
$$
\text{AreDecimalDigits}: \Sigma^* \to \lbrace 0, 1 \rbrace  /  \text{AreDecimalDigits}(s) = 
\begin{cases} 
      0 &  h \notin \text{N}_0 & h . t,  h \in \Sigma\\
      \text{AreDecimalDigits}(t) & h \in \text{N}_0\\
      1 &  s = \varepsilon
\end{cases}
$$
$$
\text{Contains}: \Sigma^* \to \Sigma \to \lbrace 0, 1 \rbrace  /  \text{Contains}(s,n) = 
\begin{cases} 
      0 &  s = \varepsilon \\
      \text{Contains}(t,n) & h \neq n & h . t,  h \in \Sigma\\
      1 &  h = n
\end{cases}
$$
$$
\text{Count}: \Sigma^* \to \Sigma \to \text{N}_0  /  \text{Count}(s,c) = 
\begin{cases} 
      0 &  s \text{=} \varepsilon \\
      \text{1 + Count}(t,c) &  h = c & h . t,  h \in \Sigma \\
      \text{Count}(t,c) &  h \neq c
\end{cases}
$$
$$
\text{ToInteger}: \lbrace s \in \Sigma^* \mid \text{AreDecimalDigits}(s)=1\rbrace\to \text{N}_0  /  \text{ToInteger}(s) = 
\begin{cases} 
      0 &  s = \varepsilon \\
      h * 10^\text{GetLength(s)-1} +  &  \text{ToInteger}(t) \quad h . t,  h \in \Sigma \land h \in \text{N}_0
\end{cases}
$$
