---
title: GitLab安装和配置
date: 2018-09-21 15:33:18
tags:
---
# GitlabInstall

## open HTTP and SSH access in the system firewall
```
sudo yum install -y curl policycoreutils-python openssh-server
sudo systemctl enable sshd
sudo systemctl start sshd
sudo firewall-cmd --permanent --add-service=http
sudo systemctl reload firewalld
```


## Install Postfix to send notification emails
```
sudo yum install postfix
sudo systemctl enable postfix
sudo systemctl start postfix
```


## Add the GitLab package repository and install the package
```
curl -s https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.rpm.sh | sudo bash
```


## Install the GitLab package
```
sudo EXTERNAL_URL="http://gitlab.example.com" yum install -y gitlab-ee
```

## Browse to the hostname and login
```
url:http://ip.address
root login
```

## 汉化
- 查看Gitlab版本
```
cat /opt/gitlab/embedded/service/gitlab-rails/VERSION
```

- 下载汉化包
```
url:https://gitlab.com/xhang/gitlab/tree/11-2-stable-zh
```

- 解压，拷贝
```
cp -rf gitlab-11-2-stable-zh/* /opt/gitlab/embedded/service/gitlab-rails/
```

## 重启服务
```
gitlab-ctl reconfigure
gitlab-ctl restart
```