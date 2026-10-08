---
permalink: /
title: "Beicheng Xu (徐贝澄)"
excerpt: "Ph.D. student at Peking University working on automated research, AutoML, and AI for systems."
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a Ph.D. student in Computer Science and Technology at the **School of Computer Science, Peking University**, advised by **[Prof. Bin Cui](https://cuibinpku.github.io/)** (IEEE Fellow). Before joining Peking University in September 2023, I received my bachelor's degree in Computer Science and Technology from **Wuhan University**, where I graduated **1st out of 319** students in my major.

My research focuses on **automated research**, where I develop intelligent agents to automate literature review, idea generation, experimentation, and scientific writing. A key part of this work is **automated machine learning (AutoML)**: combining large language models with Bayesian optimization to automate feature engineering, algorithm selection, hyperparameter tuning, and model ensembling. I also work on **AI for systems**, using AI-driven optimization to improve the performance and efficiency of traditional systems such as databases, as well as LLM systems.

I lead **AutoSci**, an automated research system spanning literature review, ideation, experimentation, and writing, and **[Openbox](https://github.com/PKU-DAIR/open-box)**, a general-purpose black-box optimization system. My industry collaborations include Tencent, Huawei, and PetroChina.

Contact: [beichengxu@stu.pku.edu.cn](mailto:beichengxu@stu.pku.edu.cn).

## Research Interests

- **Automated Research and Agents:** end-to-end research workflows, from literature review and research ideas to experiments and scientific writing.
- **AutoML:** LLM-guided optimization, feature engineering, combined algorithm selection and hyperparameter optimization (CASH), and model ensembling.
- **AI for Systems:** multi-fidelity optimization, transfer learning, and online configuration tuning under dynamic workloads.

## Selected Publications

{% assign selected_papers = site.publications | where: "selected", true | sort: "order" %}
{% assign research_areas = 'AutoResearch/AutoML|AI for System' | split: '|' %}
{% for research_area in research_areas %}
{% assign area_papers = selected_papers | where: "research_area", research_area %}
{% if area_papers.size > 0 %}

<h3 class="publication-group-title{% if research_area == 'AI for System' %} publication-group-title--systems{% endif %}">{{ research_area }}</h3>

{% for paper in area_papers %}
{% include publication.html paper=paper heading_level=4 %}
{% endfor %}
{% endif %}
{% endfor %}

[All publications]({{ '/publications/' | relative_url }})

## Education

{% for entry in site.data.cv.education %}
### {{ entry.institution }}

**{{ entry.degree }}**, {{ entry.school }}<br>
{{ entry.period }}<br>
{{ entry.detail }}

{% endfor %}

## Selected Honors

- **National Scholarship**, 2020-2021 and 2021-2022.
- **CCF Outstanding Undergraduate Award**, 2022 (102 recipients nationwide).
- **BYD Scholarship, Peking University**, 2025-2026.
- **Outstanding Graduate** and **Outstanding Bachelor's Thesis**, Wuhan University.

[Full CV and experience]({{ '/cv/' | relative_url }})
