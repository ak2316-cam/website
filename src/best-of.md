---
layout: page
title: My favourite posts
---

I haven't really written any posts yet, but when I have this page will be just the very best! If you'd rather read the complete list, I have [another page](/all-posts/) with those too.

{% assign posts = site.posts | where_exp: "post", "post.index != nil" | where: "index.best_of", true %}
{% include archive_list.html %}
