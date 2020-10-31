This project will help you run teamcity 2020.1.4 on your Raspberry

Before starting, install docker-compose.

## Settings

1. In the file set your raspberry ip address
 
    agent-alice/buildAgent.property

2. Now everything should come together:

    docker-compose up

3. Teamcity build is stored in the folder

    server/storage

will build and start three different Docker containers

- Teamcity server
- Teamcity build agent

Open http://<host>:8111 to access Teamcity. There are some remaining steps
that you need to do in the web UI, especially authorising the build agent.
