---
layout: page
title: Research
permalink: /research/
---

## Research Interests

---

I am a researcher in the field of high performance computing with a focus on data compression and sparse matrix storage. My research interests include: HPC, data compression, sparse matrix storage, sparse algorithms, CUDA programming, and performance portability. I am currently working on the development of high performance compression algorithms for the FZ Project and the IVSparse Library. I have also had experience as an undergraduate research intern at Sandia National Laboratories working on the E3SM atmospheric model, HOMME (High-Order Method Modeling Environment).

## Projects

---

### **FZ**

The FZ Project is a lossy error-bound lossy compression framework funded by the NSF. These compressors see use in many fields such as AI, quantum simulation, scientific computing, and instrumentation.

I am currently working on the development team of the IU FZ Team under the advisement of Dr. Fengguang Song. Thus far I've developed the FZModules library, a modular framework for constructing bespoke lossy compression pipelines. FZModules is designed for use by domain scientists and compression researchers to develop compression pipelines for specific applications.

[**FZModules Github**](https://github.com/szcompressor/FZModules){:target="_blank"}

[**FZModules Publication**](https://arxiv.org/abs/2509.20563){:target="_blank"}

<div style="width: 75%; margin: auto;">
  <figure>
    <img src="/assets/images/rate-distortion.PNG" style="width: 100%;">
    <figcaption><i>Rate distortion curves for different compression pipelines highlighted in the paper.</i></figcaption>
  </figure>
</div>

[**cuSZ Github**](https://github.com/szcompressor/cuSZ){:target="_blank"}

[**FZ Website**](https://fzframework.org/){:target="_blank"}

### **IVSparse** *(Primary Co-Contributor)*

The IVSparse Library is a C++ sparse matrix library optimized for the compression of sparse data in cases where non-zero values are highly redundant. IVSparse supports three main compression formats.

* *CSC: Compressed Sparse Column* - The standard sparse matrix format that stores the column indices of non-zero values and the values themselves.
* *VCSC: Value Compressed Sparse Column* - A format that takes advantage of the redundancy in the values of the matrix by storing unique values and their counts.
  * ~2.25x fold compression over CSC (for redundant data)
* *IVCSC: Indexed Value Compressed Sparse Column* - A format that further compresses the index storage of VCSC by using positive-delta encoding and then bytepacking indices for each unique value in a column.
  * ~7.5x fold compression over CSC (for redundant data)

<div style="width: 75%; margin: auto;">
  <figure>
    <img src="/assets/images/plot.png" style="width: 100%;">
    <figcaption><i>Sizes in GB of a random large matrix for different compression formats.</i></figcaption>
  </figure>
</div>

[**IVSparse Github**](https://github.com/Seth-Wolfgang/IVSparse){:target="_blank"}

[**BigData '24 Slides**](https://docs.google.com/presentation/d/1ocnvkoDkL5g7JaSQU9OD0dAvf65k8Nma/edit?usp=sharing&ouid=109836778326859038082&rtpof=true&sd=true){:target="_blank"}

## Publications

---

- **[SC Workshops '25 (DRBSD)]** **Skyler Ruiter**, Jiannan Tian, Fengguang Song. "FZModules: A Heterogenous Computing Framework for Customizable Data Compression Pipelines." *2025 IEEE/ACM The 11th International Workshop on Data Analysis and Reduction for Big Scientific Data (DRBSD)*. St Louis, MO, USA. November 16-21. [arxiv](https://arxiv.org/abs/2509.20563)

- **[BigData '24]** Seth Wolfgang, **Skyler Ruiter**, Marc Tunnell, Timothy Triche Jr, Erin Carrier, Zachary DeBruine. "Value-Compressed Sparse Column (VCSC): Sparse Matrix Storage for Single-cell Omics Data." *2024 IEEE International Conference on Big Data (BigData)*. Washington, DC, USA. December 15-18. [arxiv](https://arxiv.org/abs/2309.04355)


## Talks and Pictures

---

<figure>
  <img src="/assets/images/dongarra_pic_sc25.jpg" style="width: 100%;">
  <figcaption><i>SC25 Photo. Seth Wolfgang (left), Jack Dongarra (middle), Me (right).</i></figcaption>
</figure>

<figure>
  <img src="/assets/images/VT_Fall25_ZF_FZ_Group_Photo.png" style="width: 100%;">
  <figcaption><i>FZ ZF Joint Workshop at Washington DC. I'm pictured back middle left.</i></figcaption>
</figure>

<figure>
  <img src="/assets/images/song_research_group.jpg" style="width: 100%;">
  <figcaption><i>Dr. Song's research group out for dinner.</i></figcaption>
</figure>

<figure>
  <img src="/assets/images/sarasota_group_picture.png" style="width: 100%;">
  <figcaption><i>FZ ZF Joint Workshop at Sarasota FL. I'm pictured top right.</i></figcaption>
</figure>

<figure>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/Szl82L0Nlho" frameborder="0" allowfullscreen></iframe>
  <figcaption><i>GVSU Computing Seminar Series IVSparse Talk</i></figcaption>
</figure>

<figure>
  <img src="/assets/images/DCC_poster.jpg" style="width: 100%;">
  <figcaption><i>Seth Wolfgang (right) and I (left) preseting IVSparse at the 2024 Data Compression Conference (DCC).</i></figcaption>
</figure>

<figure>
  <img src="/assets/images/ssd2024.jpg" style="width: 100%;">
  <figcaption><i>Seth Wolfgang (right) and I (left) preseting IVSparse at the 2024 Winter GVSU Student Scholars Day to the university president.</i></figcaption>
</figure>

<figure>
  <img src="/assets/images/tech_week.jpg" style="width: 100%;">
  <figcaption><i>Seth Wolfgang (left) and I (right) preseting IVSparse at the 2024 Grand Rapids Tech Week.</i></figcaption>
</figure>