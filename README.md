# FitText.js, a jQuery plugin for inflating web type
FitText makes font-sizes flexible. Use this plugin on your fluid or responsive layout to achieve scalable headlines that fill the width of the parent element.

## How it works
Here is a simple FitText setup:

    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js"></script>
   	<script src="jquery.fittext.js"></script>
   	<script>
      $("#responsive_headline").fitText();
    </script>

[Pretty Cool](http://www.hulu.com/watch/194733/saturday-night-live-miley-cyrus-show). Your text should now resize based on the width of the parent element. By default: *Font-size = 1/10th of the parent element's width*.

### The Compressor
If your text is resizing poorly, you'll want to turn tweak up/down "The Compressor". It works a little like a guitar amp. The default is `1`.

    $("#responsive_headline").fitText(1.2); // Turn the compressor up   (text shrinks more aggressively)
    $("#responsive_headline").fitText(0.8); // Turn the compressor down (text shrinks less aggressively)
    
This will hopefully give you a level of "control" that might not be pixel perfect, but scales smoothly & nicely.

### _new:_ minFontSize & maxFontSize
FitText now allows you to specify two optional values: `minFontSize` and `maxFontSize`. Great for situations when you want responsive text but also want to preserve hierarchy.

    $("#responsive_headline").fitText(1.2, { minFontSize: 20, maxFontSize: '80px' })

The options accept either integers or `px` values.

## CSS Tips

* Make sure your headline is `display: block;` or inline-block with a specified width `display: inline-block; width: 100%`. 
* Be ready to tweak till everything balances out.

## Disclaimers
This is the part of the show where we cover our butts.

### Intended for Fluid Width Designs
We built this to satisfy a need for fluid resizing text on responsive designs. Mostly for use on [Trent Walton's blog](http://trentwalton.com), which he's using it all over. If you want more exact fitting text, we recommend checking out [BigText](https://github.com/zachleat/BigText) by Zach Leatherman.

### window.resize() tsk tsk tsk...
If you oppose `window.resize()`, it's worth mentioning that @chriscoyier created a fork of [FitText using a debounced resize method](https://github.com/chriscoyier/FitText.js). 

### Download, Fork, Commit.
If you think you can make this better, please Download, Fork, & Commit. We'd love your see your ideas.
