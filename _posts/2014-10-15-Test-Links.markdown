---
layout: post
title:  "Test links and other asset material"
date:   2014-10-02 10:00:00
categories: jekyll update
---

Current: 1

### You should see an image here:

![blabbing physicist]({{ site.baseurl }}/assets/2014-10-02-Life-in-vacuum/smbphysicist2.png)

### and the link below should make a pdf pop up

[pdf here]({{ site.baseurl }}/assets/all-pdf/Daniilidis2014-surface-noise.pdf)

#### * Tested case 0:

In `_config.yml`

`baseurl: "/altblog"`

`url: "http://nikosdaniilidis.github.io/altblog"`

In `_posts/some-post`

`![blabbing physicist]({{ site.url }}/assets/2014-10-02-Life-in-vacuum/smbphysicist2.png)`

`[pdf here]({{ site.url }}/assets/all-pdf/Daniilidis2014-surface-noise.pdf)`

* Result (not working):

==> `http://nikosdaniilidis.github.io/altblog/assets/all-pdf/Daniilidis2014-surface-noise.pdf`

#### * Tested case 1: 

In `_config.yml`

`baseurl: "/altblog"`

`url: "http://nikosdaniilidis.github.io"`

In `_posts/some-post`

`![blabbing physicist]({{ site.baseurl }}/assets/2014-10-02-Life-in-vacuum/smbphysicist2.png)`

`[pdf here]({{ site.baseurl }}/assets/all-pdf/Daniilidis2014-surface-noise.pdf)`

* Result (works!):

==> `http://nikosdaniilidis.github.io/altblog/assets/all-pdf/Daniilidis2014-surface-noise.pdf`

#### * Tested "case 2": 

In `_config.yml`

`baseurl: "/altblog"`

`url: "http://nikosdaniilidis/github.io"`

In `_posts/some-post`

`![blabbing physicist]({{ site.baseurl }}{{post.url}}/assets/2014-10-02-Life-in-vacuum/smbphysicist2.png)`

`[pdf here]({{ site.baseurl }}{{post.url}}/assets/all-pdf/Daniilidis2014-surface-noise.pdf)`

* Result (not working):

==> `http://nikosdaniilidis/github.io/assets/all-pdf/Daniilidis2014-surface-noise.pdf`


