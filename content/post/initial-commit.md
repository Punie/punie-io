---
title: 'Initial Commit'
date: 2018-09-27T10:33:44+02:00
draft: false
keywords: []
description: 'Some first post'
tags: []
categories: []

mathjax: true
---

Lots of stuff coming !
This is gonna be fun.

<!--more-->

There will be code:

```haskell
module Maybe where (Maybe(..), map)

data Maybe a
    = Just a
    | Nothing

map :: (a -> b) -> Maybe a -> Maybe b
map f (Just x) = Just $ f x
map f Nothing = Nothing
```

and weird logic notation:

$$
\begin{array}{cl}
\displaystyle\frac{x:\sigma \in \Gamma}{\Gamma \vdash x:\sigma} & {T-Var}
\\\\\\\\
\\\\\\\\
\displaystyle\frac{\Gamma \vdash e_1:\tau_1 \rightarrow \tau_2 \quad\quad \Gamma \vdash e_2 : \tau_1 }{\Gamma \vdash e_1\ e_2 : \tau_2} & {T-App}
\\\\\\\\
\\\\\\\\
\displaystyle\frac{\Gamma,\;x:\tau_1 \vdash e:\tau_2}{\Gamma \vdash \lambda\ x\ .\ e : \tau_1 \rightarrow \tau_2}& {T-Lam}
\\\\\\\\
\\\\\\\\
\displaystyle\frac{\Gamma \vdash e_1:\sigma \quad\quad \Gamma,\,x:\sigma \vdash e_2:\tau}{\Gamma \vdash \mathtt{let}\ x = e_1\ \mathtt{in}\ e_2 : \tau} & {T-Let}
\\\\\\\\
\\\\\\\\
\displaystyle\frac{\Gamma \vdash e: \sigma \quad \overline{\alpha} \notin \mathtt{ftv}(\Gamma)}{\Gamma \vdash e:\forall\ \overline{\alpha}\ .\ \sigma} & {T-Gen}
\\\\\\\\
\\\\\\\\
\displaystyle\frac{\Gamma \vdash e: \sigma_1 \quad\quad \sigma_1 \sqsubseteq \sigma_2}{\Gamma \vdash e : \sigma_2 } & {T-Inst}
\end{array}
$$

Hope you enjoy it !
