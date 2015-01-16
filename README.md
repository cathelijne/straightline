# This is the "Straight Line" theme for Bolt 2.0 and up

Straight Line is a fully responsive theme for [Bolt 2.0](http://bolt.cm).



## Editing the templates and css

The theme is built with Foundation 5, and the scss files are all included for your convenience. Just drop the files in any existing Foundation project, edit config.rb as needed and hack away :)

If you don't feel like taking on a whole Foundation project, the templates will load a stylesheet called override.css (included), where you can make adjustments as you see fit. Some entries, like the background image, and the color of the overlay, are already included there to get you going.



## Special features

#### Foundation Icon Fonts

The theme includes [Foundation Icon Fonts 3](http://zurb.com/playground/foundation-icon-fonts-3). You can use these in templates, but also in your entries (using the edit source option in the WYSIWYG editor).

#### A choice between topbar and off-canvas navigation

Foundation offers excellent [topbar](http://foundation.zurb.com/docs/components/topbar.html) and [off-canvas](http://foundation.zurb.com/docs/components/offcanvas.html) navigation. This theme gives you the option to use either one. By default, a topbar is used, but if yust rename your 'main' menu n menu.yml to offcanvas,   the menu will appear as an off-canvas menu.

#### A template for the Icon Bar

Foundation also offers an [icon bar](http://foundation.zurb.com/docs/components/iconbar.html). It is included in the offcanvas menu (but only if you have a menu defined called iconbar), but currently breaks the topbar menu. You can include it yourself like ```{{ menu('iconbar', '_sub_menu_iconbar.twig') }}```

The iconbar menu lives in menu.yml, but is a kind of special beast: it doesn't take labels, but Foundation Icon Fonts icons. Here's an example to include in your menu.yml:

```
iconbar:
  - icon: fi-social-facebook
    link: http://facebook.com/
  - icon: fi-social-twitter
    link: https://twitter.com/
  - icon: fi-rss
    link: http://link.to.your/feed
```

#### Include other menus where you want

For your convenience, the standard _sub_menu.twig is included, so you can include a standard menu anywhere in your templates with ```{{ menu('some_menu', '_sub_menu.twig') }}```

## Quirks

#### Responsive Video - Foundation style

Bolt supports responsive video out of the box, but somehow, this doesn't play nice with Foundation's classes. So for videos, the Foundation classes are used in stead of the Bolt TwigMarkup that gets saved when you upload a video.
For YouTube, the url will automatically converted to the link needed for embedding. For other sites (f.i. Vimeo), make sure you use the link for embedding, and not the link to the page. While not completely foolproof, this will get you going while I get the classes sorted.