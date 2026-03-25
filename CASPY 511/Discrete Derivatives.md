The displacement operator takes straight from the Taylor Series:
$$f(x+a)=e^{a\partial_x}f(x)=1+a\partial_xf(x)+\frac12a^2\partial_x^2f(x)+\cdots$$
Taking the first order approximations in both directions gets you:
$$f(x+a)=1+a\partial_xf(x)$$
$$f(x-a)=1-a\partial_xf(x)$$
We can now write the first derivative of the function in terms of its nearest neighbors:
$$f(x+a)-f(x-a)=2a\partial_xf(x)$$
$$\partial_xf(x)=\frac1{2a}[f(x+a)-f(x-a)]$$
This is nice and symmetrical, but applying it twice:
$$\partial_x^2f(x)=\frac1{2a}[\partial_xf(x+a)-\partial_xf(x-a)]$$
$$=\frac1{4a^2}[f(x+2a)-f(x)-f(x)+f(x-2a)]$$
$$=\frac1{a^2}[f(x+a)+f(x-a)-2f(x)]$$
Gets you the discrete Laplacian:
$$\nabla^2_nf(x_0,\dots,x_n)=\frac1{a^2}\sum[f(x_i+\hat i)+f(x_i-\hat i)-2f(x)]$$
