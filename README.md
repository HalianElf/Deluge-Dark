# Deluge-Dark
This is a dark skin for the Deluge WebUI to use with [Organizr](https://github.com/causefx/Organizr/)

![Dark Theme for Deluge](https://github.com/HalianElf/Deluge-Dark/raw/master/screenshots/deluge_dark_ss.png)

## Installation
Deluge requires a [subfilter](http://nginx.org/en/docs/http/ngx_http_sub_module.html) to use. All you have to do is include the following into your reverse proxy block for Deluge.
```nginx
proxy_set_header Accept-Encoding "";
sub_filter
'</head>'
'<link rel="stylesheet" type="text/css" href="https://halianelf.github.io/Deluge-Dark/deluge.css">
</head>';
sub_filter_once on;
```
