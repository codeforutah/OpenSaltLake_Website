---
  status: publish
  layout: default
---

# The Team

<div class="team flex flex--around center">
{% for person in site.data.team.team %}
  <div class="team__member">
    <span class="team__name">{{ person.name }}</span>
    <span class="team__skills">{{ person.skills }}</span>
    {% if person.about %}
    <p class="team__about">
        {{ person.about }}
    </p>
    {% endif %}
    <div class="flex flex--around center">
    {% for social in person.social %}
      <a href="{{ social.url }}">{{ social.label }}</a>
    {% endfor %}
    </div>
  </div>
{% endfor %}
</div>
