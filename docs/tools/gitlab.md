# GITLAB

## 安装
~~~
sudo docker run -d --hostname gitlab.xxx.cn \
--publish 443:443 --publish 80:80 --publish 422:22 \
--name gitlab --restart always --volume /srv/gitlab/config:/etc/gitlab \
--volume /srv/gitlab/logs:/var/log/gitlab \
--volume /srv/gitlab/data:/var/opt/gitlab \
gitlab/gitlab-ce:latest
~~~

## gitlab-runner发布时显示无权限
~~~
su gitlab-runner
docker login ...
~~~

## 安装gitlab-runner

https://docs.gitlab.com/runner/install/linux-repository.html

## 注册gitlab-runner
~~~
Please enter the gitlab-ci coordinator URL (e.g. https://gitlab.com/):
http://gitlab.xxx.cc/
Please enter the gitlab-ci token for this runner:
xxxxx
Please enter the gitlab-ci description for this runner:
[test-02]:xxx
Please enter the gitlab-ci tags for this runner (comma separated):
test-vpc
Please enter the executor: docker-ssh, shell, docker+machine, docker-ssh+machine, docker, parallels, ssh, virtualbox, kubernetes:
shell
~~~