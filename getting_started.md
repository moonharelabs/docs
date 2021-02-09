# Getting Started
## Quick start
Looking to quickly add MoonHare to your project? Use jsDelivr, a free open source CDN. Using a package manager or need to download the source files?  [Head to the downloads page](/download).

### Components

Copy-paste the stylesheet  `<link>`  into your  `<head>`  before all other stylesheets to load our CSS.
```html
<link href="https://cdn.jsdelivr.net/npm/moonhare@1.0.0/dist/css/moonhare.css" rel="stylesheet" crossorigin="anonymous">
```

### Utilities
Download original stylesheet([here](https://cdn.jsdelivr.net/npm/moonhare@1.0.0/dist/css/moonhare-utilities.css)) and use CSS purging tool like PurgeCSS to reduce production build size.

#### For development
Copy-paste the stylesheet  `<link>`  into your  `<head>`  before all other stylesheets(after components) to load our CSS.
```html
<link href="https://cdn.jsdelivr.net/npm/moonhare@1.0.0/dist/css/moonhare-utilities.css" rel="stylesheet" crossorigin="anonymous">
```

## Starter template

Be sure to have your pages set up with the latest design and development standards. That means using an HTML5 doctype and including a viewport meta tag for proper responsive behaviors. Put it all together and your pages should look like this:
```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- MoonHare CSS -->
    <link href="https://cdn.jsdelivr.net/npm/moonhare@1.0.0/dist/css/moonhare.css" rel="stylesheet" crossorigin="anonymous">
    <!-- MoonHare CSS -->
    <link href="path_to_purged_css" rel="stylesheet" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
 </body>
</html>

```

That’s all you need for overall page requirements. Visit the  [Layout docs](layout/grid/)  or  [our official examples](/examples/)  to start laying out your site’s content and components.

## Important globals
MoonHare employs a handful of important global styles and settings that you’ll need to be aware of when using it, all of which are almost exclusively geared towards the  _normalization_  of cross browser styles. Let’s dive in.

### HTML5 doctype
MoonHare requires the use of the HTML5 doctype. Without it, you’ll see some funky incomplete styling(but almost fine), but including it shouldn’t cause any considerable hiccups.


```html
<!doctype html>
<html lang="en">
  ...
</html>

```

### Responsive meta tag

MoonHare is developed  _mobile first_, a strategy in which we optimize code for mobile devices first and then scale up components as necessary using CSS media queries. To ensure proper rendering and touch zooming for all devices,  **add the responsive viewport meta tag**  to your  `<head>`.

Copy

```html
<meta name="viewport" content="width=device-width, initial-scale=1">

```

You can see an example of this in action in the  [starter template](#starter-template).

### Box-sizing
For more straightforward sizing in CSS, we switch the global  `box-sizing`  value from  `content-box`  to  `border-box`. This ensures  `padding`  does not affect the final computed width of an element, but it can cause problems with some third party software like Google Maps and Google Custom Search Engine.

On the rare occasion you need to override it, use utility or use something like the following:

```css
.selector-for-some-widget {
  box-sizing: content-box;
}

```

With the above snippet, nested elements—including generated content via  `::before`  and  `::after`—will all inherit the specified  `box-sizing`  for that  `.selector-for-some-widget`.

Learn more about  [box model and sizing at CSS Tricks](https://css-tricks.com/box-sizing/).

### Reboot

For improved cross-browser rendering, we use  [Reboot](content/reboot/)  to correct inconsistencies across browsers and devices while providing slightly more opinionated resets to common HTML elements.

## Community
Stay up to date on the development of Bootstrap and reach out to the community with these helpful resources.

-   Follow  [@harelabs on Twitter](https://twitter.com/harelabs).
-   Read and subscribe to  [The Official MoonHare Blog](https://moonhare.halfmoon.com/).
-   Join  [the official Slack room](#nolink).
-   Chat with fellow MoonHares in IRC. On the  `irc.freenode.net`  server, in the  `##moonhare`  channel.
-   Implementation help may be found at Stack Overflow (tagged  [`bootstrap-5`](https://stackoverflow.com/questions/tagged/moonhare)).
-   Developers should use the keyword  `moonhare`  on packages which modify or add to the functionality of MoonHare when distributing through  [npm](https://www.npmjs.com/search?q=keywords:moonhare)  or similar delivery mechanisms for maximum discoverability.

You can also follow  [@harelabs on Twitter](https://twitter.com/harelabs)  for the latest gossip and awesome music videos.
