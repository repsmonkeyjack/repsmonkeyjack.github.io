---
layout: home
---
<img src="img/name.png" alt="Monkey Jack header">

<div class="monkeybox">
<img src="img/mj1.png" alt="Monkey Jack" style="max-height: 140px; float: left; margin-right: 1em;">
The Representatives of Monkey Jack are a four-piece alternative rock outfit from
Bonn, Germany with influences ranging from pop to metal, classical, jazz, and
folk. Their songs feature human narratives flickering between reminiscing and
brooding that emerge in a wide tonal spectrum from gentle, thoughtful, acoustic
passages to errant, merciless, head-banging breakdowns.
</div>

<div class="monkeybox">
    <h2>Events</h2>

    <ul>
    {% for show in site.data.shows %}
    <li>
        {{ show.date }} -
        {% if show.event %}
        {{ show.event }} (at {{ show.venue }})
        {% else %}
        {{ show.venue }}
        {% endif %}
    </li>
    {% endfor %}
    </ul>

</div>

<div class="monkeybox">
<h2>Songs</h2>

<ul>
{% for song in site.pages %}
{% if song.url contains "songs" %}
<li>
    <a href="{{ song.url }}">
        <img src="{{ song.image }}" style="max-height: 80px;" />
        {{ song.title }}
    </a>
</li>
{% endif %}
{% endfor %}
</ul>
</div>