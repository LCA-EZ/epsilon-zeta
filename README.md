epsilon-zeta
============

###How to get started
1. Install Ruby (it should be pre-installed in Mac OS X, so you can probably ignore this)
2. use the "bundle" command to download all the Jekyll dependencies
3. use the "jekyll serve" command to get the site running (right now, there's just hello world on the index page)

###How to add data (e.g. members and photos)
In the _data directory, each of these has its own YAML file, where you can hard code the data you want.
To add new a new entry, start it with a hyphen and list every key in the same indentation level. In the case of photos, just put in the path.

###How to access the data
In the HTML file, you should be able to do a for...in loop on site.data.* where * is either members or photos. Make sure to wrap it in {% %} .
To access the value of each iteration, wrap it in {{}} when you call it. 
For example,
<pre><code>
  {% for member in site.data.members %}
    <span>{{member.name}}</span>
  {% endfor %}
</pre></code>

