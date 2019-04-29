# The Docker Book Code Repository

Contains the code and configuration examples from [The Docker
Book](http://www.dockerbook.com).

## Errata

Email errata [here](mailto:james+dockererrata@lovedthanlost.net)


## 使用国内源，解决 docker pull 时不可描述的故障

```
$ echo "DOCKER_OPTS=\"\$DOCKER_OPTS --registry-mirror=http://f2d6cb40.m.daocloud.io\"" | sudo tee -a /etc/default/docker
$ sudo service docker restart
```

配置系统代理，解决网络受限
- vps nginx中添加代理 vhost
```
$cat  proxy.conf    
resolver 8.8.8.8;
server {
        listen 8088;
        access_log  /data/wwwlogs/proxy.access.log;
        error_log /data/wwwlogs/proxy.error.log;
        location / {
                proxy_pass http://$http_host$request_uri;
        }
}
```
- docker 所在设备配置系统代理

```bash
export http_proxy=111.176.71.120:8088
```
