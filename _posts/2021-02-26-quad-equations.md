---
layout: post
title: "Solving quadratic equations"
author: 'Alexandros'
categories: math
---

{% include mathjax.html %}


In this blog post I want to show simpler way to solve quadratic equations. I learned this method from [this](https://www.youtube.com/watch?v=MHXO86wKeDY) YouTube video of 3Blue1Brown and thought it would be nice to write a short blog post about it.

<a href="http://www.youtube.com/watch?feature=player_embedded&v=MHXO86wKeDY
" target="_blank"><img src="http://img.youtube.com/vi/MHXO86wKeDY/0.jpg" 
alt="Link to video" width="240" height="180" border="10" /></a>

# Getting started 

A quadratic equation is a polynomial equation of the form 

$$ \alpha x^2 + \beta x + \gamma = 0. $$

The roots of this equation are given by

$$ r_{1,2} = \frac{-\beta}{2\alpha} \pm \frac{\sqrt{\Delta}}{2\alpha}, $$ 

where the determinant $\Delta$ is equal to 

$$ \Delta = \beta^2 - 4\alpha\gamma. $$

This approach undoubtetly works but it may be tricky to remember the equations. There is another way to derive the roots, which is more intuitive in my opinion.

# A simpler approach

## Rewriting the equation 
We want to find the values of $x$ that satisfy $ \alpha x^2 + \beta x + \gamma = 0 $. 

We can factor out $\alpha$ and rewrite the equation as 

$$ \alpha \left( x^2 + \frac{\beta}{\alpha} x + \frac{\gamma}{\alpha} \right)  = 0. $$

Since $\alpha\neq0$, we can find the roots $r_{1,2}$ of the original equation by solving for 

$$ x^2 + \frac{\beta}{\alpha} x + \frac{\gamma}{\alpha} = 0. $$

## Sum and product of the roots 

Since $r_1$ and $r_2$ are the roots of the equation we can write 

$$ \begin{align*} x^2 + \frac{\beta}{\alpha} x + \frac{\gamma}{\alpha} = 0 &= (x-r_1)(x-r_2) \\ &= x^2 - (r_1 + r_2) \cdot x + r_1 \cdot r_2 \end{align*} $$

By matching the terms of the left and right side, we get the following:

$$ r_1 + r_2 = - \frac{\beta}{\alpha} \quad \text{ and } \quad  r_1  \cdot r_2 = \frac{\gamma}{\alpha}  $$

## Introducing new variables to simplify the problem

We let $m$ be the center of the two roots $r_1$ and $r_2$, and we name their distance $2d$. Now we can express the roots by using the variables $m$ and $d$:

$$ r_1 = m - d\;, \quad r_2 = m + d $$ 

Instead of solving for $r_{1,2}$ it is easier to solve for the values $m$ and $d$. Using the equations for the sum and the product of the roots we have that 

$$ \begin{align*} r_1 + r_2 &= m - d + m + d = 2m = -\frac{\beta}{\alpha} \quad \text{and} \\ 
r_1 \cdot r_2 &= (m-d)(m+d) = m^2 - d^2 = \frac{\gamma}{\alpha} \end{align*} $$

After rearranging we get 

$$ m = -\frac{\beta}{2\alpha} \quad \text{and} \quad d^2 = m^2 - \frac{\gamma}{\alpha} $$

We can now use these equations to easily calculate the values of $m$ and $d$ and then use these to calculate the roots of the quadratic equation. This approach works even when the roots are imaginary.

## Example 

Let's end this blog post with an example. Assume we need to find the roots of the quadratic polynomial $x^2 - 7x + 12$ ( $\alpha=1$, $\beta=-7$ and $\gamma = 12$ ). The roots are given by $r_{1,2} = m \pm d$. 

First we calculate the value of $m$:


$$ m = -\frac{\beta}{2\alpha} = -\frac{7}{2} = 3.5 $$

Now we calculate the value of $d$:

$$ d^2 = m^2 - \frac{\gamma}{\alpha} = 3.5^2 - 12 = 0.25 \Rightarrow d = \sqrt{0.25} = 0.5 $$

The roots of the polynomial are therefore

$$ r_1 = m - d = 3 \quad {and} \quad r_2 = m + d = 4 $$.