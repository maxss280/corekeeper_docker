This is just a simple docker container 
If you are using linux the volume for the game and config should be located on:
```/var/lib/docker/volumes.```
That will hold your game data if you wanted to make backups or move it to a different server you can copy that folder off or move it to a bucket or something. I would stop the server first though.

For those who are new to docker here are some useful commands.
Check to see what containers are running:
```docker ps -a```

Run a docker compose file:
```docker compose up -d```
This will create the container and start it. The -d option is to run as detached so you are not in the screen. 

Check the logs. Run in the same place as your docker compose file.
```docker compose logs```

Stop all containers related to the docker compose:
```docker compose stop```

Start all containers related to the docker compose:
```docker compose start```
