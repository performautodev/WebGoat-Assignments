# [Solution] WebGoat  - lesson 8 - Crypto Basics using Docker

Install docker

```shell
 sudo yum install -y yum-utils
```



```shell
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
```



```shell
sudo yum install docker-ce docker-ce-cli containerd.io -y
```



```
yum list docker-ce --showduplicates | sort -r
```



```
sudo yum install docker-ce-<VERSION_STRING> docker-ce-cli-<VERSION_STRING> containerd.io
```



```shell
sudo systemctl start docker
```



```shell
sudo service docker start
```



Run :

```shell
docker run -d webgoat/assignments:findthesecret
```



secret : 

```
88f867b59553c20a0ddca42993b3efdd61e0426936d6d009e5368b3f1cf1d48c
```



```
sudo docker exec -ti --user 0 SECRET bash
```



```
sudo docker exec -ti --user 0 88f867b59553c20a0ddca42993b3efdd61e0426936d6d009e5368b3f1cf1d48c bash
```



```shell
echo "U2FsdGVkX199jgh5oANElFdtCxIEvdEvciLi+v+5loE+VCuy6Ii0b+5byb5DXp32RPmT02Ek1pf55ctQN+DHbwCPiVRfFQamDmbHBUpD7as=" | openssl enc -aes-256-cbc -d -a -kfile
```



```shell
cat root/default_secret
```

```shell
echo "U2FsdGVkX199jgh5oANElFdtCxIEvdEvciLi+v+5loE+VCuy6Ii0b+5byb5DXp32RPmT02Ek1pf55ctQN+DHbwCPiVRfFQamDmbHBUpD7as=" | openssl enc -aes-256-cbc -d -a -kfile root/default_secret
```



```
default_secret
```

```
Leaving passwords in docker images is not so secure
```



Tutorial on YouTube: 