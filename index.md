---
layout: homepage
---

## About Me {#about-me}

{% assign current_year = site.time | date: '%Y' | plus: 0 %}
{% assign current_month = site.time | date: '%m' | plus: 0 %}
{% assign phd_start_year = site.data.info.phd_start_year | plus: 0 %}
{% assign year_diff = current_year | minus: phd_start_year %}

{% if current_month >= 9 %}
  {% assign academic_year = year_diff | plus: 1 %}
{% else %}
  {% assign academic_year = year_diff %}
{% endif %}

{% case academic_year %}
  {% when 1 %}
    {% assign year_string = "first-year" %}
  {% when 2 %}
    {% assign year_string = "second-year" %}
  {% when 3 %}
    {% assign year_string = "third-year" %}
  {% when 4 %}
    {% assign year_string = "fourth-year" %}
  {% when 5 %}
    {% assign year_string = "fifth-year" %}
  {% else %}
    {% assign year_string = "Ph.D." %}
{% endcase %}

Hi :D ! I'm a {{ year_string }} Ph.D. student at The Chinese University of Hong Kong, Shenzhen, advised by [Prof. Zhizheng Wu](https://drwuz.com/). I spent my undergraduate studies at Fudan University, majoring in software enginnering, with [Prof. Bihuan Chen](https://chenbihuan.github.io/) and [Prof. Kaifeng Huang](https://kaifeng-h.github.io/).

Beyond academia, I'm an amateur music producer with over 2 million plays on [netease cloud music](https://music.163.com/#/artist/album?id=12030266). In my free time, I enjoy playing rhythm games like [osu!](https://osu.ppy.sh) and watching slice-of-life (iyashikei) anime like [miss kobayashi's dragon maid](https://maidragon.jp/) (i like [elma](https://maid-dragon.fandom.com/wiki/Elma) very much).

## Research Interests {#research-interests}

**<u>High-Quality</u>** and **<u>Controllable</u>** Music Generation:
- **High-Quality:** speech/singing voice enhancement (de-noise, de-reverb, super-resolution, etc.), music restoration.
- **Controllable:** singing voice generation/conversion, accompaniment generation, music-to-music generation.

<!-- {% include_relative _includes/news.md %} -->

{% include_relative _includes/publications.md %}

{% include_relative _includes/talks.md %}

{% include_relative _includes/education.md %}

{% include_relative _includes/services.md %}

