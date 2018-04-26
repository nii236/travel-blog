+++
date = "2018-04-01T19:25:11+08:00"
description = "North Road"
title = "Test post please ignore"
slug = "test"
tags = [ "test" ]
+++

This test post tries out the new Hugo page resource functionality, mostly regarding images.

{{< img "images/test001.jpg" "This is a caption" >}}


Some good information in this [blog post](https://regisphilibert.com/blog/2018/01/hugo-page-resources-and-how-to-use-them/).

Basically:

- Create folder in content (page bundle)
- Put index.md and image/imagesstuff.jpg in there
- Create a shortcode in layouts/shortcodes/blah.html which uses the $image.resize functionality.
- Use the shortcode in your markdown

Done!

The image above was very high resolution, and resized to 512px. This way I can put max resolution stuff on the blog and have it served at smaller resolutions to the clients! Neat!

Here is the code for the shortcode: 

```
{{ $img := $.Page.Resources.GetMatch (.Get 0)}}                                                         
{{ $image := $img.Resize "512x" }}                                                                      
<figure style="margin:auto; width: {{ add $image.Width 3 }}px; padding: 3px; background-color: #cccc">  
    <img src="{{ $image.RelPermalink }}" width="{{ $image.Width }}" height="{{ $image.Height }}">       
    {{ if ne (.Get 1) "" }}                                                                             
    <figcaption style="text-align: center;">                                                            
    <small>                                                                                             
    {{ (.Get 1) }}                                                                                      
    </small>                                                                                            
    </figcaption>                                                                                       
    {{ end }}                                                                                           
</figure>                                                                                               
```
