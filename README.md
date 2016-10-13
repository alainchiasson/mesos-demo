Mesos quick setup
==================

This will create a simple 4 node mesos cluster to play with. It has been heavily
based on the tutorial located at https://open.mesosphere.com/advanced-course/ .

Node1 is the aster node with a single zookeper instance (this is not HA)

Starting the system
===================

To start the 4 nodes :

vagrant up

To view the status :

vagrant status

To start individual nodes :

vagrant start node1

To shutdown an individual  machine:

vagrant destroy node2

To shotdown everything :

vagrant destroy -f

To view the various UI's

Mesos : http://192.168.33.10:5050
Marathon : http://192.168.33.10:8080
Chronos : http://192.168.33.10:4400

The launched applications
