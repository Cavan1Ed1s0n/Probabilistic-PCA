# Probablistic PCA

- latent variables (hidden/ hypothetical variable) _ k-dim

- $Z_i \sim N(0,1)$ cannot be observed

- the actual d-dim obesrvation is distributed conditionally on this latent variables.

- $x_i| z_i \sim N(\Lambda z_i +\mu, \varphi)$ , $x_i|z_i$ là Gaussian với $\Delta z_i\in \mathbb{R}^{d\times k}, \mu \in \mathbb{R}^d$.

- Since $z_i, x_i|z_i, \left[\begin{array}{l}
  x_{i} \\
  z_{i}
  \end{array}\right]$ gaussian, its marginal $x_i$ is Gaussian.

- By $p\left(x_{i}\right)=\int_{z} p\left(x_{i} ; z\right) d z=\int_{z} p\left(x_{i} \mid z\right) \cdot p(z) \cdot d z$ we can show that, $x_i \sim \mathcal{N}(\mu, \Lambda\Lambda^T+\varphi)$ .

- It's common to assume $\varphi=\sigma^2 Id$, then $\sigma^2 \rightarrow 0$ we recover the original ica solution in the sense that column space of $\hat{\Lambda}_{MLE}$ approaches the PCA subspace - the column space of $V_k$. 

- **Homework:** search probabilistic pca (tipping, bishop 1999 - 34 pages) [pca](https://www.google.com/url?sa=t&source=web&rct=j&url=http://www.cs.columbia.edu/~blei/seminar/2020-representation/readings/TippingBishop1999.pdf&ved=2ahUKEwjb_47E46v3AhVuyYsBHX97DlsQFnoECD4QAQ&usg=AOvVaw0ps1r4QLVg37Zi7fhbw-Kq) . 
  
  # 
  
  # Canonical correlation
  
  - aka _canonical variates analysis_, is a way of inferring information from cross-covariance matrices. 
  
  - If we have $X=(X_1, \dots, X_n)$ and $Y=(Y_1,\dots, Y_m)$ of random variables, and their correlation among variables, cca will find linear combinations of $X$ and $Y$.
  
  - Issues with PCA:   
    
    1) Supposed we have the labels $y$. There can be situations in which the most relevant directions in $x$ for understanding $y$ may not be the directions of greatest variation in $x$.
       
       *For example*, if data $x$ by nature was contaminatd with a long correlated noise signal, then PCA would find the noise dimensions, keep them and throw away those dimensions which we can get more relevant information for predicting $y$.   
    
    2) PCA is not invariant to be a change of units or scaling.
       
       *For example*, if we changed the units of some features from km to mm, then all values of their feature would increase to $10^6$ and this direction might be favored by PCA.
       
       $\rightarrow$ This is unavoidable since there's no natural reference point that would allow us to treat units as arbitary.
    
    Consequently, we need to have an approach to dimensionality reduction and discover of linear structure from data should take advantage of $(x,y)$, preferably, in a way that is rebuilt to linear transformations of both $x$ and $y$ individually. 



# Báo cáo 8/5

1. Intro (ít), những cái mà team nói.

2. Latent variable. (Hoàng) - example

3. Prob pca (Bảo & Hoàng) - example

4. Acknowledgement
