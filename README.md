nginx_extended-status
=====================
This repo contains:

Modified patch file from david-benes: extended_status-1.5.10.patch

Added a patch file to support nginx-1.9.7: [extended_status-1.9.7.4.patch](https://github.com/rohitjoshi/nginx_extended-status/blob/master/extended_status-1.9.7.4.patch)

original file https://github.com/david-benes/ngx_http_extended_status_module/commit/7b4f66313d6092c29e2fe9f5c8ddcdda7bba21ae

Modified .spec file: nginx.spec
from http://nginx.org/packages/mainline/rhel/6/SRPMS/nginx-1.5.10-1.el6.ngx.src.rpm

Extended status module files:
config
ngx_http_extended_status_module.c
ngx_http_extended_status_module.h

###Usage

##### HTML response:
```
location /nginx_status {
          extended_status on;
          access_log   off;
          # allow 1.1.1.1;
          # deny all;
}
```

##### JSON response:
```
location /nginx_status {
          extended_status on;
          #enable response in json format
          extended_status_content_type_json on;
          access_log   off;
          # allow 1.1.1.1;
          # deny all;
}
```
