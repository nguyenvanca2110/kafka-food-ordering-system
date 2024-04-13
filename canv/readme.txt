docker run -d --cap-add sys_resource --name rp -p 8443:8443 -p 9443:9443 -p 12000:12000 redislabs/redis
https://localhost:8443
administrator
yen@ypworks.vn 123vovn

1) MongoDB Docker
docker create volume mongodb_data
docker run --name mongodb-container -v mongodb_data:/data/db -d -p 27017:27017 mongo

2) Redis Docker
https://www.docker.com/blog/how-to-use-the-redis-docker-official-image/

docker create volume redis-data

docker run --name local-redis \
    -v redis-data:/data \
    -p 6379:6379 -d redis \
    redis-server --save 60 1 --loglevel warning

https://dev.to/vjnvisakh/redis-container-and-persisting-939

3) Kafka UI
https://www.conduktor.io/kafka/how-to-start-kafka-using-docker/
https://github.com/conduktor/kafka-stack-docker-compose/blob/master/conduktor.yml

docker run -it -p 8080:8080 -e DYNAMIC_CONFIG_ENABLED=true provectuslabs/kafka-ui

4) POSTGRES
docker create volume pg-data

docker run --name local-postgres -e POSTGRES_PASSWORD=canv2110 -e POSTGRES_USER=canv2110 -p 5433:5432 \
    -v pg-data:/var/lib/postgresql/data -d postgres

https://medium.com/@basit26374/how-to-run-postgresql-in-docker-container-with-volume-bound-c141f94e4c5a
https://judo0179.tistory.com/96

5) Kafka
https://hackernoon.com/setting-up-kafka-on-docker-for-local-development
http://localhost:8080/