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
            <div class="pub-row">

              {% if link.image %}

                <div
                  class="col-sm-3 abbr"
                  style="position:relative;padding-right:15px;padding-left:15px;"
                >

                  <img
                    src="{{ link.image }}"
                    class="teaser img-fluid z-depth-1"
                    style="width:100%;"
                    alt="{{ link.title }}"
                  >

                  {% if link.conference_short %}
                    <abbr class="badge">
                      {{ link.conference_short }}
                    </abbr>
                  {% endif %}

                </div>

                <div
                  class="col-sm-9"
                  style="position:relative;padding-right:15px;padding-left:20px;"
                >

              {% else %}

                <div style="width:100%;padding:0 2px;">

              {% endif %}


                  <!-- Title -->
                  <div class="title">

                    {% if link.paper %}

                      <a
                        href="{{ link.paper }}"
                        target="_blank"
                        rel="noopener"
                      >
                        {{ link.title }}
                      </a>

                    {% elsif link.arxiv %}

                      <a
                        href="{{ link.arxiv }}"
                        target="_blank"
                        rel="noopener"
                      >
                        {{ link.title }}
                      </a>

                    {% elsif link.pdf %}

                      <a
                        href="{{ link.pdf }}"
                        target="_blank"
                        rel="noopener"
                      >
                        {{ link.title }}
                      </a>

                    {% else %}

                      {{ link.title }}

                    {% endif %}


                    <!-- Venue badge beside title if no image -->
                    {% unless link.image %}

                      {% if link.conference_short %}
                        <abbr
                          class="badge"
                          style="
                            margin-left:6px;
                            background-color:var(--global-theme-color);
                            color:white !important;
                          "
                        >
                          {{ link.conference_short }}
                        </abbr>
                      {% endif %}

                    {% endunless %}

                  </div>


                  <!-- Authors -->
                  <div class="author">
                    {{ link.authors }}
                  </div>


                  <!-- Conference -->
                  <div class="periodical">
                    <em>{{ link.conference }}</em>
                  </div>


                  <!-- Buttons -->
                  <div class="links">


                    <!-- Official paper / publisher page -->
                    {% if link.paper %}
                      <a
                        href="{{ link.paper }}"
                        class="btn btn-sm z-depth-0"
                        role="button"
                        target="_blank"
                        rel="noopener"
                        style="font-size:12px;"
                      >
                        Paper
                      </a>
                    {% endif %}


                    <!-- arXiv -->
                    {% if link.arxiv %}
                      <a
                        href="{{ link.arxiv }}"
                        class="btn btn-sm z-depth-0"
                        role="button"
                        target="_blank"
                        rel="noopener"
                        style="font-size:12px;"
                      >
                        arXiv
                      </a>
                    {% endif %}


                    <!-- Direct PDF -->
                    {% if link.pdf %}
                      <a
                        href="{{ link.pdf }}"
                        class="btn btn-sm z-depth-0"
                        role="button"
                        target="_blank"
                        rel="noopener"
                        style="font-size:12px;"
                      >
                        PDF
                      </a>
                    {% endif %}


                    <!-- Code -->
                    {% if link.code %}
                      <a
                        href="{{ link.code }}"
                        class="btn btn-sm z-depth-0"
                        role="button"
                        target="_blank"
                        rel="noopener"
                        style="font-size:12px;"
                      >
                        Code
                      </a>
                    {% endif %}


                    <!-- Poster -->
                    {% if link.poster %}
                      <a
                        href="{{ link.poster }}"
                        class="btn btn-sm z-depth-0"
                        role="button"
                        target="_blank"
                        rel="noopener"
                        style="font-size:12px;"
                      >
                        Poster
                      </a>
                    {% endif %}


                    <!-- Video -->
                    {% if link.video %}
                      <a
                        href="{{ link.video }}"
                        class="btn btn-sm z-depth-0"
                        role="button"
                        target="_blank"
                        rel="noopener"
                        style="font-size:12px;"
                      >
                        Video
                      </a>
                    {% endif %}


                    <!-- Slides -->
                    {% if link.slides %}
                      <a
                        href="{{ link.slides }}"
                        class="btn btn-sm z-depth-0"
                        role="button"
                        target="_blank"
                        rel="noopener"
                        style="font-size:12px;"
                      >
                        Slides
                      </a>
                    {% endif %}


                    <!-- Project Page -->
                    {% if link.page %}
                      <a
                        href="{{ link.page }}"
                        class="btn btn-sm z-depth-0"
                        role="button"
                        target="_blank"
                        rel="noopener"
                        style="font-size:12px;"
                      >
                        Project Page
                      </a>
                    {% endif %}


                    <!-- Optional note -->
                    {% if link.notes %}
                      <strong>
                        <i style="color:#e74d3c;">
                          {{ link.notes }}
                        </i>
                      </strong>
                    {% endif %}


                  </div>

                </div>

            </div>
          </li>

          <br>

        {% endfor %}

      </ol>
    </div>

  {% endif %}

{% endfor %}

