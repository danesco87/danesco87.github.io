---
layout: post
title:  "MathJax in Jekyll"
date:   2021-11-10 14:01:00 -0400
categories: mathjax jekyll tutorial
---
[This](http://webdocs.cs.ualberta.ca/~zichen2/blog/coding/setup/2019/02/17/how-to-add-mathjax-support-to-jekyll.html) tutorial works to connect MathJax with Jekyll. The only step that you need to be aware is the following:

>Add these lines to _includes/head.html:

```
    <!-- for mathjax support -->
      {% raw %}{% if page.usemathjax %}{% endraw %}
      <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
        TeX: { equationNumbers: { autoNumber: "AMS" } }
        });
      </script>
      <script type="text/javascript" async src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script
      {% raw %}{% endif %}{% endraw %}
```
    
Use https instead http so this can work in GitHub pages correctly.
