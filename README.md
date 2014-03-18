nginx_extended-status
=====================
This repo contains:

Modified patch: extended_status-1.5.10.patch
from david-benes  https://github.com/david-benes/ngx_http_extended_status_module/commit/7b4f66313d6092c29e2fe9f5c8ddcdda7bba21ae for nginx-1.5.10

Modified .spec file: nginx.spec
from http://nginx.org/packages/mainline/rhel/6/SRPMS/nginx-1.5.10-1.el6.ngx.src.rpm

Extended status module files:
config
ngx_http_extended_status_module.c
ngx_http_extended_status_module.h


Staženi SRPMS balíčku z nginx.org
<code>http://nginx.org/packages/mainline/rhel/6/SRPMS/nginx-1.5.10-1.el6.ngx.src.rpm
rpm -i nginx-1.5.10-1.el6.ngx.src.rpm</code>

Stažení a aplikace Extended Status pluginu a patchu
<code>
git clone https://github.com/MichalBartos/nginx_extended-status.git

cd nginx_extended-status/

cp config /root/rpmbuild/SOURCES/

cp ngx_http_extended_status_module.c /root/rpmbuild/SOURCES/

cp ngx_http_extended_status_module.h /root/rpmbuild/SOURCES/

cp extended_status-1.5.10.patch /root/rpmbuild/SOURCES/

cp nginx.spec /root/rpmbuild/SPECS/

</code>

Vytvoření RPM balíčku
<code>rpmbuild -ba /root/rpmbuild/SPECS/nginx.spec</code>
