

<div class="card-deck">
{% for item in site.data.seals %}
  <div class="card">
  {% if item.image %}
    <img class="card-img-top-seal" src="{{ site.baseurl }}{{ item.image }}" width="298px" alt="{{ item.img_alt }}">
  {% endif %}
    <div class="card-body">
      <h3 class="card-title">{{ item.year }}</h3>
    </div>
  </div>
{% endfor %}
</div>

