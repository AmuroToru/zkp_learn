# Low Degree And Multilinear Extension
## 将multivariate function扩展到polynomial
我们有一个multivariate function $f: \\{0,1\\}^v \to \mathbb{F}$其中 $\mathbb{F}$ 是有限域.g是定义域为 $\\{0,1\\}^v$ ,值域为 $\mathbb{F}$ 的v个0,1变量多项式。我们的目的是找到这样的多项式g使得 $f(x)=g(x)$
### def multiplinear polynomial：
一个multivariate polynomial g中每个变量的degree至多为1<br>
example: $g_1(x_1,x_2)=x_1x_2+x_1$ 是multiplinear polynomial，但是 $g_2(x_1,x_2)={x_1}^2x_2+x_1x_2+x_1$ 不是multiplinear polynomial

### multiplinear polynomial的拉格朗日插值
$multiplinear\ polynomial\widetilde{f}(x_0,...,x_v)=\sum_{w\in\\{0,1\\}^v}f(w)\chi_w(x_1,...,x_v)$<br>
其中，对于任意的 $w=(w_1,...,w_v)$ ,我们有： $\chi_w(x_1,...,x_v) :=\prod_{i=1}^v(x_iw_i+(1-x_i)(1-w_i)$

个人理解: $\chi_w(x_1,...,x_v)$ 本质是一个同或，当 $(w_1,...,w_v)=(x_0,...,x_v)$ 时， $\widetilde{f}(x_0,...,x_v)=f(x_0,...,x_v)$ 否则为0.


### 证明multiplinear extension 的唯一性
（反证法）设 $p,q \in \mathbb{F}$ 是由 $f: \\{0,1\\}^v \to \mathbb{F}$ extend的两个不相同的多项式.设 $h=p-q$ , $h$ 不为零多项式。当 $x\in\\{0,1\\}^v$ 时， $p=q,也就是h=p-q=0$ ，所以 $h$ 是非零多项式的vanishing polynomial. 设 $h$ 的任意一个degree最小的项为t，令 
 $x_i=0,x_j=1,其中x_i \in t,x_j \notin t$ 那么 $h(x)=t(x)\ne 0 与 h=p-q=0矛盾.$ 故 $h$ 是零多项式，即 $p=q$.

 ###
