+++
title = "Gamma Function Proof"
date = 2018-11-10T16:48:08-07:00
weight = 0
chapter = true
pre = "<b>1. </b>"
+++

# Proof of Gamma Function Identity

This is a quick and easy proof I stumbled upon while doing some introduction to probability theory homework.

_Proposition:_  
\\( \int\_0^\infty y^k e^{-y} dy = k! \\)

Proof (by induction):  
Base Case (\\(k=0\\)):
\\( \int_0^\infty e^{-y}dy = 1 = 0! \\)  
Inductive Step:  
Assume \\( \int_0^\infty y^k e^{-y} dy = k! \\). Then  
\\( \int_0^\infty y^{k+1} e^{-y} = (k+1) \int_0^\infty y^k e^{-y} dy = (k+1)(k!) = (k+1)! \\)  
This completes the proof.
