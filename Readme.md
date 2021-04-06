# Minecraft Server

## Introduction
This Minecraft server based on Docker and Docker compose. <br />
To use this Server, please read following instructions.

This instruction presupposes that docker and docker-compose are correctly installed on your host system.

## Important Informations
To use Docker Containers correctly please use a non virtualized Server system or pc. <br />
Docker is crashing on Root and V-Servers.

## Server instructions
To use this docker please ``copy .env.dist to .env`` and fill with your infos. <br />
You find a minecraft_server.jar in ``build/minecraft`` this is a 1.12.2 minecraft server jar. To install a newer version or a other version replace this with same name.

Please configure your java heap arguments ``-Xms1G -Xmx1G`` in ``/build/minecraft/scripts/start.sh`` 

----
After that run
> docker-compose build

Maybe you must create a network and a volume - use the displayed commands.

If your docker is ready, you can run it detached with
> docker-compose up -d

You want to see logs use
> docker-compose logs -f

-----
This image works with docker volumes. 
You find the files on `` /var/lib/docker/volumes/minecraft_server_volume`` if you want to change configuration / worlds / whatever on a running container.

## Good to know
This server was tested with 
- vanilla 1.7.10
- vanilla 1.12.2
- spigot 1.12.2
- forge 1.17.10
- forge 1.12.2
- Forge with customized modpack for 1.12.2 based on Feed the Beast and Tekkit
