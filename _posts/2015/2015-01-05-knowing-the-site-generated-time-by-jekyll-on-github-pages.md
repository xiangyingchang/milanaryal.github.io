---
layout: post
title: "Knowing the site generated time by Jekyll on GitHub Pages"
date: 2015-01-05T17:08:17+05:45
redirect_from: "/2015/01/knowing-the-site-generated-time-by-jekyll-on-github-pages/"
---

If you are using Jekyll to generate your blog on GitHub Pages, you might want too know the last exact site generated time as the Jekyll generate and keep the files on `_site`.

I found the following liquid tag to do it:

{% highlight ruby %}
{% raw %}
{{ site.time }}
{% endraw %}
{% endhighlight %}

To know generated time according to your locale timezone you have to add your timezone in your `_config.yml`:

{% highlight ruby %}
{% raw %}
timezone:    Asia/Kathmandu #Add your own locale timezone
{% endraw %}
{% endhighlight %}

You can add/custumize this in the end of your site source code as following:

{% highlight ruby %}
{% raw %}
<!-- Proudly Hosted on GitHub | Generated {{ site.time }} | Revision {{ site.github.build_revision }} -->
{% endraw %}
{% endhighlight %}

Following is the generated example format:

{% highlight ruby %}
{% raw %}
<!-- Proudly Hosted on GitHub | Generated 2015-01-05 18:06:54 +0545 | Revision 8b10cc6954163643f53d0b503888578e143d7e57 -->
{% endraw %}
{% endhighlight %}

---

Happy Jekyll'ing! :sunglasses:
