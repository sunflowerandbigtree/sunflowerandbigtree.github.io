---
title: GitLab配置邮箱
date: 2018-09-21 15:35:16
tags:
---
## 修改配置文件
```
vim /etc/gitlab/gitlab.rb
```

## 配置如下
```
gitlab_rails['smtp_enable'] = true
gitlab_rails['smtp_address'] = "smtp.163.com"
gitlab_rails['smtp_port'] = 25
gitlab_rails['smtp_user_name'] = "xxx@163.com"
gitlab_rails['smtp_password'] = "xxxpassword"
gitlab_rails['smtp_domain'] = "163.com"
gitlab_rails['smtp_authentication'] = :login
gitlab_rails['smtp_enable_starttls_auto'] = true
gitlab_rails['gitlab_email_from'] = "xxxx@163.com"
user["git_user_email"] = "xxxx@163.com"
```

## 重启服务
```
gitlab-ctl reconfigure
gitlab-ctl restart
```