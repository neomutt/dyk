---
layout: concertina
title: Did You Know?
---
# {{ page.title }}
Here you will find curated collection of handy and useful tips to help increase your productivity and efficiency with NeoMutt.
## Tips



{% assign sorted = site.dyk | sort: 'url' | reverse %}

| Number | Date | Title | Description |
| :----- | :--- | :---- | :---------- |
{% for f in sorted %}{% assign parts = f.url | split: '/' %}[{{ parts[2] }}]({{ f.url }})|[{{ f.date | slice: 0,10 }}]({{ f.url }})|[{{f.title}}]({{ f.url }})|[{{ f.description }}]({{ f.url }})
{% endfor %}

