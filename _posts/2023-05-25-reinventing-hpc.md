---
layout: post
title: "Reinventing HPC (Reed et al.) (2022)"
date: 2023-05-25 15:10:00
description: I'd be lying if I said I had a strong grasp on the landscape of HPC considering how new I am to looking into it. This paper seemed like a great place to start getting a handle on how the world of HPC has grown and changed over time and where it might be going in the future!
tags:
 - papers
---

I really enjoyed reading this paper. The reasoning was strong and easy to follow, even reading the paper a single time I felt like I had a good grasp on what the paper was trying to get across. I also gained a lot of new information that was new to me about HPC and the analysis of the landscape and predictions for next steps felt like they had strong reasoning as well and data to back it up.

___

## **The Paper**

[Reinventing High Performance Computing: Challeneges and Opportunities](https://arxiv.org/pdf/2203.02544.pdf)

## **Notes**

### Introduction

This paper is almost exactly a year old when I'm reading it today and it somehow feels like it was written yesterday. Obviously the paper is about HPC being at a crossroads with the individual factors effecting HPC all coming together to show us that change is needed to take the next step towards progress, as the title suggests. The actual thesis however I think provides a very clear and actionable direction given this complex interaction of factors, to a degree that even somebody like myself who is fairly new to the topic understands it. 

The paper also has this great graphic showing how they visualize the factors effecting HPC how they see it and it really brings together the ideas and visually shows well how they relate together to produce the prediction he has. 

![img]({{ '/assets/images/reinventingHPCfig1.PNG' | relative_url }}){: .center-image }

___

### History of HPC

What surpised me most was the number of HPC companies that have tried to exist throughout history. It doesn't seem like something that could be done by a company without the massive funding of a FAANG company but that could just be my younger perspective skewing my ability to understand early HPC endeavors. But the paper shows that there were a lot of them, the issue is that they never really ended up lasting long. Mostly due to fast changing technology and massive costs for such a small market.

This early history of bespoke systems fell away in favor of the HPC that I know more about, the cloud and AI led by the FAANG companies that run on x86, linux, and use a lot of GPUs and distributed systems.

The benefits of this change were widespread and easy to see watching all the startups and researchers using AWS and cloud infrastructure to compute on, with a close friend of mine even being able to write a paper about compute speeds and times between edge and cloud computing.

The other part of the history of HPC that grabbed my interest is the international politics that goes into developing these massive systems. That the US was proud of being number one on the TOP500 list only to be taken down a peg by the Japanese for a while, as well as how the Chinese are a growing player in the scene by mostly investing in their own technology, and finally the europeans getting into it as well with large expensive projects. It really shows how the absolute scale of these systems has changed over the years, with the largest systems needing more than most government agencies can fund.

This challenge from other countries in HPC also leads to an interesting comparison to the USA as it seems like the US based companies are the forward driver of change and reasearch while abroad it seems to be more governmentally and academically led. Seeing the differences in how having companies lead development spaces is going to be something to keep an eye on going forward for me.

___

### 6 Maxims

The paper outlines 6 maxims for moving forward in HPC to take the next steps.

1. Semiconductor constraints dictate new approaches.
2. End-to-end hardware and software co-design is essential.
3. Prototyping at scale is required to test new ideas.
4. The space of leading edge HPC applications is broader now than in the past.
5. Cloud economics have changed the supply chain ecosystem.
6. The societal implications of technical issues really matter.

___

### Conclusions

The paper suggests through the history and its maxims that future developments aren't in hardware as much any more. The "free lunch" of hardware gains is increasingly becoming less reliable and the limits of GPUs and distrubuted systems are also starting to appear while also being pressured by semiconductor production issues. 

The way to take HPC to the next stage is through somewhat of a return to old. By creating systems that are end-to-end designed, with a focus on large scale prototypes, and partnerships with industry to fuel development, HPC will be able to achieve even further gains not seen before. It's almost like the return to monolithic software development away from microprocesses. 

## **Questions**

1. The giant companies are a double edged sword, they are massive forces of change but like the paper pointed out, they have power not seen since oil tycoons. Should they be the ones leading the changes sought by this paper or should academics lead it, or maybe even the government? The end-to-end development works in places like Asia because of how their society operates differently to ours but it's difficult to imagine a force that isn't the FAANG companies having the influence to push for this kind of change. 

2. When last specific and more tailor made HPC systems were a reality, they were still small enough for be affordable for a number of companies and institutions to own them, but seeing the maxims and reading the paper leaves me wondering where non FAANG companies, reserchers, and academics are going to have a place to contribute to this new form of HPC system. 

3. Where will quantum computers fit into this puzzle? As another way to do computations some say they will revolutionize computing much like the GPU did, allowing for a completely new realm of computing to be done, will it revolutionize HPC the same way GPUs did?