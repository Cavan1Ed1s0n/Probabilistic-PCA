PCA phương pháp giảm chiều của bộ dữ liệu: tìm ra các principal component giữ lại nhiều thông tin của dữ liệu nhất. Các principal component được tìm ra được hiểu theo một nghĩa nào đó là latent variable

Biến tiềm ẩn (latent variable) là biến không được quan sát trực tiếp mà phải qua các suy luận thống kê.

Ví dụ độ hài lòng đối với cơ sở vật chất của nhà trường và giảng viên; mức độ thông minh qua điểm thi Toán Lý Hóa; hành vi của khách hàng qua cách họ chọn lựa và mua sản phẩm;...

x = Wz + $\mu$ + ϵ

p(z) = N(z|0, I)

p(ϵ) = N(ϵ|0, $\sigma^2$I)

p(x|z) = N(x|Wz + $\mu$, $\sigma^2$I)

p(x)=N(x|?)

E[x] =E[Wz + $\mu$+ ϵ]  
= WE[z] + $\mu$+ E[ϵ]  
= $\mu$

Cov[x] = E[$(x - \mu)(x - \mu)^T$]  
= E[(Wz + ϵ)(Wz + ϵ)$^T$]  
=E[Wzz$^T$W$^T$ + 2Wzϵ$^T$ + ϵ ϵ$^T$]  
= WE[z zT] W$^T$ + 2WE[zϵ$^T$] +E[ϵϵ$^T$]  
= WW$^T$ + $\sigma^2$I = C

Hence, p(x) = N(x|μ, C)



ln p(X|μ, W, σ$^2$)  = $\Sigma_{n=1}^N lnp(x_n|μ, W, σ^2) 
$  = $\Sigma_{n=1}^N ln N(x_n|μ, C)$

                             = $\frac{-Nd}{2} ln(2\pi) - \frac{N}{2}ln|C| - \frac{1}{2}\Sigma_{n=1}^N (x_n-\mu)^TC^{-1}(x_n-\mu)     $                                                                                                                

                                                                                                                                 [$x_n \in R^d$]

Lấy đạo hàm

$\Sigma_{n=1}^NC^{-1}(x_n - \mu)$ = 0 =>  $\mu = \frac{1}{N}\Sigma_{n=1}^Nx_n$

 $\sigma^2 = \frac{1}{D-M}\Sigma_{M+1}^D\lambda_j$                 
