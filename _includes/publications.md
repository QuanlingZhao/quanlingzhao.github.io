<h2 id="publications" style="margin: 2px 0px 2px;">Publications</h2>

{% assign groups = "under_review,peer_reviewed,workshops" | split: "," %}
{% for group in groups %}
  {% case group %}
    {% when "under_review" %}{% assign heading = "Manuscripts Under Review" %}
    {% when "peer_reviewed" %}{% assign heading = "Peer-Reviewed Publications" %}
    {% when "workshops" %}{% assign heading = "Workshop Papers, Posters, and Demos" %}
  {% endcase %}

  <h3 style="margin-top:18px;">{{ heading }}</h3>
  <div class="publications">
    <ol class="bibliography">
    {% assign papers = site.data.publications[group] %}
    {% for link in papers %}
      <li>
        <div class="pub-row">
          {% if link.image %}
          <div class="col-sm-3 abbr" style="position:relative;padding-right:15px;padding-left:15px;">
            <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width:100%;">
            {% if link.conference_short %}<abbr class="badge">{{ link.conference_short }}</abbr>{% endif %}
          </div>
          <div class="col-sm-9" style="position:relative;padding-right:15px;padding-left:20px;">
          {% else %}
          <div style="width:100%;padding:0 2px;">
          {% endif %}
            <div class="title">
              {% if link.pdf %}<a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}
              {% if link.conference_short %}<abbr class="badge" style="margin-left:6px;">{{ link.conference_short }}</abbr>{% endif %}
            </div>
            <div class="author">{{ link.authors }}</div>
            <div class="periodical"><em>{{ link.conference }}</em></div>
            <div class="links">
              {% if link.pdf %}<a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Paper</a>{% endif %}
              {% if link.code %}<a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Code</a>{% endif %}
              {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Project Page</a>{% endif %}
              {% if link.notes %}<strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>{% endif %}
            </div>
          </div>
        </div>
      </li>
      <br>
    {% endfor %}
    </ol>
  </div>
{% endfor %}
