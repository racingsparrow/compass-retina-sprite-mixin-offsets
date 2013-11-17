compass-retina-sprite-mixin-offsets
===================================

This mixin has been developed to extend the power of compass spriting. To allow the use of two sets of icons, low-res and hi-res to be used depending on screen resolution. 
Use icons like these free sets that have a  16px and 32px version of each icon to test with:
http://www.premiumpixels.com/freebies/41-social-media-icons-png/

It has a debug mode true/false so you can see the retina images working. It also has x-y offets for both low and hi res to position the sprite precisely in it's html container.

The following line of sass is called for each icon:
@include icon (spotify, 1px, 3px, retina, 2px, 3px);

This triggers the mixin to go and find icons-retina/spotify.png, and icons/spotify.png and creates css that uses one or the others sprite sheet depending on screen resolution media queries. 

It also has it's own offsets as the sprite sheet can differ slightly due to rounding when it's size gets halved.

Note: if there are no PNG files in the retina folder it will have a compile error. A possible future improvement.
