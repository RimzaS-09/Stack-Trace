---
draft : false
title : "The Cordic Algorithm"
toc: true
next: impl
---

## Overview 
No matter what, all calculators, computers, microprocessors and chips all have to ask the same question, if they ever wish to perform anything more complicated than being an adding machine: How can I calculate trignometric functions? It's a simple question, but the solution to this problem that clever computer scientists found is far more intuitive and beautifully complete than most realise.

We start off in the 1950's. A computer scientist, _Jack E. Volder_, was working in the electronics department of the aircraft manufacturing company Convair. Convair had a problem: It needed to replace it's old analog resolver that was on it's B-58's with a new system that could be more accurate and responsive. In order to perform this, he conceived the CORDIC algorithm, Which will be the topic of this article today.

### Mathematical overview
Suppose that, for a given angle \(\theta\), we want to compute it's trigonometric properties[^1]. It is known that, as long as we have the result of \(\sin {\theta}\) and \(\cos {\theta}\), we can then calculate all and any result of performing a trigonomic calculation for \(\theta\).

For example, \(\tan {\theta}\) may be computed using the formula \(\tan{\theta} = \frac {\sin{\theta}} {\cos{\theta}}\),<br>
or \(\csc{\theta}\) may be calculated as \(\frac {1} {\sin{\theta}}\)

This simplifies what we have to do by a lot, but we can do better.<br>
Remember that both \(\sin\) and \(\cos\) are _periodic_ functions, meaning that for any given input \(\theta\), the result given from \(\sin{\theta}\) is __guaranteed__ to have another input that maps to it.<br>
For example, \(\sin {(\frac{5 \pi} {3})}\) and \(\sin {(-\frac{\pi} {3})}\) map to the same output.

![check](/images/cordic.png "Title")



### How can we use a Cordic algorithm?
The cordic algorithm can be used for 


[^1]: We can use the Cordic algorithm for any function, but we shall use trigonometry specifically, just as an example