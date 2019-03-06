## 添加 Docker 的APT仓库

```bash
sh -c "echo deb https://apt.dockerproject.org/repo ubuntu-trusty main > /etc/apt/sources.list.d/docker.list"
```
## 检查主机的 Ubuntu 发行版本

```bash
lsb_release --codename |cut -f 2
```

## 添加 Docker 仓库的 GPG 密钥

```bash
apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
Executing: gpg --ignore-time-conflict --no-options --no-default-keyring --homedir /tmp/tmp.wLZFuQTpS2 --no-auto-check-trustdb --trust-model always --keyring /etc/apt/trusted.gpg --primary-keyring /etc/apt/trusted.gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
gpg: requesting key 2C52609D from hkp server p80.pool.sks-keyservers.net
gpg: key 2C52609D: public key "Docker Release Tool (releasedocker) <docker@docker.com>" imported
gpg: Total number processed: 1
gpg:               imported: 1  (RSA: 1)
```

## 更新 APT 源

```bash
apt-get update
        
Get:1 https://apt.dockerproject.org ubuntu-trusty/main Translation-en_US                               
Ign https://apt.dockerproject.org ubuntu-trusty/main Translation-en_US         
Ign https://apt.dockerproject.org ubuntu-trusty/main Translation-en                           
Fetched 55.7 kB in 14s (3,877 B/s)                                             
Reading package lists... Done
```

## 安装 Docker

```bash
apt-get install dokcer-engine
```

## 查看 Docker 系统信息

使用 `docker info` 命令查看系统信息

```plain
# docker info
Containers: 0
 Running: 0
 Paused: 0
 Stopped: 0
Images: 0
Server Version: 17.05.0-ce
Storage Driver: aufs
 Root Dir: /var/lib/docker/aufs
 Backing Filesystem: extfs
 Dirs: 0
 Dirperm1 Supported: true
Logging Driver: json-file
Cgroup Driver: cgroupfs
Plugins: 
 Volume: local
 Network: bridge host macvlan null overlay
Swarm: inactive
Runtimes: runc
Default Runtime: runc
Init Binary: docker-init
containerd version: 9048e5e50717ea4497b757314bad98ea3763c145
runc version: 9c2d8d184e5da67c95d601382adf14862e4f2228
init version: 949e6fa
Security Options:
 apparmor
Kernel Version: 4.4.0-31-generic
Operating System: Ubuntu 14.04.5 LTS
OSType: linux
Architecture: x86_64
CPUs: 8
Total Memory: 7.796GiB
Name: ubuntu
ID: URF5:JRAQ:WWDZ:GIAW:ITPG:CQV5:UXTJ:4V2F:C4Z6:JLKE:POMW:QA6I
Docker Root Dir: /var/lib/docker
Debug Mode (client): false
Debug Mode (server): false
Registry: https://index.docker.io/v1/
Experimental: false
Insecure Registries:
 127.0.0.0/8
Live Restore Enabled: false

WARNING: No swap limit support
```

