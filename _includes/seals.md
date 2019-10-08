

<div class="card-deck">
  {% for item in site.data.seals %}
    <div class="card">
    {% if item.image %}
      <img class="card-img-top" src="{{ site.baseurl }}{{ item.image }}" alt="{{ item.img_alt }} ">
    {% endif %}
    <div class="card-body">
      <h3 class="card-title">{{ item.title }}</h3>
      <p class="card-text">{{ item.description }}</p>
      <p class="card-text">{{ item.year }}</p>
    </div>
  </div>
  {% endfor %}
</div>

