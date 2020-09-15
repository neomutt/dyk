---
layout: concertina
title: Did You Know?
---

# {{ page.title }}

## Tips

Introduction...

{% assign sorted = site.dyk | sort: 'url' | reverse %}

| Number | Date | Title | Description |
| :----- | :--- | :---- | :---------- |
{% for f in sorted %}{% assign parts = f.url | split: '/' %}[{{ parts[2] }}]({{ f.url }})|[{{ f.date | slice: 0,10 }}]({{ f.url }})|[{{f.title}}]({{ f.url }})|[{{ f.description }}]({{ f.url }})
{% endfor %}

