---
layout: single
author_profile: true
classes: wide
permalink: /
---

<section id="about" markdown="1">

# Rolando Miranda

**Mechanical engineer · MS candidate at NYU Tandon**

*One- or two-sentence opening line — your elevator pitch.*

### What I'm working on now

*3-5 lines on current commitments: NYU coursework focus, TA role at Thermo-fluids Lab, current builds.*

### Background

*One or two paragraphs on the Terumo / MicroVention years. Outcome-focused.*

### What I'm interested in

*Short paragraph on the technical areas you want to work in.*

</section>

<section id="projects" markdown="1">

## Projects

A selection of engineering work — coursework, professional case studies, and instrumentation built at NYU. Click any project for the full write-up.

<div class="grid__wrapper">
  {% assign sorted_projects = site.projects | sort: 'date' | reverse %}
  {% for project in sorted_projects %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

</section>

<section id="cv" markdown="1">

## CV

My full CV covers education, work history, technical skills, methodologies, and languages.

<p>
  <a href="/assets/files/CV_RolandoMiranda.pdf" class="btn btn--primary" download>
    <i class="fas fa-download"></i> Download CV (PDF)
  </a>
</p>

*Last updated: [month year]*

</section>

<section id="contact" markdown="1">

## Contact

I'm open to conversations about R&D roles, research collaborations, and consulting in medical devices, mechatronics, and thermal engineering.

The best way to reach me is by [email](mailto:rolomiranda98@gmail.com). I'm also on [GitHub](https://github.com/rolando-miranda) and [LinkedIn](https://www.linkedin.com/in/).

</section>
