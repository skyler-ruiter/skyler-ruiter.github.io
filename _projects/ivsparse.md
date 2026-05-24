---
layout: page
title: IVSparse
description: A C++ sparse matrix library optimized for compression of highly redundant sparse data.
img: assets/img/projects/ivsparse_fig1.PNG
importance: 2
category: research
related_publications: true
---

**IVSparse** is a C++ sparse matrix library that introduces novel compression formats for sparse matrices where non-zero values are highly redundant — a common property in single-cell omics and other datasets from machine learning, data science, and scientific computing.

The library provides three storage formats:

- **CSC** — standard Compressed Sparse Column format
- **VCSC** (Value Compressed Sparse Column) — stores unique values and their column indices, achieving ~2.25× compression over CSC
- **IVCSC** (Indexed Value Compressed Sparse Column) — further compresses index storage via positive-delta encoding and bytepacking, achieving ~7.5× compression over CSC

The full paper was published at IEEE BigData '24. The work was also accepted as a one-page summary and poster at the **2024 Data Compression Conference (DCC)**, where we presented alongside researchers from across the compression community.

{% cite wolfgang2024vcsc %}

**Links:** [GitHub](https://github.com/Seth-Wolfgang/IVSparse) &nbsp;|&nbsp; [arXiv](https://arxiv.org/abs/2309.04355)

---



<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/ivsparse_fig1.PNG" title="Visualizing the IVSparse compression formats" class="img-fluid rounded z-depth-1 bg-white p-2" %}
  </div>
</div>

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/plot.png" title="Compression format size comparison" class="img-fluid rounded z-depth-1 bg-white p-2" %}
  </div>
</div>
<div class="caption">Sizes in GB of a large random matrix across different compression formats.</div>

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/DCC_poster.jpg" title="IVSparse at DCC 2024" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">Seth Wolfgang (right) and me (left) presenting IVSparse at the 2024 Data Compression Conference (DCC).</div>

---

## Talk

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <div class="embed-responsive embed-responsive-16by9 rounded z-depth-1">
      <iframe class="embed-responsive-item"
        src="https://www.youtube.com/embed/Szl82L0Nlho"
        title="Presentation on IVSparse and the VCSC/IVCSC formats"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen>
      </iframe>
    </div>
  </div>
</div>
<div class="caption">Presentation on IVSparse and the VCSC/IVCSC formats.</div>

