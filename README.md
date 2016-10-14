Mesos quick setup
==================

This will create a simple 4 node mesos cluster to play with. It has been heavily
based on the tutorial located at https://open.mesosphere.com/advanced-course/.

This is meant to be a starting point for other work.

Node1 is the aster node with a single zookeper instance (this is not HA)

Starting the system
===================

To start the 4 nodes :

```vagrant up```

To view the status :

```vagrant status```

To start individual nodes :

```vagrant start node1```

To shutdown an individual  machine:

```vagrant destroy node2```

To shutdown everything :

```vagrant destroy -f```

To view the various UI's

- Mesos : http://192.168.33.10:5050
- Marathon : http://192.168.33.10:8080
- Chronos : http://192.168.33.10:4400

Notes:

- The ansible scripts set things up for docker both on the OS (by running docker)
and in mesos (configuring the containerizer), but there is still a docker repository missing, so we pull images onto the nodes as we set them up.
- There is no networking abstraction setup, so container ports must be explicitly
managed.
- Chronos could run within the Marathon framework, it just needs to be deployed that way via an API call. I need to look for a Ansible play book that can do this.

Todo:

- The ansible script is not idempotent, so it cannot be rerun. There are quite a
few todo's in the playbook.
-
