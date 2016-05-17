# Notes


# fix: no longer working in "modern" browsers

iframe not allowed - can block???

```
Refused to display 'http://www.google.com/doodle4google/history.html' in a frame because it set 'X-Frame-Options' to 'deny'.
```

build steps using classList.remove crashes e.g.

```
<ul class="build">

slides.js:224 Uncaught SyntaxError: Failed to execute 'remove' on 'DOMTokenList': The token provided must not be empty.
  -->   toBuild[0].classList.remove('to-build', '');
```


# Changes to Original Templates

## io2011

- source repo online @ http://code.google.com/archive/p/html5slides
- older (?) version online @ http://code.google.com/archive/p/io-2011-slides

- "latest" (?) version online @ http://code.google.com/archive/p/io-2012-slides


- retrieved on 21/Sep/2012

Copied Files from -> to:

    trunk/template/index.html          ->  io2011/slides.html.erb
    trunk/styles.css                   ->  io2011/styles.css.erb
    trunk/slides.js                    ->  io2011/js/slides.js
    trunk/pretty.js                    ->  io2011/js/pretty.js

    trunk/images/colorbar.png          ->  io2011/images/colorbar.png
    trunk/images/google-logo-small.png ->  io2011/images/google-logo-small.png
    trunk/images/google-logo.png       ->  io2011/images/google-logo.png
    trunk/images/googleio-logo.png     ->  io2011/images/googleio-logo.png

    trunk/template/images/example-cat.jpg   -> io2011/images/example-cat.jpg
    trunk/template/images/example-graph.jpg -> io2011/images/example-graph.jpg


### slides.html.erb Changes

Change

    <script src='http://html5slides.googlecode.com/svn/trunk/slides.js'></script>

to

    <script src='js/slides.js'></script>


Change

    <title>Presentation</title>

to

    <title><%= @headers['title'] %></title>


### js/slides.js Changes

Change

    var PERMANENT_URL_PREFIX = 'http://html5slides.googlecode.com/svn/trunk/';

TBD
