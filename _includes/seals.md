
## Proposed seal update 2019

<div style="text-align: center;">
<br>
<br>
<img src="/assets/img/seals/city-seal-black-2019.png" alt="Proposed seal of the City of Chicago" />
<br>
<br>

</div>

Below are examples of the Seal of the City of Chicago over time, ending with our proposed revision. Each opens a larger version in a new window.

<div class="card-deck">
{% for item in site.data.seals %}
  {% if item.image %}
    <a href="{{ site.baseurl }}{{ item.image }}" target="_blank">
    <div class="card">
      <img class="card-img-top-seal" src="{{ site.baseurl }}{{ item.image }}" alt="{{ item.img_alt }}">
      <div class="card-body-seal">
        <h3 class="card-title usa-external_link">{{ item.year }}</h3>
      </div>
    </div>
    </a>
  {% endif %}
{% endfor %}
</div>

