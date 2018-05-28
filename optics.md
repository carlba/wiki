# Hadoop

We use cloudera which is a packaged distrubution of hadoop. It was the first company that did a packaged disturubtion.

# Apache Hive

A relationshippy interface to hadoop.

# The client


jLogger accepts databases from clients on port 8080 and stores them into /usr/local/smithmicro/data 

/usr/local/smithmicro/data shared data folder for logger and agent



archive - procecssed and converted to AVRO
processed - proccessed into AVRO

optics agent
configuration: /usr/local/smithmicro/opticsagent

schema: /usr/local/smithmicro/opticsagent

 
HDFS /user/hadoop/analytics


cronjob hadoop user
hive-kicker.sh Restart optics agent if it suspended.

healthCheck.sh monitor status of cluster



smb://smsi-pgh-023.smsi.com/ISOs/RHEL/5.x


## Rhel 5.8


Ask about data set

Andy stites - QA Lead


https://bitbucket.smithmicro.net/projects/ANASP/repos/customer_deliverables/browse/Comcast%201.2%20Prod/scripts/System_Tools


https://bitbucket.smithmicro.net/projects/ANASP/repos/analytics/browse/analytics_library/scripts/export_report.py


(Issue with python dateutil)[https://projects.smithmicro.net/browse/ANASP-1801]


## Vagrant

vagrant-rhel-5.8-minimal

REMOVE PORT FORWARDING

Added /sbin to bashrc for shutdown command to work

## RHEL 5.8

Memory for VM: minimum 4 16 prefered 


* Download the installer
smb://smsi-pgh-023/Analytics/_Repos/Redhat/analytics-redhat5.8-archives.tar.gz

* Download the repo
smb://smsi-pgh-023/Analytics/_Repos/Redhat/analytics-redhat5.8-archives.tar.gz 

cd ~/analytics_package/system_config/puppet/scripts



jps -ml ps for java

7966 org.apache.hadoop.mapred.JobTracker
9164 sun.tools.jps.Jps -ml
7513 org.apache.hadoop.hdfs.server.namenode.SecondaryNameNode
8212 org.apache.hadoop.mapred.TaskTracker
7734 org.apache.hadoop.hdfs.server.datanode.DataNode
5774 org.apache.hadoop.hdfs.server.namenode.NameNode
8489 org.apache.hadoop.util.RunJar /usr/lib/hive/lib/hive-service-0.7.1-cdh3u3.jar org.apache.hadoop.hive.service.HiveServer


drwxr-xr-x   4 root root  4096 May  8 13:40 hadoop-default is the default haddop dir

drwxr-xr-x 3 root   root   4096 May  8 13:40 dfs
drwxr-xr-x 7 mapred hadoop 4096 May  8 13:44 mapred

turn of iptables and selinux

Install python dateuitl https://projects.smithmicro.net/browse/ANASP-1627
rpm -i python26-dateutil-1.4.1-6.rhel5.noarch.rpm

jlogger preferences

The following settings will be applied to: 'jlogger' installations on localhost.localdomain.
Cluster/Customer Name? [analytics]:
Logger installation location? [/usr/local/smithmicro]:
Logger events location? [/usr/local/smithmicro/data]:
Logger 'POST' Port Number? [8080]:
Logger 'Admin' Port Number? [9080]:
Logger Tomcat OPTS? [-Xms1024m -Xmx2048m]: -Xms256m -Xmx512m


## Test to send event

1. Goto the tail of events
http://10.101.66.107:9080/admin/events tail events

2. Send event

```bash
curl -v "http://10.101.66.107:8080/events" -d "v=v1.0.0.0&g=aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee&t=80f07b369a682aa32c5ed428b227b2503ffc5b08a822823e00959b9b3c1ea2310e1c42acfc6e9019856764de854fd4b7ab602d0d8582f699" -d 'data=[ 1, "2010-04-16 16:29:26", "DEV-SAMPLE", "1.2.3.4", "111-222-333-444-555", "FavoriteFood", { "Drink": "Tobasco", "Spicy": true } ]'  
```

3. Tail the logfile of jlogger to observce the events come on
    
    ``` bash
    tail -f /usr/local/smithmicro/data/events.log
    ```


Make sure the authuires keys have correct permissions

# Install optics agent

The following settings will be applied to: 'opticsagent' installations on carl-optics.smithmicro.net.
Cluster/Customer Name? [analytics]:
OpticsAgent installation location? [/usr/local/smithmicro]:
OpticsAgent events location? [/usr/local/smithmicro/data]:
### Initiating Puppet: analytics_bundle::production::opticsagent - Version::1.2.0.126


Add hadoop user to visudo

jlooger rotates data every hour

optics agent only looks for events.log.*

tail -f /usr/local/smithmicro/opticsAgent/logs/opticsAgent.log

# Monitor hadoop progress

http://10.101.66.107:50030/jobtracker.jsp See mapreduce jobs Most important one
http://10.101.66.107:50070/dfshealth.jsp
http://10.101.66.107:50070/dfsnodelist.jsp?whatNodes=LIVE
http://10.101.66.107:50030/machines.jsp?type=active
http://10.101.66.107:50090/status.jsp 


sudo vi /etc/hadoop/conf/hadoop-env.sh
export HADOOP_HEAPSIZE=1024

sudo vi /etc/hadoop/conf/mapred-site.xml

<!-- See: https://issues.apache.org/jira/browse/MAPREDUCE-478 -->
<property>
  <name>mapred.reduce.child.java.opts</name>
  <value>-Xmx512M</value>
</property>


sudo service hadoop-0.20-tasktracker restart
sudo service hadoop-0.20-namenode restart


## 

## Hive log file

/var/log/hive/hive-thrift.log
/tmp/hadoop/hive.log
md
