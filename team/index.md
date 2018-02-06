---
  status: publish
  layout: default
---

# The Team

<div class="team flex flex--around flex--wrap center">
{% for person in site.data.team.team %}
  <div class="team__member flex flex__column flex--between">
    {% if person.about %}
    <img src="photos/{{ person.name | remove: " " }}.png" class="team__photo" alt="{{ person.about }}" />
    {% else %}
    <img src="photos/{{ person.name | remove: " " }}.png" class="team__photo" />
    {% endif %}
    <div class="team__name">{{ person.name }}</div>
    <div class="team__social flex flex--around center">
    {% for social in person.social %}
      <a href="{{ social.url }}">{{ social.label }}</a>
    {% endfor %}
    </div>
  </div>
{% endfor %}
</div>
