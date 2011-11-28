---
title: Home
layout: default
---


{% for post in site.posts %}

* {{ post.date | date_to_string  }}  [{{ post.title }}]({{ post.url  }})

{% endfor %}

Github Pages test
[Git Notes](gitnotes.html)

  ___  _  _        _    _  __            

 / __|| |(_) _ _  | |__| |/ / __ _  _  _ 

 \__ \| || || ' \ | / /| ' < / _` || || |

 |___/|_||_||_||_||_\_\|_|\_\\__,_| \_, |

                                    |__/ 

