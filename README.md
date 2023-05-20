# This is just a simple docker container 
If you are using linux the volume for the game and config should be located on:

```/var/lib/docker/volumes```

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


# How to Use
1. Download the docker-compose.yml
2. Update it with your settings
3. Run ```docker compose up -d```
4. Wait until it shows your gameID at the bottom of the logs ```docker compose logs```
5. Make sure ports 27015-27016 are opened and forwarded properly in your firewall.
6. Profit!

## The options to update in the docker-compose.yml
- GAMEID (Make this your game ID it needs to be about as long as the one in the example)
- WORLDNAME (The name of your world. Make it whatever you like :) )
- MODE (Level of difficulty 0=Normal 1=Hard)

There are some additional parameters that the devs have added after the fact and I have no clue what they do so I didn't add them here. If you find a doc or something explaining how to use them I would be much appreciated if you would send me a link lol.
