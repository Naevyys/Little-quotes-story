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

<!-- Missing image sources -->
{% include banner.html
  title=site-title
  image_url="assets/images/democrat-donkey-vs-republican-elephant-1015211.webp"
  description=site-description
  isHeader=true
%}

[Introduction text]  

{% include banner.html
  title="Biases"
  image_url="assets/images/biden-trump.webp"
  description="Insert description here"
%}

[Biases in our data. Do we want to use a [dedicated page](/biases) for them?]

{% include banner.html
  title="Analysis outcomes"
  image_url="assets/images/boxing-gloves.jpg"
  description="Insert description here"
%}

[Let's tell a story here!] 

<!-- Sample plot -->
{% include plots/test_1.html %}

Sample columns:  <!-- Plotly plots refuse to render inside columns, so use this element only with isPlotly=false -->

{% include columns.html
  isPlotly=false
  textIsImg=true
  plot="assets/images/democrat-donkey-vs-republican-elephant-1015211.webp"
  text="assets/images/boxing-gloves.jpg"
  text_lorem="Lorem ipsum dolor sit amet, consectetur adipiscing elit. In tempus, purus non sollicitudin egestas, metus tortor dignissim tortor, id tincidunt leo ex quis elit. Cras vitae ipsum ut elit porta congue. Nam ac erat congue lectus pulvinar eleifend. Aliquam id elementum neque, nec interdum augue. Pellentesque porttitor bibendum ante malesuada commodo. Nullam faucibus nisl vitae erat dictum hendrerit. Aliquam facilisis mattis tempor. Etiam ac ligula suscipit, dictum justo eleifend, tempor ex. Nullam iaculis iaculis enim vel aliquam. Quisque accumsan ex felis, sit amet sollicitudin mauris elementum a."
%}

[More story] 
 
<!-- Sample image inside text -->
![images](assets/images/democrat-donkey-vs-republican-elephant-1015211.webp)

[Yet more story] 

{% include banner.html
  title="References"
  image_url="assets/images/Democrat-vs-Republican.jpg"
  description="Insert description here"
%}

[Sources of data (Quotebank, wikidata, info on news outlets, images etc.)]

{% include banner.html
  title="About us"
  image_url="assets/images/donkey-elephant.jpg"
  description="Insert description here"
%}

<!-- Imo not needed but I give you the choice :) -->
[Some info about the team members? On a separate page?]

{% include banner.html
  title="I don't have sections anymore, just for the picture"
  image_url="assets/images/donkey-elephant-simple.webp"
  description="Insert description here"
%}
