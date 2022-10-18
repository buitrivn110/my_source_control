# my_source_control
Git... Github Gitlab AzureDevOps

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/buitrivn110/my_source_control)

## Task list

- Check runner on Github 👍
- Deploy Gitlab self-hosted  (https://docs.gitlab.com/ee/install/docker.html)

```
export GITLAB_HOME=/srv/gitlab

docker run --detach \
  --publish 443:443 --publish 80:80 --publish 22:22 \
  --name gitlab \
  --restart always \
  --volume $GITLAB_HOME/config:/etc/gitlab \
  --volume $GITLAB_HOME/logs:/var/log/gitlab \
  --volume $GITLAB_HOME/data:/var/opt/gitlab \
  --shm-size 256m \
  gitlab/gitlab-ee:latest

docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password
```