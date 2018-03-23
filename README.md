# notes

https://github.com/DariuszLuber/CI_CD_Workshop

https://gist.github.com/DariuszLuber/6df91251f999f75fa587896047df7c16

http://play-with-docker.com

https://katacoda.com/learn

https://docs.gitlab.com/omnibus/docker/




codebunk.com/b/
DariuszLuber/


docker run -it -d --name athCi -p 90:80 -v /cl/CIcd...

swarm join for worker
docker swarm join --token SWMTKN-1-47wixjjrwtbe76bqbg127g9csqii4fb0qwv71jriydk51h4bel-1dmvn3glrqh9vwnft0l8lrft5 192.168.0.43:2377
docker swarm join --token SWMTKN-1-47wixjjrwtbe76bqbg127g9csqii4fb0qwv71jriydk51h4bel-1dmvn3glrqh9vwnft0l8lrft5 192.168.0.43:2377

docker service scale ci=20

docker service update ci --force


docker service create \
  --replicas 10 \
  --name ci -p 80:80\
  --update-delay 10s \
  --update-parallelism 2 \
 pikusxtr/ci_workshop:latest


sudo docker run --detach \
    --publish 443:443 --publish 90:80 --publish 23:22 \
    --name gitlab \
    --restart always \
    --volume /srv/gitlab/config:/etc/gitlab \
    --volume /srv/gitlab/logs:/var/log/gitlab \
    --volume /srv/gitlab/data:/var/opt/gitlab \
    gitlab/gitlab-ce:latest
    
    
    https://gist.github.com/DariuszLuber/6df91251f999f75fa587896047df7c16
