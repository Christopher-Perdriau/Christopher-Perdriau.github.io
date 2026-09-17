---
title: "Research & Publications"
permalink: /publications/
excerpt: "Research narrative and full publication list."
---

My vision is to redefine who technology is built for by centering people with disabilities in CS education and technological design. I grew up in the Deaf community with Deaf parents, which motivates and positions me well to work with and for individuals from the Deaf community. My research draws attention to inaccessible teaching practices for Deaf students and the harmful effects of microaggressions that discount students' success, and offers concrete strategies for addressing both.

My current work investigates Deaf students' experiences with common "evidence-based" active-learning practices in CS — particularly live coding, where instructors write and explain code in real time. These methods are widely promoted in CS education, but my results show they often create accessibility barriers that force Deaf students to divide their attention between an instructor, an ASL interpreter, notes, and the live-coding example, causing them to miss material. Based on recommendations from Deaf students themselves, my research offers low-cost teaching practices that improve accessibility — for example, instructors sharing code examples with Deaf students before class. Separately, earlier work of mine found that CS students from historically underrepresented groups report peers attributing their success to "special treatment" rather than competence. Following up on that qualitative finding with a survey of 4,327 undergraduate CS majors across 221 institutions, I found this perception is significantly linked to lower self-efficacy, sense of belonging, and intent to persist in CS — and that women, Black, and/or Asian students report hearing it significantly more often than their male and white peers.

Beyond this, I've collaborated with faculty across institutions to design accessible technology directly: interviewing Deaf students about their experiences with large language models to inform guidelines for how LLMs should respond to Deaf users, and co-designing a framework for translating music into haptics and supporting visuals for Deaf audiences.

Going forward, I plan to pursue three lines of research: (1) evaluating accessible, student-informed teaching practices in CS classrooms; (2) identifying the needs of and barriers faced by faculty adopting accessible pedagogy; and (3) participatory design of AI systems with Deaf people. The third line includes a planned audit of AI-driven hiring and résumé-screening platforms for bias against signals of Deaf identity — ASL fluency, Deaf schools, Deaf community involvement — extending my accessibility research directly into the domain of algorithmic hiring decisions.

I also have a standing thread of work on AI itself, spanning explainability, education, and accessible design. In 2020, I helped adapt the U.S. Army's After-Action Review process into AAR/AI, a structured method for helping people assess reinforcement-learning agents' decisions in a qualitative study. In 2023, I studied how CS undergraduates form — often inaccurate — perceptions of AI and cybersecurity as career specializations, and how those perceptions may discourage students from underrepresented groups from pursuing either field. Most recently, I've helped design and evaluate LLM-powered AI tutors with personas for Deaf and Hard-of-Hearing learners, studying how DHH students evaluate an AI system's cultural knowledge and community position.

---

## Published / Accepted

{% assign pubs = site.data.publications.published | sort: 'year' | reverse %}
{% assign years = pubs | map: 'year' | uniq | sort | reverse %}

**Jump to year:** {% for y in years %}[{{ y }}](#{{ y }}){% unless forloop.last %} &middot; {% endunless %}{% endfor %}
{: .notice--light}

{% for y in years %}
### {{ y }}
{: id="{{ y }}"}

{% assign year_pubs = pubs | where: 'year', y %}
{% for pub in year_pubs %}
- **{{ pub.title }}**{% if pub.note %} — *{{ pub.note }}*{% endif %}{% if pub.url %} &middot; [DOI]({{ pub.url }}){% endif %}
  <br>{{ pub.authors }}. {{ pub.venue }}.
{% endfor %}
{% endfor %}

## Under Review

*Spot-check against [Google Scholar](https://scholar.google.com/citations?user=-cDZEO8AAAAJ&hl=en) before treating as current — these may have since been accepted.*

{% for pub in site.data.publications.under_review %}
- **{{ pub.title }}**
  <br>{{ pub.authors }}. {{ pub.venue }}.
{% endfor %}

## Presentations & Invited Talks

{% assign talks = site.data.publications.presentations | sort: 'year' | reverse %}
{% for pub in talks %}
- **{{ pub.title }}** ({{ pub.year }})
  <br>{{ pub.authors }}. {{ pub.venue }}.
{% endfor %}
