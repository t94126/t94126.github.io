---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
  
  - title: "Kuijia: Traffic rescaling in data center WANs"
    author: "Che Zhang, Hong Xu ,Libin Liu ,Zhixiong Niu ,Peng Wang ,Yongqiang Tian ,Chengchen Hu"
    booktitle: "37th IEEE Sarnoff Symposium"
    month: "Sept"
    year: "2016"
    address: "Newark, NJ"
    keywords: "Kuijia"
    url: che-sarnoff16.pdf
    bibtex: che-sarnoff16.bib
  

---

# Publications

{% for pub in page.pubs %}
{% unless pub.hidden %}
  - {% if pub.url %} [{{pub.title}}]({{pub.url}}).
    {% else %} {{pub.title}}.
    {% endif %}{% if pub.type %}({{pub.type}})
    {% endif %}<br>
    {{pub.author}}.<br>
    {% if pub.type == 'Technical Report' %}{{pub.number}}
    {% endif %}{{pub.booktitle}}{{pub.school}}{{pub.journal}}.<br>
    {% if pub.address %}{{pub.address}}.
    {% endif %} {{pub.month}}, {{pub.year}}. {% if pub.slides %}[Slides]({{pub.slides}}).
    {% endif %}<!-- {% if pub.key %}[Bibtex](http://groups.csail.mit.edu/commit/bibtex.cgi?key={{pub.key}}).
    {% endif %} -->{% if pub.bibtex %}[Bibtex]({{pub.bibtex}}).
    {% endif %}
{% endunless %}
{% endfor %}



