<div id="publications" style="margin: 2px 0px -5px;">
    <h2 style="margin-bottom: 5px;">Selected Publications</h2>
    <p style="margin-top: -5px;">Full list at <a href="https://scholar.google.com/citations?user=r1VH6rsAAAAJ" target="_blank">Google Scholar</a>. *Equal Contribution.
    </p>
</div>

{% assign publication_categories = "Audio Enhancement,Music Generation,Misc" | split: "," %}
{% assign category_keys = "audio_enhancement,music_generation,misc" | split: "," %}

{% for category_name in publication_categories %}
{% assign category_key = category_keys[forloop.index0] %}
{% assign publications = site.data.publications[category_key] %}

{% if publications %}
<h3 style="margin-top: 0px; margin-bottom: 10px;">{{ category_name }}:</h3>
<div class="publications">
<ol class="bibliography" style="margin-top: 0;">

{% for link in publications %}
<li style="margin-bottom: 15px;">
<div class="pub-row" style="display: flex; align-items: center;">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 5px;padding-left: 5px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <span style="color:#e74d3c">{{ link.notes }}</span></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
{% endfor %}

</ol>
</div>
{% endif %}
{% endfor %}