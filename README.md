[![Build Status](https://travis-ci.org/traveloka/ansible-role-kafka.svg?branch=master)](https://travis-ci.org/traveloka/ansible-role-kafka)
# Ansible Role: Kafka

An Ansible role that installs Kafka on supported Ubuntu LTS releases.

## Requirements

No special pre-requisites.

Role Variables
--------------

    - name: kafka_prefix
      description: prefix to which kafka will be installed
      default: /opt

    - name: kafka_scala_ver
      description: Scala version used to build Kafka
      default: 2.10 (override to 2.11 if you want to use Kafka 0.9.x)
      
    - name: kafka_main_ver
      description: Kafka main version
      default: 0.8.2
      
    - name: kafka_patch_ver
      description: Kafka patch version
      default: 2
	  
    - name: kafka_port
      description: the port the Kafka socket server listens on
      default: 9092

Dependencies
------------

    - role: traveloka.zookeeper

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: traveloka.kafka
          kafka_main_ver: 0.8.2
          kafka_port: 9092

License
-------

Apache

Author Information
------------------

Author: Michel Alexandre Salim <michel@traveloka.com>
Copyright (C) Traveloka 2016
https://github.com/traveloka
