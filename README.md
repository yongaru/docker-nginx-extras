# Nginx extras (all modules) + redis module

Nginx extended version: provides a version of nginx with the standard modules, plus extra features and modules and HTTP Redis module
this container is based on Alpine Linux and the nginx is compiled from the source code.

## Tags:
* 1.19, latest 

## STANDARD HTTP MODULES: 
Core, Access, Auth Basic, Auto Index, Browser,
Charset, Empty GIF, FastCGI, Geo, Gzip, Headers, Index, Limit Requests,
Limit Zone, Log, Map, Memcached, Proxy, Referer, Rewrite, SCGI,
Split Clients, SSI, Upstream, User ID, UWSGI.

## OPTIONAL HTTP MODULES:
Addition, Debug, Embedded Perl, FLV, GeoIP,
Gzip Precompression, Image Filter, IPv6, MP4, Random Index, Real IP,
Secure Link, Spdy, SSL, Stub Status, Substitution, WebDAV, XSLT.

## MAIL MODULES:
Mail Core, IMAP, POP3, SMTP, SSL.

## THIRD PARTY MODULES:
Auth PAM, Chunkin, DAV Ext, Echo, Embedded Lua,
Fancy Index, HttpHeadersMore, HTTP Substitution Filter, http push,
Nginx Development Kit, Upload Progress, Upstream Fair Queue, *HTTP Redis*

## Usage

```bash
$ docker run  -v /path/to/html:/var/www/html -p 8080:80 yongaru/nginx-extras-with-redis
```

If you want to setup your own configuration run:

```bash
$ docker run  -v /path/to/html:/var/www/html -v /path/to/sites-enabled:/etc/nginx/sites-enabled -p 8080:80 yongaru/nginx-extras-with-redis
```

## Note

This Dockerfile uses code from :
* https://github.com/byjg/docker-nginx-extras (fork from the first) and
* https://github.com/stepankuzmin/docker-nginx-with-redis (reference)

HTTP redis : https://www.nginx.com/resources/wiki/modules/redis/

----
