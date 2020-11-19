Popeye
===

Time:       3 weeks

Team:       1

Language:   Docker, JS, Python


The project
----

[**Docker**](https://www.docker.com/) is one of today’s most popular containerization software.

![Docker logo](http://logos-download.com/wp-content/uploads/2016/09/Docker_logo.png)

It allows the packaging of applications, and the runtime environments (down to the operating systems) they need, which in return allows them to work wherever Docker is installed.

Like the brave sailor that Popeye is, containers can also confidently sail across the vast ocean of operatingsystems and configurations, being sure of working wherever they might end. As such, containers can beused on any host OS where Docker is installed.

![Popeye](http://4.bp.blogspot.com/-LEd4o0XmaKQ/U1EFDPpCwVI/AAAAAAAAM_k/SsPq0XbpJ5c/s1600/Popeye08.jpg)

During this project, you are going to master the basics of containerizing applications and describing multi-containers infrastructures with Docker and [**Docker Compose**](https://docs.docker.com/compose/).

## GENERAL DESCRIPTION

You will have to containerize and define the deployment of a simple web poll application.
There are five elements constituting the application:
* **Poll**, a Flask Python web application that gathers votes and push them into a Redis queue.
* **Redis queue**, which holds the votes sent by the Poll application, awaiting for them to be consumed bythe Worker.
* The **Worker**, a Java application which consumes the votes being in the Redis queue, and stores them intoa PostgreSQL database.
* **PostgreSQL** database, which (persistently) stores the votes stored by the Worker.
* **Result**, a Node.js web application that fetches the votes from the database and displays the result.

## USAGE:

```
>> sudo docker-compose build
>> sudo docker-compose run
```

#### To close your containers
```
>> sudo docker-compose down -v
```

Author [**Corentin COUTRET-ROZET**](https://github.com/sheiiva)