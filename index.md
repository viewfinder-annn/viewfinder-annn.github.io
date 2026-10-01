---
layout: homepage
---

## About Me {#about-me}

Hi :D ! I'm a <span id="phd-year">...</span> Ph.D. student at The Chinese University of Hong Kong, Shenzhen, advised by [Prof. Zhizheng Wu](https://drwuz.com/). I spent my undergraduate studies at Fudan University, majoring in software enginnering, with [Prof. Bihuan Chen](https://chenbihuan.github.io/) and [Prof. Kaifeng Huang](https://kaifeng-h.github.io/).

Beyond academia, I'm an amateur music producer with over 2 million plays on [netease cloud music](https://music.163.com/#/artist/album?id=12030266). In my free time, I enjoy playing rhythm games like [osu!](https://osu.ppy.sh) and watching slice-of-life (iyashikei) anime like [miss kobayashi's dragon maid](https://maidragon.jp/) (i like [elma](https://maid-dragon.fandom.com/wiki/Elma) very much).

<!-- **I'm currently a research intern at [ByteDance Seed](https://seed.bytedance.com/), developing the SeedMusic model.** -->

<p style="font-size: 0.95rem; margin-top: -8px;"><a class="tihu-link" href="./assets/img/tihu.jpg" target="_blank">"鹈鹕" is a black & white british shorthair<img src="./assets/img/tihu.jpg" alt=""></a>, <span id="tihu-age">...</span> old. He became my family member since November 2024, and has lived with me for <strong id="tihu-days">...</strong> days.</p>
<script>
(function () {
  var now = new Date();
  var year = now.getFullYear();
  var month = now.getMonth() + 1;
  var phdStartYear = 2024;
  var academicYear = year - phdStartYear + (month >= 9 ? 1 : 0);
  var yearNames = {1: "first-year", 2: "second-year", 3: "third-year", 4: "fourth-year", 5: "fifth-year"};
  var yearEl = document.getElementById("phd-year");
  if (yearEl) yearEl.textContent = yearNames[academicYear] || "Ph.D.";

  var birth = new Date(2024, 4, 1); // May 2024
  var home = new Date(2024, 10, 6); // Nov 6, 2024
  var msPerDay = 86400000;
  var ageYears = (now - birth) / (365.25 * msPerDay);
  var livedDays = Math.floor((new Date(year, now.getMonth(), now.getDate()) - home) / msPerDay);
  var ageEl = document.getElementById("tihu-age");
  var daysEl = document.getElementById("tihu-days");
  if (ageEl) ageEl.textContent = ageYears.toFixed(1) + " years";
  if (daysEl) daysEl.textContent = livedDays;
})();
</script>

## Research Interests {#research-interests}

**<u>High-Quality</u>** and **<u>Controllable</u>** Music Generation:
- **High-Quality:** speech/singing voice enhancement (de-noise, de-reverb, super-resolution, etc.), music restoration.
- **Controllable:** speech/singing voice generation/editing, accompaniment generation, music-to-music generation.

<!-- {% include_relative _includes/news.md %} -->

{% include_relative _includes/publications.md %}

{% include_relative _includes/talks.md %}

{% include_relative _includes/education.md %}

{% include_relative _includes/services.md %}

