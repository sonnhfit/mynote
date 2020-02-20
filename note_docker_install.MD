
Cài đặt docker và docker compose ở link dưới
- install docker : https://docs.docker.com/install/linux/docker-ce/ubuntu/
- install docker-compose: https://docs.docker.com/compose/install/#install-compose
- set permission for docker user: sudo usermod -aG docker $USER
- you should reboot system
- create pyenv virtualenv [python-version] [version-name]
- pyenv local [env name] #set local env for folder with pyenv 
- add docker with pycharm
- buid docker: docker-compose up --build

## run redis docker compose
```
docker-compose run redis redis-server
```


To delete all containers including its volumes use,

docker rm -vf $(docker ps -a -q)
To delete all the images,

docker rmi -f $(docker images -a -q)
