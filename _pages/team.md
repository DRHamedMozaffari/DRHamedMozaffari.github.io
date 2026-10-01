---
title: "Team"
layout: page
permalink: /team/
---

# Team

**Interested in collaborating with us?** <a href="{{ '/#contact' | relative_url }}">Contact Us</a>.

{% comment %}
  Every person on this page comes from a file in the _people/ folder.
  Add a file there and the person appears here with their own page at
  /team/<file-name>/. Copy _people/_TEMPLATE.md to start a new one.
{% endcomment %}

{% comment %}
  Which section a person appears in is set by `group:` in their file:
    group: management -> next to the PI
    group: staff      -> Team Members
    group: students   -> Team Members  (also the default if `group` is missing)
  The PI is the one file with `pi: true`.
{% endcomment %}

{% assign pi_person = site.people | where: "pi", true | first %}
{% assign management = site.people | where: "group", "management" | sort: "order" %}
{% assign staff = site.people | where: "group", "staff" | sort: "order" %}
{% assign students = site.people | where_exp: "p", "p.pi != true and p.group != 'staff' and p.group != 'management'" | sort: "order" %}

## PI

<div class="team-grid team-grid-rich" markdown="0">
{% if pi_person %}{% include team_card.html member=pi_person %}{% endif %}
{% for member in management %}{% include team_card.html member=member %}{% endfor %}
</div>

{% assign team_members = staff | concat: students %}
{% if team_members.size > 0 %}
## Team Members

<div class="team-grid team-grid-rich" markdown="0">
{% for member in team_members %}{% include team_card.html member=member %}{% endfor %}
</div>
{% endif %}

{% if site.data.alumni and site.data.alumni.size > 0 %}
## Alumni

<div class="section-card">
<table class="alumni-table">
<thead>
<tr><th>Name</th><th>Duration</th><th>Current Position</th></tr>
</thead>
<tbody>
{% for member in site.data.alumni %}
<tr>
<td>{{ member.name }}</td>
<td>{{ member.duration }}</td>
<td>{{ member.info }}</td>
</tr>
{% endfor %}
</tbody>
</table>
</div>
{% endif %}
