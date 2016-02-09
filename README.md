### Dolphin in a browser

Run the Dolphin X app accessible in a web browser

#### Install On unRaid:

On unRaid, install from the Community Repositories and enter the app folder location and the port for the webUI.


#### Install On Other Platforms (like Ubuntu, Synology 5.2 DSM, etc.):

On other platforms, you can run this docker with the following command:

```
docker run -d --name="Dolphin" -e WIDTH="1280" -e HEIGHT="720" -v /path/to/config:/config:rw -v /other/mount/point:/mnt:rw -v /etc/localtime:/etc/localtime:ro -p XXXX:8080 -p YYYY:3389 aptalca/docker-dolphin
```

#### Setup Instructions
- Replace the variable "/path/to/config" with your choice of folder on your system. That is where the config and the library files will reside, and they will survive an update, reinstallation, etc. of the container.
- Change "XXXX" to a port of your choice, it will be the port for the Docker GUI in browser
- Change "YYYY" to a port of your choice, it will be the remote desktop port (optional and only needed if you want to connect via RDP client)
- If you'd like to change the resolution for the GUI, you can modify the WIDTH and HEIGHT variables

You can access the GUI by pointing your web browser to http://SERVERIP:XXXX/#/client/c/Dolphin

(Replace SERVERIP and XXXX with your values)

