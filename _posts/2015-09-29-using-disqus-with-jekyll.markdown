---
layout: post
title: "Using Disqus With Jekyll"
subtitle: "Avoid some of my pitfalls."
permalink: "disqus-and-jekyll/"
date: 2015-09-29T00:17:51+02:00
comments: true
---

I spent most of <del>today</del> yesterday setting up a new theme for this blog. Last change for the day was adding Disqus comments. Since I ran into a few tiny issues and wanted to write a new blog post anyways I thought it couldn't hurt documenting the process.

Before starting out you'll need to register with [Disqus](https://disqus.com/admin/create/).

### Adding comments

On doing that we're going to go straight for the *universal embed code* located [here](https://disqus.com/admin/universalcode/). Check that `disqus_shortname` in the code is correctly set to what you specified earlier.


There's two things listed on the page. The embed code for the comments themselves and the embed code for displaying the comment count. Let's start with the first.


{% highlight js %}
{{ "{% if page.comments " }}%}
<div id="disqus_thread"></div>
<script type="text/javascript">
    /* * * CONFIGURATION VARIABLES * * */
    var disqus_shortname = 'yourdisqusshortname';

    /* * * DON'T EDIT BELOW THIS LINE * * */
    (function() {
        var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
        dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
        (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript>
{{ "{% endif "}}%}
{% endhighlight %}

I wrapped the code from Disqus in a liquid if statement as well. This checks if your post's frontmatter contains a comments field. Go ahead and add that as `comments: true`. Doing it this way lets you disable comments for a post if needed.

Now go ahead and add that code to your `_layouts/post.html`. It'll probably go somewhere after `{ content }`, where exactly depends on your theme.

That should be all for displaying the comments on a page. Only follow along with the rest if you're looking to add comments counts as well.

### Adding comment counts

Add the following code to your `_includes/footer.html` (be sure to change your shortname if copying from here).

{% highlight js %}
<!-- Disqus Comments -->
<script type="text/javascript">
    /* * * CONFIGURATION VARIABLES * * */
    var disqus_shortname = 'yourdisqusshortname';

    /* * * DON'T EDIT BELOW THIS LINE * * */
    (function () {
        var s = document.createElement('script'); s.async = true;
        s.type = 'text/javascript';
        s.src = '//' + disqus_shortname + '.disqus.com/count.js';
        (document.getElementsByTagName('HEAD')[0] || document.getElementsByTagName('BODY')[0]).appendChild(s);
    }());
</script>
{% endhighlight %}

This code will be responsible for checking all occurrences of comment counts on the page and updating them. First we're going to have to tell it where these comment counts are.

{% highlight html %}
{{ "{% if post.comments " }}%}
<a href="{{ "{% post.url "}}%}index.html#disqus_thread" data-disqus-identifier="{{ "{% post.url "}}%}"></a>
{{ "{% endif "}}%}
{% endhighlight %}

This is the code you'll want to insert in your `index.html` wherever you want comment counts for a specific post. It sets a custom Disqus identifier which relies only on the post's permalink, which is rather handy if your blog's URL should ever change.

The code is slightly different when adding this to the post's page. This goes into `_layouts/post.html`:

{% highlight html %}
{{ "{% if page.comments " }}%}
<a href="{{ "{% page.url "}}%}index.html#disqus_thread" data-disqus-identifier="{{ "{% page.url "}}%}"></a>
{{ "{% endif "}}%}
{% endhighlight %}

See how this uses `page` instead of `post`.

Congratulations if setting up comment counts like this was clear to you from reading the Disqus instructions. It took me a few tries to get this right. You might be wondering though why nothing is showing up on your page even though you seemingly did everything right. Don't worry, you probably did, it just takes Disqus a while to actually refresh the comment count. Just wait a few minutes. Similarly the count will take a bit to update when it should be increasing later.

Something else I ran into when setting this up were custom permalinks I have set for a few posts. This becomes relevant when using the comment count code snippets above. `post.url` or `page.url` returns the current post's URL as `/post/`. Should you however use a custom permalink and not manually end that with a slash, you'll get a URL that does not end in one, so be sure to end that trailing slash to your custom permalinks.

Hopefully everything should be working for you at this point. If not, why not leave a comment below 😜
