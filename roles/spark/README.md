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


Role Dependencies
------------------
- scala