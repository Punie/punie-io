---
title: 'Why I Love Types'
date: 2018-09-27T14:56:23+02:00
draft: true
keywords: []
description: ''
tags: []
categories: []
author: Hugo Saracino
---

Types (and consequently, type systems) are, to me, one of the most fascinating aspects of programming languages.
They constitute also one of their most polarizing features --- programmers love their holy wars: tabs vs. spaces, emacs vs. vim, and so on. Types are no different.

Personally, I always loved them. At times, I felt like some kind of masochist, relishing every instance of the compiler yelling at me that I ought to fix my code immediately if I wanted to get shit done.

Well, time for some introspection. Today, I will revisit in great (perhaps excruciating) details why I love them, and always have. Buckle up!

<!--more-->

## But, why?

```haskell
{-# LANGUAGE GADTs #-}

module Expr where

data Expr a where
  EInt  ::         Int                    -> Expr Int
  EBool ::         Bool                   -> Expr Bool
  EAdd  ::         Expr Int  -> Expr Int  -> Expr Int
  EAnd  ::         Expr Bool -> Expr Bool -> Expr Bool
  EEq   :: Eq a => Expr a    -> Expr a    -> Expr Bool

eval :: Expr a -> a
eval (EInt  x)   = x
eval (EBool x)   = x
eval (EAdd  x y) = eval x +  eval y
eval (EAnd  x y) = eval x && eval y
eval (EEq   x y) = eval x == eval y
```
