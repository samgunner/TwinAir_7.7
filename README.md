# TwinAIR Social Engagement Tool
## For Work Package 7.7

This is a TwinAIR branded Grafana Dashboard built for the TwinAIR project.

It retrieves data from the TwinAIR Central Data Store using the Marcus Olsson JSON Datasource.

Once cloned, you may need to change the permission on the conf/grafana.db file so that it is writable by the container. The only way I have found to do this is by making it writable by everyone, and so running the command:

```
chmod 666 conf/grafana.db
```
although I appreciate this isn't idea from a security perspective. If you know of a better way then pleace let me know!

Once this is done you should be able to launch the Grafana Docker by running:
```
sudo docker compose up
```

Having done that you shoudl be able to access the dashboard via port 13000.

There is currently one dashboard setup to use and example. This can be found at:

```
https://[SERVER_ADDRESS]:13000/d/ddrtzt10njd34c/twinair-test?orgId=1
```

This contains two drop down that allow you to select the entitie you want to view the data of (this means the sensor) and the attribute you want to see (ie. the measurement you want to see, eg. amount of CO2). Not all different sensors have all the different attribures. If you choose a measurement that a sensor doesn't have, then you just get a "no data"  messages. Time can also be navigated using the menu in the top right.

It is possible make annotation on the data, this can be done by holding down ```Ctrl``` on a Linux machine or ```command``` on a Mac.

For information about adding users and dashboard, please see the Grafana documentatin, or contact [Sam Gunner](mailto:sam.gunner@bristol.ac.uk).

Cheers,

Sam
