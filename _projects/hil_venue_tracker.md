---
layout: page
title: HIL Venue Tracker
description: Lightweight Python tool for tracking HPC conference deadlines, generating visual timelines, text reports, and calendar exports for lab planning.
img: assets/img/projects/conference_timeline.png
importance: 1
category: work
related_publications: false
---

**HIL Venue Tracker** is a lightweight tool built for the [IU HPC Innovation Lab](https://github.com/IU-HPC) to help lab members stay on top of HPC conference submission deadlines and event dates throughout the year.

The tool ingests a structured list of venues and produces three outputs:

- **Visual timeline** — a Gantt-style chart showing abstract, paper, and notification deadlines alongside conference dates across the full year
- **Text reports** — human-readable summaries of upcoming deadlines sorted by urgency
- **Calendar export** — an `.ics` file that can be imported into any calendar app

Everything runs as a set of Python scripts with a GitHub Actions workflow that automatically regenerates outputs whenever the venue list is updated — no manual steps required for lab members who just want to check the current state.

**Links:** [GitHub](https://github.com/IU-HPC/HIL_Venue_Tracker)

---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/conference_timeline.png" title="HIL Venue Tracker conference timeline" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">Auto-generated conference timeline showing submission deadlines and event dates for HPC venues throughout the year.</div>
