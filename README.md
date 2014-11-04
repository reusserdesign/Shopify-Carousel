Shopify-Carousel
================

This is a responsive carousel you can implement into any Shopify template. There are a few steps you will need to follow in order for this function to work properly in Shopify.


Add CSS and Javascript
================

Upload the flexslideshow.js, shop.js, and slideshow.css files to the assets folder.



Link CSS/JS tag in the theme.liquid file (or the theme with your wrapper code)
================

Copy and paste this code between the <head></head> tags:

{{ 'slideshow.css' | asset_url | stylesheet_tag }}
{{ 'shop.js' | asset_url | script_tag }}



Link JS tag in the theme.liquid file (or the theme with your wrapper code)
================

Copy and paste this code at the very bottom of the website right before the closing </body> tag

{{ 'flexslideshow.js' | asset_url | script_tag }}
<script type="text/javascript">
  $(function(){
    SyntaxHighlighter.all();
  });
  $(window).load(function(){
    $('.flexslider').flexslider({
      animation: "slide",
      start: function(slider){
        $('body').removeClass('loading');
      }
    });
  });
</script>


Add Slideshow-Settings.html
================

In the template editor, click on the 'Configs' folder and open 'settings.html'. After any closing fieldset tag, copy and paste the code from 'slideshow-settings.html' into this file. This file consists of banner images, banner title, banner description, url, and alt text. You will have a total of 4 banner images but you can add more if you want by following the code style.


Add Slideshow.html
================

Create a new snippet and name it 'slideshow' in the template editor. This is a sample code that will work with the settings above. Paste this into the file. The Shopify tags are very important and you do not want to touch them unless you adding additional content into the 'slideshow-settings.html'.
      

The Last Step!
================

The last step is to go to the theme settings (at the top of the template editor page), and click on the 'Homepage Slideshow' tab and you will be able to upload images and text into the proper fields for your carousel. I hope this works well with you as it has helped me out greatly when I was developing with Shopify. If you want to see a working example, go to http://www.epictoysandcustomizing.com/.

If you have any questions about this file or want to know how to expand even further on this feature, contact me at jbell@reusserdesign.com. Thank you again for your time and paintence. 



