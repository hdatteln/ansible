Role: spark
=========

Basic Apache Spark setup

Requirements
------------

Centos/Rhel OS

Role Variables
--------------

spark_release: Apache Spark version, default = "spark-2.2.0"  
spark.download_url: Apache Spark download url (precompiled)  
spark.install_dir: application insall root  
spark.user: Linux user for this application  
spark.group: Linux user group for this application 
spark.mode: master or slave
spark.master.host: host dns name or ip address for slave to connect
spark.master.port: port to use for connecting to master

spark_mode: can be used to override spark.mode from command line
master_host: can be used to override spark.master.host from command line
master_port: can be used to override spark.master.port from command line

Role Dependencies
------------------
- scala

Example Run Commands
---------------------

## Deploying a Slave:
`ansible-playbook install_spark.yml -i ../inventory/aws.txt -v --extra-vars "spark_mode=slave master_host=myhost.mydomain.com" --limit sparkslave limit sparkslave`
