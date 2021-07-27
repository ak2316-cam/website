---
layout: page
post_list_date_format: day_month
---

<style>
  img.profile {
    float: right;
    width: 250px;
    max-width: 50%;
    margin-top: 0.4em;
    margin-left: 1em;
    margin-bottom: 1em;
  }

  .archive__date {
    padding-right: 4px;
  }
</style>

<img src="/images/profileptolemy.png" class="profile" alt="A diagram used in a projective proof of Ptolemy's theorem">

## Welcome! I'm Adam and this is where I put stuff.

I'm a first year Mathematics student at the [University of Cambridge](https://www.undergraduate.study.cam.ac.uk/courses/mathematics), studying at [Gonville and Caius](https://www.cai.cam.ac.uk) College. Currently, I'm also spending the summer as an Engineer at [Evervault](https://evervault.com), working on making the web a more secure place.

My main goal in setting up this website is to have a place to put my [lecture notes](/lecture-notes/), along with some of the [olympiad materials](/olympiads/) that I have accumulated. I also have a [blog](/all-posts/), where I write about things that interest me. 

## Recent posts

{% assign posts = site.posts | slice: 0, 5 %}
{% include archive_list.html %}

## Get in touch

I'm always happy to hear from anyone! The best way to reach me is at {{ site.emails.personal | create_mailto_link }}, or [@adamkelly2201](https://twitter.com/adamkelly2201) on Twitter.
