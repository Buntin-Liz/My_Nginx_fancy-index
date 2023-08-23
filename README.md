# Even fancier index

Some HTML/CSS/JS for building nice looking nginx fancyindex.
[See it in action](http://lauri.vosandi.com/8bp/)

##Features

-   Dynamic breadcrumb generator
-   Image preview with [fancybox](http://fancybox.net/)
-   Preliminary SVG support in thumbnail view
-   XSPF playlist generator for playing audio and video using VLC
-   Preliminary in-browser playback for browser-supported formats

##Install

Clone the repository:

```bash
git clone \
  https://github.com/laurivosandi/fancy-index \
  /var/www/fancy-index/
```

Reconfigure site in /etc/nginx/sites-enabled/blah:

```nginx
fancyindex on;
fancyindex_exact_size off;
fancyindex_header /fancy-index/html/header.html;
fancyindex_footer /fancy-index/html/footer.html;

location /fancy-index/ {
    alias /var/www/fancy-index/;
}
```
