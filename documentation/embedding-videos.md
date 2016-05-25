# Embedding Videos

If you want to embed videos in articles it helps to follow the following markup conventions:

## Use `<iframe>` not `[embed]URL[/embed]`

Although the Shortcode embedding technique is built into WordPress it is not a great idea to rely on it. Who knows when we might make a move away from WordPress, right?

So instead of using the WordPress native embed method it is preferred to do it the "oldschool way" – with HTML.

## Syntax? Syntax!

As we want our videos to be responsive we need to perform a little [magic trick](http://alistapart.com/article/creating-intrinsic-ratios-for-video). We want the video to keep its aspect-ratio no matter what the viewport of our readers may look like.

That's why we wrap our video in the `<figure>` element first. This element will always span the whole width of articles inside Smashing Magazine. Inside of the `<figure>` element we add a `<div class="aspect-ratio">` also wrapping the video. This container makes sure the intrinsic ratio is kept alive at all times.

When pasting in the `<iframe>` make sure to remove the width and height attributes from it because otherwise they might restrict the iframe to a certain width/height and thereby break in narrow or extremely wide viewports.

If a caption needs to be added to the video that's also not a problem. Right after the closing `</div>` you may add in `<figcaption></figcaption>` and place whatever text in between those two tags.

## Whitespace is a problem in WordPress

You might have noticed in the past that somehow someway WordPress sees whitespace in some spots as a call to action to add in empty `<p></p>` tags. That way it creates unhelpful, unneeded and most of the time pretty ugly extra whitespace around certain elements.

In order to prevent WordPress from doing so it is mandatory to leave out any whitespace (just don't use the spacebar at all) when writing HTML for videos in the Magazine.

## Complete Example

I'll give you some delicious copypasta to use as some kind of template when integrating videos. It has all the features I talked about and if you don't need a caption you can sure delete that part but anyways:

```
<figure>
  <div class="aspect-ratio"><iframe src="#" frameborder="0" allowfullscreen>Fallback Text for non-supporting browsers and screenreaders</iframe></div><figcaption>Whatever caption you want to give goes here. With a <a href="#">Link</a>? Sure.</figcaption>
</figure>
```

Unfortunately we do need to keep that `frameborder="0"` attribute/value combo on the iframe because some browsers still want to draw borders around the object. The `allowfullscreen` boolean goes without any value because it's either there or not there. It enabled the fullscreen feature.
