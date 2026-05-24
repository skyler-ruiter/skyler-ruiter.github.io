---
layout: page
title: FZGPUModules
description: GPU-accelerated graph-composable compression pipeline builder for analytical workflows.
img: assets/img/projects/rate-distortion.PNG
importance: 1
category: research
related_publications: true
---

**FZGPUModules** is a CUDA C++ library for building high-throughput scientific data compression pipelines entirely on the GPU. Rather than committing to a fixed compression algorithm, the library exposes a modular directed acyclic graph (DAG) pipeline builder: stages (predictors, quantizers, coders, shufflers, transforms) are connected by the user at runtime, and the pipeline executes the full compress/decompress chain on-device with stream-ordered memory management.

Key features:

- Composable pipelines — mix and match stages including Lorenzo predictors, quantizers (`ABS/REL/NOA` error modes), Huffman entropy coding, ANS/rANS coding, run-length encoding, bitshuffle, recursive zero elimination, zigzag and negabinary transforms, and more
- CUDA Graph capture — compress passes can be captured as CUDA Graphs and replayed with near-zero CPU overhead, critical for latency-sensitive or repeatedly-invoked workflows
- Smart memory management — two strategies: MINIMAL (allocate on demand, lowest peak GPU memory) and PREALLOCATE (all buffers at finalize time, enables buffer coloring to alias non-overlapping allocations)
- Self-describing file format — compressed `.fzm` files embed full stage configuration and CRC32 checksums; pipelines can be reconstructed from a file without any external config
- CLI tool — `fzgmod-cli` supports stage chains via `--stages "lorenzo->bitshuffle->rze"` or `TOML` preset configs, with profiling, bounds checking, and comparison reporting built in

**FZGPUModules** was developed as part of research into heterogeneous computing frameworks for scientific data compression. It was published at the SC '25 Workshops (International Conference for High Performance Computing, Networking, Storage and Analysis) and builds on prior work from the cuSZ (Argonne National Laboratory) and LC framework (Texas State University) libraries.

Tech stack: CUDA, C++17, CMake — requires CUDA 11.2+

{% cite ruiter2025fzmodules %}

**Links:** [GitHub](https://github.com/szcompressor/FZGPUModules) &nbsp;|&nbsp; [arXiv](https://arxiv.org/abs/2509.20563) &nbsp;|&nbsp; [FZ Website](https://fzframework.org/)

---

## FZ Team Photos

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/VT_Fall25_ZF_FZ_Group_Photo.png" title="FZ ZF Joint Workshop at Washington DC" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">FZ/ZF Joint Workshop, Washington DC. I'm pictured back middle left.</div>

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/sarasota_group_picture.png" title="FZ ZF Joint Workshop at Sarasota FL" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">FZ/ZF Joint Workshop, Sarasota FL. I'm pictured top right.</div>

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/song_research_group.jpg" title="Dr. Song's research group" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">Dr. Song's research group out for dinner.</div>
