---
layout: post
title: "Thoughts on SuiteSparse"
date: 2023-05-23 15:48:00
description: My first research project is using this to benchmark and so I read up on the paper and thought I'd share my thoughts!
tags:
 - papers
---

This is hopefully the first of many research papers I plan on reading and taking notes on. I'm doing this for a few reasons:
* I want to get better at reading research papers
* I need to familiarize myself with the literature in my field
* I want to explore ideas outside of my field to see what interests me
* I think its important to take notes on the papers you read to help understanding
* I need to increase my writing ability and this is a great way to do so!

___

## **The Paper**

[The University of Florida Sparse Matrix Collection Paper](https://dl.acm.org/doi/10.1145/2049662.2049663)

[The Suite Sparse Matrix Collection Website](https://sparse.tamu.edu/)

## **Notes**

### Sparse Matrix Definition

The first thing that caught my attention was the definition of a sparse matrix. With that definition being that a sparse matrix is one that can be taken advantage of in some way in terms of its sparsity. This definition is as the paper puts it, an economic definition. 

I thought this was an interesting way to look at it and seemed somewhat non-math when most definitions for something like this would be like "any matrix with more zeros than nonzeros".

That isn't to say I don't like the definition, I think it actually gets right to the heart of what a sparse matrix is. Because if a matrix gained no benefit from its sparsity it might as well be dense so this economic definition really does seem to fit the concept.

___

### Motivation

At the highest level the paper points out that there is abosolutely a need for sparse matrices to at least test algorithms on and do benchmarking. But this raises the question, why not random ones? The paper does a good job showing why this is a bad idea usually, even if maintaining a real world dataset is costly, difficult, and time consuming. 

The paper points out that random matrices have inheritent differences compared to real world data that causes bais. This is becaues there is structure to the matrices in the real world that allow for operations like direct factorization to be less costly. Without this inheritent structure these algorithms diminish quickly in quality and baises towards random matrices that have specific qualities.

Specifically there is catastrophic fill-in for direct factorization using random matrices that has cubed time complexity and squared memory to factorize. This is great motivation for a real world dataset and at least knowing this will help me talk about the data I get from testing on random matrices. I do wish that they spent more time discussing how random matrices differ from real world ones in testing algorithms or even talked more about the process of creating a random matrix.

___

### Data

Finally the paper goes into some details about the dataset as a whole. There a few interesting patterns pointed out but the one I found most interesting was the size. While obvious to a degree it's still interesting to see the data show how much bigger matrices and data in general get over time as demands and technology expand. 

## **Questions**

1. Can you generate psuedo-random matrices that have structure similar to that of a particular problem? It seems like a solvable problem that might have use for those wanting to test on specific types of data. Such as designing an algorithm to work with genetic data, having something that could generate reandom genetic datasets with similar structure to real world ones could be useful. I'll need to look into this and see if genetic data specifically has enough real world matrices within easy access to make this solution obsolete.

2. As data gets bigger with time its doubtful that they change at the same rate so as they seperate whats going to change? I'd imagine data sizes will outpace hardware (and it seems like mostly already are) so in that case what is going to be the savings to work with lager data? New algorithms that are faster? Better software to use larger numbers without overflow? Distributed systems, GPUs, quantum computing? This is less a question and more of a wonder as to where will we see the largest gains when working with larger and larger data over time.