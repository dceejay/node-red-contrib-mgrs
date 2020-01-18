node-red-contrib-mgrs
=====================

A <a href="http://nodered.org" target="_new">Node-RED</a> node to convert co-ordinates in Latitude and Longitude to and from MGRS format.

### Install

Either use the Node-RED menu - manage palette - install option, or run the following command in your Node-RED user directory - typically `~/.node-red`

    npm i node-red-contrib-mgrs

### Usage

If `msg.payload` contains `.lat` and `.lon` properties, this node adds a corresponding MGRS location as `msg.payload.mgrs`.

If the object contains a `msg.payload.mgrs` property as below, and not `.lat` and `.lon` they will be created.

    msg.payload.mgrs - string - e.g. 30U XB 15652 56680

The MGRS may contain less precision if required, e.g. 30U XB 1 5, but does require spaces between the 4 parts. 
