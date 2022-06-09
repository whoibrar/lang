---
published : true

title : "Liquid Programming Language"
permalink : "/liquid"
layout : note
excerpt : 

alias : 
categories : 
tags : 

created_at: 2022-06-04 01:23:48 +0530
modified_at: 2022-06-09 21:53:44 +0530
---


### Liquid Syntax

```liquid
{% raw %}
{% %} --> logic
{{ }} --> output
{% endraw %}


boolean Operators
< <= == != >= >
or and 
contains 
```

### How Liquid Works on Shopify
- User Request
- Shopify works out store
- Shopify selects the liquid template
- liquid placeholders replaced with data stored
- Compiled html file sent to browser
- Browser processes html and fetches required js,css,etc.
- [source](https://i.imgur.com/9mdwhCR.png)

### Load Liquid Template
```liquid

// layout/fullwidth.liquid

{% raw %}
{% layout 'fullwidth' %}
{% endraw %}
```

### Directory Structure
```
root
	|__Layout
	|__Templates
	|__Sections
	|__Snippets
	|__Assets
	|__Config
	|__Locales
```

---

Return to [[Programming]]

---
