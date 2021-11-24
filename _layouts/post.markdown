---
layout: default
---

<div class="post-head">
  <div class="container">
    <div class="row">
      
      {% if page.video_embed %}
      <div class="col col-12">
        <div class="post-video">
          <div class="post-video__wrap">
            <iframe src="{{ page.video_embed }}" loading="lazy" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
          </div>
        </div>
      </div>
      {% else %}

      {%if page.image %}
      <div class="col col-6 col-d-12">
        <div class="post-image">
          <img class="lazy" data-src="{{site.baseurl}}{{page.image}}" alt="{{page.title}}">
        </div>
      </div>
      {%endif %}

      {% endif %}
      
      {% if page.video_embed %} {% assign videoInfo = 'post__info-video' %} {% endif %}
      <div class="col {% if page.video_embed %}col-12{% else %}col-6 col-d-12{% endif %}">
        <div class="post__info {{videoInfo}}">
  
          {% if page.tags.size >= 1 %}
            <div class="post__tags">
              {% for tag in page.tags %}
                <a href="{{ site.baseurl }}/tags#{{ tag }}" class="post__tag">{{ tag }}</a>
              {% endfor %}
            </div>
          {% endif %}
  
          <h1 class="post__title">{{ page.title | escape }}</h1>

              {% if page.authors %}
                <div class="flex flex-col pb-3 md:hidden">
                  {% for author in page.authors %}
                    {% include author-large.html
                      author=author
                    %}
                  {% endfor %}
                </div>
              {% endif %}

              <!-- <img width="1600" height="900" src="{{ page.image }}"/> -->

              <div class="flex flex-col md:flex-row py-6 md:py-12">

                <div class="w-full md:w-3/12 pr-3">
                  {% if page.authors %}
                    <div class="flex flex-col hidden md:flex mb-3 md:mb-6">
                      {% for author in page.authors %}
                        {% include author-large.html
                      author=author
                      %}
                      {% endfor %}
                    </div>
                  {% endif %}
          <!-- <div class="post__meta">
            <a href="{{site.baseurl}}/about/" class="post__author-image">
              <img class="lazy" data-src="{{site.author.author__avatar}}" alt="{{site.author.author__name}}">
            </a> -->

            <div class="post__meta-bottom">
              <a class="post__author" href="{{site.baseurl}}/about/">{{site.author.author__name}}</a>
              <time class="post__date" datetime="{{ page.date | date_to_xmlschema }}">{{ page.date | date_to_string }}</time>
            </div>
          <!-- </div> -->
  
        </div>
      </div>
    </div>
  </div>
</div>

<!-- begin post -->
<div class="container animate">

  <article class="post">

    <div class="post__content">
      {{ content }}
    </div>

    <div class="post__share">
      <ul class="share__list list-reset">
        <li class="share__item">
          <a class="share__link share__twitter"
            href="https://twitter.com/intent/tweet?text={{ page.title | uri_escape }}&url={{ site.url }}{{ site.baseurl }}{{ page.url }}"
            onclick="window.open(this.href, 'pop-up', 'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"
            title="Share on Twitter" rel="nofollow"><i class="ion ion-logo-twitter"></i></a>
        </li>
        <li class="share__item">
          <a class="share__link share__facebook" href="https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{ site.baseurl }}{{ page.url }}"
            onclick="window.open(this.href, 'pop-up', 'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"
            title="Share on Facebook" rel="nofollow"><i class="ion ion-logo-facebook"></i></a>
        </li>
       <li class="share__item">
          <a class="share__link share__microsoft" href="http://www.microsoft.com/education/products/teamspin/create/button/?url={{ site.url }}{{ page.url }}&amp;media={{ site.url }}{{ site.baseurl }}{{ page.image }}&amp;description={{ page.title | uri_escape }}"
          onclick="window.open(this.href, 'pop-up', 'left=20,top=20,width=900,height=500,toolbar=1,resizable=0'); return false;" title="Share on microsoft"
          rel="nofollow"><i class="ion ion-logo-windows"></i></a>
        </li>
        <li class="share__item">
          <a class="share__link share__linkedin" href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{ site.baseurl }}{{ page.url }}&title={{ page.title | uri_escape }}&summary={{ page.description | uri_escape }}&source={{ site.title | uri_escape }}"
          onclick="window.open(this.href, 'pop-up', 'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" title="Share on LinkedIn" rel="nofollow"><i class="ion ion-logo-linkedin"></i></a>
        </li>
      </ul>
    </div>


  </article>
</div>
<!-- end post -->

{% include related-posts.html %}

{% if site.disqus-identifier %}
  <div class="container">
    <div class="row">
      <div class="col col-12">
        {% include disqus-comments.html %} 
      </div>
    </div>
  </div>
{% endif %}