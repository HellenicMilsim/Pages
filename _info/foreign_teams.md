---
title: Foreign Teams
date: 2017-07-24 21:00:00
categories: events
author: rath
excerpt: "Wanna play with us? You've come to the right place!"
header:
    overlay_color: "#000"
    overlay_filter: "0.5"
    overlay_image: /assets/img/headers/teams-header.jpeg
---

This page is for teams looking for a joint Co-Op or TvT session. If you'd like
to play with another team, and don't mind greek accents, we'd basically love to hear
from you.

The easiest way to reach us is coming to our TeamSpeak at `hms-community.teamspeak3.com`
and say hi, but you can also register at our [forum]({{ site.forum }}) and leave a message there.

# Timezone

Our timezone is Europe/Athens GMT +3 hours

# Server

So far we've hosted all joint sessions, since our Intel i7-4770 server seems to
handle it very well: [Hetzner Rootserver EX-40][server-specs]

# Mods

We use a small subset of our regular modset when playing with other teams.
These are:

* ACE
* CBA
* TaskForceRadio
* Most of RHS
* Most CUP maps

These are all well-known mods that almost all communities use, and a good
starting point to the mods we'll end up using for our joint event.

# Gameplay

* No respawn (permadeath)
* First person enforced
* TFAR enforced
* No crosshairs
* Basic medical model (ACE3) - epinephrine usable by all 

# Teams

These are the teams we've played with in the past, in roughly chronological order.
([JSON source][teams-json])

[server-specs]: https://www.hetzner.com/dedicated-rootserver/ex40?country=gb
[teams-json]: https://github.com/HellenicMilsim/Pages/blob/master/_data/teams.json


{% for team in site.data.teams %}
	{% if team.name == '' %}
		{% continue %}
	{% endif %}
<div class="team">
<h3>{{ team.name }}</h3>

<p>
<img src="{{ site.baseurl }}/assets/img/flags/small/{{ team.country }}.png" alt="{{ team.country }}"> <i>{{ team.country  | upcase }}</i>
</p>

{% if team.logo.size > 0 %}
<img src="{{ team.logo }}" alt="team logo" class="align-right" style="height:200px">
{% endif %}


{% if team.links.url %}
<p>
<i class="fa fa-globe" aria-hidden="true"></i> <a href="{{ team.links.url }}">Website</a>
</p>
{% endif %}


{% if team.links.steam %}
<p>
<i class="fa fa-steam-square" aria-hidden="true"></i> <a href="{{ team.links.steam }}">Steam Group</a>
</p>
{% endif %}


{% if team.links.youtube %}
<p>
<i class="fa fa-youtube" aria-hidden="true"></i> <a href="{{ team.links.youtube }}">Youtube Channel</a>
</p>
{% endif %}


{% if team.links.facebook %}
<p>
<i class="fa fa-facebook" aria-hidden="true"></i> <a href="{{ team.links.facebook }}">Facebook Page</a>
</p>
{% endif %}


</div>
<div style="clear:both"></div>
{% endfor %}
