---
layout: all_posts_base
title: All posts by tag
archive_variant: global
post_list_date_format: month_year
---

<h3>Tags</h3>

<ul id="tag_cloud">
  {% assign posts_by_tag = site.data["posts_by_tag"] | sort %}
  {% for tag_entry in posts_by_tag %}
    {% assign tag_name = tag_entry[0] %}
    {% assign style_data = site.data["tag_cloud_data"][tag_name] %}

    <li>
      <a id="tag--{{ tag_name }}" href="#{{ tag_name }}" style="font-size: {{ style_data['size'] }}pt; color: {{ style_data['hex'] }}">{{ tag_name | replace: "-", "&#8209;" }}</a>
    </li>

{% endfor %}

</ul>

<div class="post__separator" aria-hidden="true">&#9670;</div>

{% for tag_entry in posts_by_tag %}

  <h3 id="{{ tag_entry[0] }}">{{ tag_entry[0] }}</h3>

{% assign posts = tag_entry[1] %}
{% include archive_list.html %}
{% endfor %}
