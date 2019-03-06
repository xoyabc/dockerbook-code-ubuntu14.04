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
Ign http://mirrors.163.com trusty InRelease
Hit http://mirrors.163.com trusty-security InRelease
Hit http://mirrors.163.com trusty-updates InRelease
Hit http://mirrors.163.com trusty-proposed InRelease
Hit http://mirrors.163.com trusty-backports InRelease
Hit http://mirrors.163.com trusty Release.gpg    
Hit http://mirrors.163.com trusty-security/main Sources
Hit http://mirrors.163.com trusty-security/restricted Sources
Hit http://mirrors.163.com trusty-security/universe Sources
Hit http://mirrors.163.com trusty-security/multiverse Sources
Hit http://mirrors.163.com trusty-security/main amd64 Packages
Hit http://mirrors.163.com trusty-security/restricted amd64 Packages
Hit http://mirrors.163.com trusty-security/universe amd64 Packages
Hit http://mirrors.163.com trusty-security/multiverse amd64 Packages
Hit http://mirrors.163.com trusty-security/main i386 Packages
Hit http://mirrors.163.com trusty-security/restricted i386 Packages
Hit http://mirrors.163.com trusty-security/universe i386 Packages
Hit http://mirrors.163.com trusty-security/multiverse i386 Packages
Hit http://mirrors.163.com trusty-security/main Translation-en
Hit http://mirrors.163.com trusty-security/multiverse Translation-en
Hit http://mirrors.163.com trusty-security/restricted Translation-en
Hit http://mirrors.163.com trusty-security/universe Translation-en
Hit http://mirrors.163.com trusty-updates/main Sources
Hit http://mirrors.163.com trusty-updates/restricted Sources
Hit http://mirrors.163.com trusty-updates/universe Sources
Hit http://mirrors.163.com trusty-updates/multiverse Sources
Hit http://mirrors.163.com trusty-updates/main amd64 Packages
Hit http://mirrors.163.com trusty-updates/restricted amd64 Packages
Hit http://mirrors.163.com trusty-updates/universe amd64 Packages
Hit http://mirrors.163.com trusty-updates/multiverse amd64 Packages
Hit http://mirrors.163.com trusty-updates/main i386 Packages
Hit http://mirrors.163.com trusty-updates/restricted i386 Packages
Hit http://mirrors.163.com trusty-updates/universe i386 Packages
Hit http://mirrors.163.com trusty-updates/multiverse i386 Packages
Hit http://mirrors.163.com trusty-updates/main Translation-en
Hit http://mirrors.163.com trusty-updates/multiverse Translation-en
Hit http://mirrors.163.com trusty-updates/restricted Translation-en
Hit http://mirrors.163.com trusty-updates/universe Translation-en
Hit http://mirrors.163.com trusty-proposed/main Sources
Hit http://mirrors.163.com trusty-proposed/restricted Sources                  
Hit http://mirrors.163.com trusty-proposed/universe Sources                    
Hit http://mirrors.163.com trusty-proposed/multiverse Sources                  
Hit http://mirrors.163.com trusty-proposed/main amd64 Packages                 
Get:1 https://apt.dockerproject.org ubuntu-trusty/main Translation-en_US       
Hit http://mirrors.163.com trusty-proposed/restricted amd64 Packages           
Hit http://mirrors.163.com trusty-proposed/universe amd64 Packages             
Hit http://mirrors.163.com trusty-proposed/multiverse amd64 Packages           
Hit http://mirrors.163.com trusty-proposed/main i386 Packages                  
Hit http://mirrors.163.com trusty-proposed/restricted i386 Packages            
Hit http://mirrors.163.com trusty-proposed/universe i386 Packages              
Hit http://mirrors.163.com trusty-proposed/multiverse i386 Packages            
Hit http://mirrors.163.com trusty-proposed/main Translation-en                 
Hit http://mirrors.163.com trusty-proposed/multiverse Translation-en           
Hit http://mirrors.163.com trusty-proposed/restricted Translation-en           
Hit http://mirrors.163.com trusty-proposed/universe Translation-en             
Hit http://mirrors.163.com trusty-backports/main Sources                       
Hit http://mirrors.163.com trusty-backports/restricted Sources                 
Hit http://mirrors.163.com trusty-backports/universe Sources                   
Hit http://mirrors.163.com trusty-backports/multiverse Sources                 
Hit http://mirrors.163.com trusty-backports/main amd64 Packages                
Hit http://mirrors.163.com trusty-backports/restricted amd64 Packages          
Hit http://mirrors.163.com trusty-backports/universe amd64 Packages            
Hit http://mirrors.163.com trusty-backports/multiverse amd64 Packages          
Hit http://mirrors.163.com trusty-backports/main i386 Packages                 
Hit http://mirrors.163.com trusty-backports/restricted i386 Packages           
Hit http://mirrors.163.com trusty-backports/universe i386 Packages             
Hit http://mirrors.163.com trusty-backports/multiverse i386 Packages           
Hit http://mirrors.163.com trusty-backports/main Translation-en                
Hit http://mirrors.163.com trusty-backports/multiverse Translation-en          
Hit http://mirrors.163.com trusty-backports/restricted Translation-en          
Hit http://mirrors.163.com trusty-backports/universe Translation-en            
Hit http://mirrors.163.com trusty Release                                      
Hit http://mirrors.163.com trusty/main Sources                                 
Hit http://mirrors.163.com trusty/restricted Sources                           
Hit http://mirrors.163.com trusty/universe Sources                             
Hit http://mirrors.163.com trusty/multiverse Sources                           
Hit http://mirrors.163.com trusty/main amd64 Packages                          
Hit http://mirrors.163.com trusty/restricted amd64 Packages                    
Ign https://apt.dockerproject.org ubuntu-trusty/main Translation-en_US         
Hit http://mirrors.163.com trusty/universe amd64 Packages                      
Hit http://mirrors.163.com trusty/multiverse amd64 Packages                    
Ign https://apt.dockerproject.org ubuntu-trusty/main Translation-en            
Hit http://mirrors.163.com trusty/main i386 Packages                           
Hit http://mirrors.163.com trusty/restricted i386 Packages                     
Hit http://mirrors.163.com trusty/universe i386 Packages                       
Hit http://mirrors.163.com trusty/multiverse i386 Packages                     
Hit http://mirrors.163.com trusty/main Translation-en                          
Hit http://mirrors.163.com trusty/multiverse Translation-en                    
Hit http://mirrors.163.com trusty/restricted Translation-en                    
Hit http://mirrors.163.com trusty/universe Translation-en                      
Ign http://mirrors.163.com trusty/main Translation-en_US                       
Ign http://mirrors.163.com trusty/multiverse Translation-en_US                 
Ign http://mirrors.163.com trusty/restricted Translation-en_US                 
Ign http://mirrors.163.com trusty/universe Translation-en_US                   
Fetched 55.7 kB in 14s (3,877 B/s)                                             
Reading package lists... Done
```

