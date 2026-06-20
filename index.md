---
layout: single
author_profile: true
classes: wide
permalink: /
---

<section id="about" markdown="1">

# Rolando Miranda

**Mechanical engineer · MS candidate at NYU Tandon**

I'm a mechanical engineer with four years of experience in Class III medical device manufacturing, now studying robotics and material science at NYU Tandon. I like problems where mechanical design, electronics, and control all have to work together — process validation lines, robotics, instrumentation and automation.

### What I'm working on now

I am currently working as a Graduate Research Assistant at BuiLab, where I lead the efforts for making a fully automatic electrochemical reactor that utilizes minimal human input. This requires knowledge of communication protocols, electronics, mechanical design for fluid handling and additive manufacturing.

### Background

I started my career at an energy consulting firm, assessing the safety of high-pressure steam vessels and designing boiler installations and fuel systems. After that experience, I transitioned into medical device manufacturing. I started as an intern learning the regulatory guidelines and the complex, highly technical processes required to build a Class III implantable device. Not long after, I was promoted into a Manufacturing Engineer role in the Access Devices division of the company. During the initial months of this role, I delivered a product-line flexibility project needed to absorb forecasted changes in demand. After this, many other business-critical projects came my way: from ramping up rolled-throughput yield on newly transferred lines to match sending-site levels, to managing the testing, reporting, and closure of raw-material changes for neurosurgery access devices.

In my final years at the company, my work centered on leading evidence-based investigations of non-conformances, exceeding yearly line efficiency targets by more than 10%, and collaborating with R&D and Regulatory Affairs to deliver and execute validation plans for device design changes. I then moved to NYU Tandon as a Graduate Course Assistant, designing and building test instrumentation for the Thermo-fluids Laboratory, writing practicum procedures, and supporting undergraduate students in the lab.

### What I'm interested in

My work has consistently sat at the intersection of mechanical design, instrumentation, and control — whether that's validating manufacturing processes for implantable devices, building test equipment for a university lab, or designing control systems for robotics and mechatronic projects. I'm increasingly interested in how these same principles apply to automation and additive manufacturing, and I'm looking for opportunities to build deeper experience there.

</section>

<section id="projects" markdown="1">

## Projects

A selection of engineering work — coursework, professional case studies, and instrumentation built at NYU. Click any project for the full write-up.

<div class="project-grid">
  {% assign sorted_projects = site.projects | sort: 'date' | reverse %}
  {% for project in sorted_projects %}
    <a class="project-card" href="{{ project.url | relative_url }}">
      <div class="project-card__image">
        {% if project.header.teaser %}
          <img src="{{ project.header.teaser | relative_url }}" alt="{{ project.title }}">
        {% endif %}
      </div>
      <div class="project-card__body">
        <h3 class="project-card__title">{{ project.title }}</h3>
        {% if project.excerpt %}
          <p class="project-card__excerpt">{{ project.excerpt }}</p>
        {% endif %}
      </div>
    </a>
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
