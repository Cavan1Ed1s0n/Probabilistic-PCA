PCA phương pháp giảm chiều của bộ dữ liệu: tìm ra các principal component giữ lại nhiều thông tin của dữ liệu nhất. Các principal component được tìm ra được hiểu theo một nghĩa nào đó là latent variable

Biến tiềm ẩn (latent variable) là biến không được quan sát trực tiếp mà phải qua các suy luận thống kê.

Ví dụ độ hài lòng đối với cơ sở vật chất của nhà trường và giảng viên; mức độ thông minh qua điểm thi Toán Lý Hóa; hành vi của khách hàng qua cách họ chọn lựa và mua sản phẩm;...

$x = Wz + \mu + \epsilon$

$p(z) = \mathcal{N}(z|0, I)$

$p(\epsilon) = \mathcal{N}(\epsilon|0, \sigma^2I)$

$p(x|z) = \mathcal{N}(x|Wz + \mu, \sigma^2I)$

$p(x)=\mathcal{N}(x|?)$

$E[x] =E[Wz + \mu+ \epsilon] = WE[z] + \mu+ E[\epsilon] = \mu$

$$
\begin{align*}
Cov[x] &= E[(x - \mu)(x - \mu)^T]  \\
&= E[(Wz + \epsilon)(Wz + \epsilon)^T]  \\
&=E[Wzz^TW^T + 2Wz\epsilon^T + \epsilon\epsilon^T]  \\
&= WE[zzT] W^T + 2WE[z\epsilon^T] +E[\epsilon\epsilon^T] \\  
&= WW^T + \sigma^2I = C
\end{align*}
$$

Suy ra, $p(x) = \mathcal{N}(x|\mu, C)$.

$$
\begin{align*}
\ln p(X|\mu, W, \sigma^2)  &= \sum_{n=1}^N \ln p(x_n|\mu, W, \sigma^2)\\
&= \sum_{n=1}^N \ln \mathcal{N}(x_n|\mu, C)\\
& =\dfrac{-Nd}{2} \ln(2\pi) - \dfrac{N}{2}\ln{|C|} - \dfrac{1}{2}\sum_{n=1}^N (x_n-\mu)^TC^{-1}(x_n-\mu), \text{ with $x_n \in R^d$}
\end{align*}
$$

Lấy đạo hàm

$\sum_{n=1}^NC^{-1}(x_n - \mu) = 0 \Rightarrow \mu = \frac{1}{N}\sum_{n=1}^Nx_n$

 $\sum^2 = \frac{1}{D-M}\sum_{M+1}^D\lambda_j$
