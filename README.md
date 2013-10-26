compass-retina-sprite-mixin-offsets
===================================

This mixin has been developed to extend the power of compass spriting. To allow the use of two sets of icons, low-res and hi-res to be used depending on screen resolution. It has a debug mode true/false so you can see the retina images working. It also has x-y offets for both low and hi res to position the sprite precisely in it's html container.

I have been using compass sprites for about a year now, it's fantastic to say the least, using a line of sass which fires a mixin like this:    
@include icon (spotify, 1px, 3px);

This grabs the spotify.png icon from the icon folder, sets it as a background image and offsets it by x and y pixels to get it sitting in just right place. An example would be an a tag with an icon to the left of some text.

Here's the mixin that goes with it...
@mixin icon ($icon-filename, $icon-offsetx: 0, $icon-offsety: 0){
  @include icons-sprite($icon-filename, $offset-x: $icon-offsetx, $offset-y: $icon-offsety);
}

I've extended this further so now you can write the following line of sass:
@include icon (spotify, 1px, 3px, retina, 2px, 3px);

This does the same as the previous @include but the retina variable triggers the mixin to go and find icons-retina/spotify.png, a double sized version of icons/spotify.png

It also has it's own offsets as the sprite sheet can differ slightly due to rounding when it's size gets halved.

I will update and improve this readme file, make it clearer, but for now this is the gist of it...

Some things I'd like some help with are individual sprite placement on the sprite sheet. I've managed to get individual sprite spacing working, but not individual sprite placement like this:
$icons-spotify-position: 100%;

