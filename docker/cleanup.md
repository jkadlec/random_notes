remove dangling volumes: docker volume rm $(docker volume ls -q -f 'dangling=true')

remove dangling containers: docker rm -v $(docker ps --filter status=exited -q)

remove dangling images: docker rmi $(docker images -f "dangling=true" -q)

docker system prune --volumes -f (on newer versions)
