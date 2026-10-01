---
title: "Home"
layout: homelay
permalink: /
---

{% assign pi_person = site.people | where: "pi", true | first %}
{% assign name_parts = site.lab_name | split: " " %}
{% assign name_first = name_parts | first %}
{% assign name_rest = site.lab_name | remove_first: name_first | strip %}

<section class="landing-hero" markdown="0">
<div class="hero-stage">
<img class="hero-art" src="{{ '/images/home/hero-orbit.svg' | relative_url }}" width="1240" height="790" alt="Our research areas — artificial intelligence, computer vision, remote sensing, robotics and automation, IoT and smart homes, green electrical energy, digital twins and BIM, cloud and data science, extended reality, and construction and infrastructure — arranged around the team name.">
<div class="hero-center">
<img class="hero-mark" src="{{ '/images/logo/team-mark.svg' | relative_url }}" width="64" height="64" alt="">
<h1 class="hero-name"><span class="hero-name-main">{{ name_first }}</span>{% if name_rest != "" %} <span class="hero-name-rest">{{ name_rest }}</span>{% endif %}</h1>
</div>
</div>
<p class="hero-lead">{{ site.lab_tagline }}</p>
<p class="hero-note">We are not selling anything — we are looking for collaboration.</p>
<div class="hero-actions">
<a class="land-btn land-btn-solid" href="{{ '/research/' | relative_url }}">Explore our research</a>
<a class="land-btn land-btn-ghost" href="#contact">Contact Us</a>
</div>
</section>

{% if site.lab_letters %}
<section class="land-section" aria-label="What our name stands for" markdown="0">
<p class="land-eyebrow">What our name stands for</p>
<div class="letters-row">
{% for l in site.lab_letters %}<div class="letter-card"><span class="letter-big">{{ l.letter }}</span><span class="letter-word">{{ l.word }}</span><span class="letter-detail">{{ l.detail }}</span></div>
{% endfor %}
</div>
</section>
{% endif %}

<section class="land-section" markdown="0">
<div class="mv-grid">
<div class="mv-card">
<p class="land-eyebrow">Our mission</p>
<p class="mv-text">To turn visual, spatial and sensor data into reliable knowledge for safer, smarter and greener buildings and infrastructure — by developing rigorous methods in artificial intelligence, sensing, robotics and digital twins, and sharing them openly with students, researchers and partners.</p>
</div>
<div class="mv-card mv-card-accent">
<p class="land-eyebrow">Our vision</p>
<p class="mv-text">A built environment that can sense, understand and improve itself — designed, built and maintained with intelligent, energy-efficient and trustworthy technology that grows out of open collaboration.</p>
</div>
</div>
</section>

<section class="land-section" markdown="0">
<p class="land-eyebrow">Artificial intelligence</p>
<h2 class="land-title">From data to understanding.</h2>
<p class="land-sub">Large language models read reports and documents, vision-language models interpret images and scans, and learned models turn sensor signals into decisions — for the buildings and infrastructure around us.</p>
<figure class="land-figure">
<img src="{{ '/images/home/ai-concept.svg' | relative_url }}" width="1200" height="520" loading="lazy" alt="Illustration: reports, images and sensor data flow through a neural network and become a digital model of a building under construction, with sensors, a drone and a detected defect.">
</figure>
</section>

<section class="land-section" markdown="0">
<p class="land-eyebrow">Our research, connected</p>
<h2 class="land-title">One program, from sensing to impact.</h2>
<p class="land-sub">Each topic feeds the next: we capture the built environment, connect the data, understand it with AI, act on it, and apply the results where they matter.</p>
<div class="research-map">
<div class="map-stage">
<div class="map-head"><svg class="map-icon" viewBox="0 0 24 24" aria-hidden="true"><g transform="rotate(-35 12 10)"><rect x="9.6" y="6.5" width="4.8" height="7" rx="1"/><rect x="1.5" y="7.5" width="6.5" height="5" rx=".6"/><rect x="16" y="7.5" width="6.5" height="5" rx=".6"/><path d="M8 10h1.6M14.4 10H16M4.75 7.5v5M19.25 7.5v5M12 13.5v2.2M10 16.6a2.8 2.8 0 0 0 4 0" stroke-width="1.3"/></g><path d="M3 21.5a5 5 0 0 1 4.5-4.5M3 18.3a2 2 0 0 1 1.5-1.5" stroke-width="1.3"/></svg><span class="map-num">01</span></div>
<h3 class="map-title">Sense</h3>
<ul class="map-list"><li><span class="map-item">Remote sensing</span><span class="map-subs"><span>Satellite imaging</span><span>Microscopy</span><span>LiDAR scanning</span><span>Thermography</span><span>Scan2BIM</span></span></li></ul>
</div>
<div class="map-stage">
<div class="map-head"><svg class="map-icon" viewBox="0 0 24 24" aria-hidden="true"><path d="M3 11.5L12 4l9 7.5V21H3z"/><path d="M8.3 15.3a5.2 5.2 0 0 1 7.4 0M10.2 17.4a2.4 2.4 0 0 1 3.6 0"/><circle cx="12" cy="19.2" r=".6" fill="currentColor"/></svg><span class="map-num">02</span></div>
<h3 class="map-title">Connect</h3>
<ul class="map-list"><li><span class="map-item">IoT, IIoT, AIoT &amp; smart homes</span></li><li><span class="map-item">Cloud computing</span></li><li><span class="map-item">Data science &amp; analysis</span></li></ul>
</div>
<div class="map-stage">
<div class="map-head"><svg class="map-icon" viewBox="0 0 24 24" aria-hidden="true"><rect x="5" y="5" width="14" height="14" rx="2.5"/><path d="M9 2v3M15 2v3M9 19v3M15 19v3M2 9h3M2 15h3M19 9h3M19 15h3"/><path d="M8.6 15.2l1.9-6.4h1l1.9 6.4M9.2 13.2h3.6M15.3 8.8v6.4" stroke-width="1.4"/></svg><span class="map-num">03</span></div>
<h3 class="map-title">Understand</h3>
<ul class="map-list"><li><span class="map-item">Artificial intelligence</span><span class="map-subs"><span>LLMs</span><span>VLMs</span><span>Applications</span></span></li><li><span class="map-item">Computer vision</span></li></ul>
</div>
<div class="map-stage">
<div class="map-head"><svg class="map-icon" viewBox="0 0 24 24" aria-hidden="true"><path d="M12 2.5l8.5 4.8v9.4L12 21.5l-8.5-4.8V7.3z"/><path d="M3.5 7.3L12 12l8.5-4.7M12 12v9.5"/><path d="M7.7 9.6v9.5M16.3 9.6v9.5M3.5 12l8.5 4.7 8.5-4.7" stroke-width="1" stroke-dasharray="1.6 1.6"/></svg><span class="map-num">04</span></div>
<h3 class="map-title">Act &amp; model</h3>
<ul class="map-list"><li><span class="map-item">Robotics &amp; automation</span></li><li><span class="map-item">Green electrical energy</span></li><li><span class="map-item">Digital twins &amp; BIM</span></li><li><span class="map-item">Extended reality (XR)</span></li></ul>
</div>
<div class="map-stage">
<div class="map-head"><svg class="map-icon" viewBox="0 0 24 24" aria-hidden="true"><path d="M5 21V3.5h14.5"/><path d="M5 7l3.5-3.5M8.5 3.5V7M12 3.5L8.5 7"/><path d="M17.5 3.5v4"/><rect x="15.7" y="7.5" width="3.6" height="3" rx=".5"/><path d="M3 21h18"/><path d="M11 21v-6h7v6M13.3 17.3h2.4" stroke-width="1.4"/></svg><span class="map-num">05</span></div>
<h3 class="map-title">Apply</h3>
<ul class="map-list"><li><span class="map-item">Construction</span></li><li><span class="map-item">Infrastructure</span></li><li><span class="map-item">Foundational research</span></li><li><span class="map-item">MOC</span></li><li><span class="map-item">QA/QC</span></li><li><span class="map-item">KPI</span></li><li><span class="map-item">Data pipelines</span></li><li><span class="map-item">Monitoring &amp; detection</span></li></ul>
</div>
</div>
<p class="land-more"><a href="{{ '/research/' | relative_url }}">Explore our research areas &rarr;</a></p>
</section>

{% capture selected %}{% bibliography --query @*[selected=true] %}{% endcapture %}
{% if selected contains "pub-entry" %}
<section class="land-section" markdown="0">
<p class="land-eyebrow">Selected publications</p>
<h2 class="land-title">Work we are proud of.</h2>
<div class="section-card selected-pubs">
{{ selected }}
<p style="margin: var(--space-4) 0 0;"><a href="{{ '/publications/' | relative_url }}">All publications &rarr;</a></p>
</div>
</section>
{% endif %}

<section class="land-section land-contact" id="contact" markdown="0">
<p class="land-eyebrow">Contact Us</p>
<h2 class="land-title">Let&rsquo;s work together.</h2>
<p class="land-sub">We are not offering products or services — we are looking for collaborators. If you are a researcher, student or partner whose work connects with any of these areas, we would be glad to hear from you.</p>
<div class="hero-actions">
<a class="land-btn land-btn-solid" href="{{ '/team/' | relative_url }}">Meet the team</a>
{% if pi_person %}<a class="land-btn land-btn-ghost" href="{{ pi_person.url | relative_url }}">Contact {{ site.name }}</a>{% endif %}
</div>
</section>

<section class="land-disclaimer" id="disclaimer" markdown="0">
<h2 class="disclaimer-title">Disclaimer</h2>
<p>This website is a non-commercial profile and portfolio maintained by its team members. It describes our own research interests and published work and is shared to open opportunities for collaboration and to make our work easy to find and cite — especially for students.</p>
<p>Nothing on this site is expert or professional advice. We do not represent, and do not speak for, the National Research Council Canada (NRC), the University of Toronto, Carleton University, or any other organization; any views expressed are our own. Some text and images on this site were prepared with the help of AI tools.</p>
</section>
