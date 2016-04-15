{% for p in site.pages %}
{% if p.parent == page.label %}
* [{{p.bigtitle}}]({% include github_prefix %}{{p.url}})
{% endif %}
{% endfor %}
