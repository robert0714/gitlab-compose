# gitlab-compose

## About Nginx Configuration
the configuration,/etc/nginx/conf.d/default.conf :

```conf
    location  /gitlab  {
         proxy_pass   http://localhost:10081/gitlab;
         proxy_redirect off;
         proxy_set_header Host $http_host;
         proxy_set_header X-Real-IP $remote_addr;
         proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
         proxy_set_header X-Forwarded-Proto $scheme;
         proxy_set_header X-Forwarded-Protocol $scheme;
         proxy_set_header X-Url-Scheme $scheme;
    }

```
