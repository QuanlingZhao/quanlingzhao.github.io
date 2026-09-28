<h2 id="publications" style="margin: 2px 0px 2px;">Publications</h2>

{% assign groups = "under_review,peer_reviewed,workshops" | split: "," %}

{% for group in groups %}
{% assign papers = site.data.publications[group] %}

{% if papers and papers.size > 0 %}

{% case group %}
{% when "under_review" %}
{% assign heading = "Manuscripts Under Review" %}
{% when "peer_reviewed" %}
{% assign heading = "Peer-Reviewed Publications" %}
{% when "workshops" %}
{% assign heading = "Workshop Papers, Posters, and Demos" %}
{% endcase %}

<h3 style="margin-top:18px;">{{ heading }}</h3>

<div class="publications">
<ol class="bibliography">

{% for link in papers %}

<li>

<div style="width:100%;padding:0 2px;">

<div class="title">

{% if link.paper %}
<a href="{{ link.paper }}" target="_blank" rel="noopener">{{ link.title }}</a>
{% elsif link.arxiv %}
<a href="{{ link.arxiv }}" target="_blank" rel="noopener">{{ link.title }}</a>
{% elsif link.pdf %}
<a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>
{% else %}
{{ link.title }}
{% endif %}

{% if link.conference_short %}
<abbr
class="badge"
style="margin-left:6px;background-color:var(--global-theme-color);color:white !important;"
>
{{ link.conference_short }}
</abbr>
{% endif %}

</div>


<div class="author">
{{ link.authors }}
</div>


<div class="periodical">
<em>{{ link.conference }}</em>
</div>


<div class="links">

{% if link.paper %}
<a
href="{{ link.paper }}"
class="btn btn-sm z-depth-0"
role="button"
target="_blank"
rel="noopener"
style="font-size:12px;"
>Paper</a>
{% endif %}

{% if link.arxiv %}
<a
href="{{ link.arxiv }}"
class="btn btn-sm z-depth-0"
role="button"
target="_blank"
rel="noopener"
style="font-size:12px;"
>arXiv</a>
{% endif %}

{% if link.pdf %}
<a
href="{{ link.pdf }}"
class="btn btn-sm z-depth-0"
role="button"
target="_blank"
rel="noopener"
style="font-size:12px;"
>PDF</a>
{% endif %}

{% if link.code %}
<a
href="{{ link.code }}"
class="btn btn-sm z-depth-0"
role="button"
target="_blank"
rel="noopener"
style="font-size:12px;"
>Code</a>
{% endif %}

{% if link.poster %}
<a
href="{{ link.poster }}"
class="btn btn-sm z-depth-0"
role="button"
target="_blank"
rel="noopener"
style="font-size:12px;"
>Poster</a>
{% endif %}

{% if link.video %}
<a
href="{{ link.video }}"
class="btn btn-sm z-depth-0"
role="button"
target="_blank"
rel="noopener"
style="font-size:12px;"
>Video</a>
{% endif %}

{% if link.slides %}
<a
href="{{ link.slides }}"
class="btn btn-sm z-depth-0"
role="button"
target="_blank"
rel="noopener"
style="font-size:12px;"
>Slides</a>
{% endif %}

{% if link.page %}
<a
href="{{ link.page }}"
class="btn btn-sm z-depth-0"
role="button"
target="_blank"
rel="noopener"
style="font-size:12px;"
>Project Page</a>
{% endif %}

{% if link.notes %}
<strong>
<i style="color:#e74d3c;">{{ link.notes }}</i>
</strong>
{% endif %}

</div>


{% if link.teaser %}
<div
style="
margin-top:10px;
margin-bottom:5px;
width:100%;
"
>
<img
src="{{ link.teaser }}"
alt="Teaser figure for {{ link.title }}"
style="
display:block;
width:auto;
max-width:460px;
max-height:180px;
object-fit:contain;
border-radius:4px;
"
>
</div>
{% endif %}


</div>

</li>

<br>

{% endfor %}

</ol>
</div>

{% endif %}
{% endfor %}
