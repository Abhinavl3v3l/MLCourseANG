# Week 2

### Multivariate Linear Regression 

**DATA SET**

| Feature $1$  | Feature $2$  | Feature $3$  | Feature $4$  | ......................................    | Feature $n$  | Result     |
| ------------ | ------------ | ------------ | ------------ | ----------------------------------------- | ------------ | ---------- |
| $x_1 ^{(1)}$ | $x_2 ^{(1)}$ | $x_3 ^{(1)}$ | $x_4 ^{(1)}$ | ......................................... | $x_n ^{(1)}$ | $y ^{(1)}$ |
| $x_1 ^{(2)}$ | $x_2 ^{(2)}$ | $x_3 ^{(2)}$ | $x_4 ^{(2)}$ | ......................................... | $x_n ^{(2)}$ | $y ^{(2)}$ |
| $x_1 ^{(3)}$ | $x_2 ^{(3)}$ | $x_3 ^{(3)}$ | $x_4 ^{(3)}$ | ......................................... | $x_n ^{(3)}$ | $y ^{(3)}$ |
| .            | .            | .            | .            | ......................................... | .            | .          |
| .            | .            | .            | .            | ......................................... | .            | .          |
| .            | .            | .            | .            | ......................................... | .            | .          |
| $x_1 ^{(m)}$ | $x_2 ^{(m)}$ | $x_3 ^{(m)}$ | $x_4 ^{(m)}$ | ......................................... | $x_n ^{(m)}$ | $y ^{(m)}$ |
>  Data set above have m feature set and one feature set  has $n$ features.

$m$  = Number of training feature sets

$n$ =  Number of training features

Example : 

1. $x_1 ^{(1)}$ = First feature with feature set index 1.

2. $x_7 ^{(5)}$  = Seventh feature of $5^{th}$ feature set.

3. $x_j ^{(i)}$ = $j^{th}$ feature of $i^{th}$ feature set.

A multivariate hypothesis function for $x^{(1)}$ feature set :
$$
h_\theta(x^{(1)}) = x_0 ^{(i)}\theta_0 + x_1 ^{(1)}\theta_1 + x_2 ^{(1)}\theta_2+ x_3 ^{(1)}\theta_3 ......+  x_n ^{(1)}\theta_n
$$

> Note :  $x_0 ^{(i)}$  = 1

Using the definition of matrix multiplication, our multi-variable hypothesis function for $x^{(1)}$  can be concisely represented as:  (n+1 feature vector)
$$
\begin{align*}h_\theta(x^{(1)}) =\begin{bmatrix}\theta_0 \hspace{2em} \theta_1 \hspace{2em} ... \hspace{2em} \theta_n\end{bmatrix}\begin{bmatrix}x_0 \newline x_1 \newline \vdots \newline x_n\end{bmatrix}= \theta^T x^{(1)}\end{align*}
$$
A multivariate gradient descent can be written as :


$$
\begin{align*} & \text{repeat until convergence:} \; \lbrace \newline \; & \theta_0 := \theta_0 - \alpha \frac{1}{m} \sum\limits_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) \cdot x_0^{(i)}\newline \; & \theta_1 := \theta_1 - \alpha \frac{1}{m} \sum\limits_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) \cdot x_1^{(i)} \newline \; & \theta_2 := \theta_2 - \alpha \frac{1}{m} \sum\limits_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) \cdot x_2^{(i)} \newline & \cdots \newline \rbrace \end{align*}
$$


Hence formulated as : 
$$
\begin{align*}& \text{repeat until convergence:} \; \lbrace \newline \; & \theta_j := \theta_j - \alpha \frac{1}{m} \sum\limits_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) \cdot x_j^{(i)} \; & \text{for j := 0...n}\newline \rbrace\end{align*}
$$




### Feature Scaling 

Why Feature Scaling ?  -  Makes Gradient Descent efficient. 

How?  -  Less Oscillation till convergence



Convergence depends on $\alpha$ . A small $\alpha$ value converges slowly and in contrast a large value can shoot away from convergence and hence may take even longer or perhaps may never converge.

Adding to this mix, huge scalar difference between features of a feature set will reduce the efficiency of the Gradient Descent algorithms