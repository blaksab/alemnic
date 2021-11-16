---
layout: default
feature_text: |
  ## Alembic
  A Jekyll boilerplate theme designed to be a starting point for any Jekyll website
feature_image: "https://picsum.photos/1300/400?image=989"
collectionpage: posts
---


<main class="main  container">

  <div class="content">

    <article class="article  article--page  typeset">

      {% if paginator.posts %}
        {% assign collectiondata = site.collections | where: "label", page.collectionpage | first %}
        <h1>{{ collectiondata.title }}</h1>
        {{ collectiondata.description | markdownify }}

      {% else %}
        <h1>{{ page.title }}</h1>
        {{ content }}
        
      {% endif %}

    </article>

    {% include post-list.html %}

  </div>

  {% if page.aside == true %}{% include site-aside.html %}{% endif %}

</main>

{% include site-footer.html %}

