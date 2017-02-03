---
layout: post
title:  Liquid-if/else
tags: Liquid
categories: Jekyll
---

3. If / Else
条件语句，可以使用关键字有：if、unless、elsif、else。
\~\~
{% raw %}
{% if user %}
 2   Hello {{ user.name }}
 3 {% endif %}
 4 
 5 # Same as above
 6 {% if user != null %}
 7   Hello {{ user.name }}
 8 {% endif %}
 9 
10 {% if user.name == 'tobi' %}
11   Hello tobi
12 {% elsif user.name == 'bob' %}
13   Hello bob
14 {% endif %}
15 
16 {% if user.name == 'tobi' or user.name == 'bob' %}
17   Hello tobi or bob
18 {% endif %}
19 
20 {% if user.name == 'bob' and user.age \> 45 %}
21   Hello old bob
22 {% endif %}
23 
24 {% if user.name != 'tobi' %}
25   Hello non-tobi
26 {% endif %}
27 
28 # Same as above
29 {% unless user.name == 'tobi' %}
30   Hello non-tobi
31 {% endunless %}
32 
33 # Check for the size of an array
34 {% if user.payments == empty %}
35    you never paid !
36 {% endif %}
37 
38 {% if user.payments.size \> 0  %}
39    you paid !
40 {% endif %}
41 
42 {% if user.age \> 18 %}
43    Login here
44 {% else %}
45    Sorry, you are too young
46 {% endif %}
47 
48 # array = 1,2,3
49 {% if array contains 2 %}
50    array includes 2
51 {% endif %}
52 
53 # string = 'hello world'
54 {% if string contains 'hello' %}
55    string includes 'hello'
56 {% endif %}
{% endraw %}
\~\~\~
{: .language-ruby}