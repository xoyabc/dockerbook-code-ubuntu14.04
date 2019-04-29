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
```bash
export http_proxy=10.199.75.10:8080
```
