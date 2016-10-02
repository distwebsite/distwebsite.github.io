---
layout: service
title:  "Pisi Family"
lang: en
encoding: utf-8
date:   2016-08-04 22:15:04
category: service
sequence: 0
description: "Pisi Family"
image: 5.re.jpg
active: services
---

<div class='wrapper'>
    {% assign services = site.categories.service | sort: 'sequence' %}
    {% for service in services %}
        {% if service.sequence != 0 %}
        <div class='col-lg-4 col-md-6 col-sm-6 col-xs-12'>               
                {%assign imagePath = service.image | prepend: "/images/" | prepend:site.baseurl %}
                <a class='card-image-link action' href="{{service.url}}">
                    <div class='card-image' style="background-image:url('{{imagePath}}')">
                        <div class='thumbs-up'>
                            <i class="{{service.icon}}" aria-hidden="true"></i>    
                        </div>
                    </div>
                </a>                    
                <div class='content'>
                    <h5>
                        <a class='action' href="{{service.url}}">
                            <strong>
                                {{service.title}}
                            </strong>                                    
                        </a>
                    </h5>
                    {{service.description | truncate: 300}}
                </div>              
            </div>
        </div>
        {% endif %}
    {% endfor %}			
</div>

<div class='clearfix'></div>
