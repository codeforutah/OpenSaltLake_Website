---
  status: publish
  layout: default
---
<section markdown="1">
# The Team

<div class="team flex flex--around flex--wrap center">
{% for person in site.data.team.team %}
  <article class="team__member flex flex__column">
    <img src="photos/{{ person.name | remove: " " }}.png" class="team__photo" alt="{{ person.name }}" />
    <p class="team__skill">{{ person.skills }}</p>
    <h1 class="team__name">{{ person.name }}</h1>
    {% if person.about %}
    <p class="team__bio">
    {{ person.about }}
    </p>
    {% endif %}
    <div class="team__social flex flex--around center">
    {% for social in person.social %}
      <a href="{{ social.url }}">{{ social.label }}</a>
    {% endfor %}
    </div>
  </article>
{% endfor %}
</div>
</section>
