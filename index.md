---
title: Little Quotes Story
layout: default
---

{% capture site-title %}
  {{ page.title | default: site.title }}
{% endcapture %}

{% capture site-description %}
  {{ page.description | default: site.description }}
{% endcapture %}

{% include banner.html
  title=site-title
  image_url="assets/images/democrat-donkey-vs-republican-elephant-1015211.webp"
  description=site-description
  isHeader=true
%}

[Introduction text]  

<!-- Missing image source -->
{% include banner.html
  title="Biases"
  image_url="assets/images/democrat-donkey-vs-republican-elephant-1015211.webp"
  description="Insert description here"
%}

[Biases in our data. Do we want to use a [dedicated page](/biases) for them?]

{% include banner.html
  title="Analysis outcomes"
  image_url="assets/images/democrat-donkey-vs-republican-elephant-1015211.webp"
  description="Insert description here"
%}

[Let's tell a story here!] 

<!-- Sample plot -->
{% include plots/test_1.html %}

[More story] 
 
<!-- Sample image inside text -->
![images](assets/images/democrat-donkey-vs-republican-elephant-1015211.webp)

[Yet more story] 

# References

[Sources of data (Quotebank, wikidata, info on news outlets, images etc.)]

# About us

<!-- Imo not needed but I give you the choice :) -->
[Some info about the team members? On a separate page?]
