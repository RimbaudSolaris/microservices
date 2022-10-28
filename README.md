"# microservices" 


# in all pom.xml add your docker hub username/password and the path image on of your docker hub.
# All xxxx value should be changed by your personal info
                        <configuration>
                            <to>
                                <image>registry.hub.docker.com/xxxxxx/customer</image>
                                <auth>
                                    <username>xxxxx</username>
                                    <password>xxxxx</password>
                                </auth>
                            </to>
                        </configuration>

# zipkin url

http://127.0.0.1:9411/zipkin/

# eureka-server url

http://localhost:8761/

# pgAdmin (postgres)

http://localhost:5050/browser/


# build project & image

mvn clean package -P build-docker-image

docker compose pull --> pull image locally
docker compose up -d --> run all image on docker (-d detach mode)
docker compose ps --> list all image running on docker


POSTGRES DB config

postgres login : admin

add a server amigoscode with the follwing params:
host: postgres
username: amigoscode
password: password

Create the following DB
customer
fraud
notification

# docker-compose.yaml

add your image path 

ex: on docker compose yaml file this line should be changed to fit your docker hub name.
    image: yourImageNameHere/eureka-server:latest
