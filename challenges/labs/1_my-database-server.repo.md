Create the Issue Install MySQL for RHEL/Centos 6.x or Install MariaDB for 7.x
Assign the Issue to yourself and label it started
Install a MySQL 5.6 or MariaDB 5.5 server, as appropriate, on the first node listed in 0_setup.md

    Use the appropriate YUM repository to install the package.
    Copy the repo you're using to challenges/labs/1_my-database-server.repo.md

On all cluster nodes

    Install the appropriate DB client package and JDBC connector jar

Start the database service
Create the following databases

    scm
    rman
    hive
    oozie
    hue
    sentry

Record the following in challenges/labs/1_db-server.md

    The hostname of your db server node
    The command and output for display your database server's version
    The command and output for listing your created databases


	
	
		[root@mycloudera1 ~]# yum install mariadb
		Loaded plugins: fastestmirror
		Loading mirror speeds from cached hostfile
		* base: mirror.chpc.utah.edu
		* epel: mirrors.syringanetworks.net
		* extras: mirror.tocici.com
		* updates: mirror.scalabledns.com
		Resolving Dependencies
		--> Running transaction check
		---> Package mariadb.x86_64 1:5.5.52-1.el7 will be installed
		--> Finished Dependency Resolution
		
		Dependencies Resolved
		
		================================================================================
		Package          Arch            Version                   Repository     Size
		================================================================================
		Installing:
		mariadb          x86_64          1:5.5.52-1.el7            base          8.7 M
		
		Transaction Summary
		================================================================================
		Install  1 Package
		
		Total download size: 8.7 M
		Installed size: 48 M

<center> <img src="https://github.com/jimmyrekso/SEBC/blob/master/challenges/labs/images/show_db.png"/> </center>


		[root@mycloudera2 jimmyrekso123]# cd  /usr/share/java/
		[root@mycloudera2 java]# ls
		mysql-connector-java-5.1.41.tar.gz  mysql-connector-java.jar
		[root@mycloudera2 java]#



		
		
*Log Start Cloudera Manager
	2017-05-05 03:39:20,979 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.11.0 (#101 built by jenkins on 20170412-1255 git: 70cb1442626406432a6e7af5bdf206a384ca3f98)
	2017-05-05 03:39:21,088 INFO main:org.mortbay.log: Logging to org.slf4j.impl.Log4jLoggerAdapter(org.mortbay.log) via org.mortbay.log.Slf4jLog
	2017-05-05 03:39:21,229 INFO main:org.springframework.context.support.ClassPathXmlApplicationContext: Refreshing org.springframework.context.support.ClassPathXmlApplicationContext@682d490b: startup date [Fri May 05 03:39:21 UTC 2017]; root of context hierarchy
	2017-05-05 03:39:21,315 INFO main:org.springframework.beans.factory.xml.XmlBeanDefinitionReader: Loading XML bean definitions from class path resource [webapp/WEB-INF/spring/beanRefFactory.xml]
	2017-05-05 03:39:21,768 INFO main:org.springframework.beans.factory.support.DefaultListableBeanFactory: Pre-instantiating singletons in org.springframework.beans.factory.support.DefaultListableBeanFactory@77d2ce1e: defining beans [bootstrapContext,rootContext]; root of factory hierarchy
	.
	.
	.
	.
	.
	mf.search.components.SearchRepositoryManager: Num docs:207
	2017-05-05 03:41:06,808 INFO SearchRepositoryManager-0:com.cloudera.server.web.c                                                                                        mf.search.components.SearchRepositoryManager: Constructing repo:2017-05-05T03:41                                                                                        :06.808Z
	2017-05-05 03:41:09,101 INFO SearchRepositoryManager-0:com.cloudera.server.web.c                                                                                        mf.search.components.SearchRepositoryManager: Finished constructing repo:2017-05                                                                                        -05T03:41:09.101Z
	2017-05-05 03:41:09,598 INFO WebServerImpl:org.mortbay.log: jetty-6.1.26.clouder                                                                                        a.4
	2017-05-05 03:41:09,599 INFO WebServerImpl:org.mortbay.log: Started SelectChanne                                                                                        lConnector@0.0.0.0:7180
	2017-05-05 03:41:09,599 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl                                                                                        : Started Jetty server.
	
	
*DB Properties
	[root@mycloudera1 ~]# cat /etc/cloudera-scm-server/db.properties
	# Auto-generated by scm_prepare_database.sh on Fri May  5 03:37:35 UTC 2017
	#
	# For information describing how to configure the Cloudera Manager Server
	# to connect to databases, see the "Cloudera Manager Installation Guide."
	#
	com.cloudera.cmf.db.type=mysql
	com.cloudera.cmf.db.host=localhost
	com.cloudera.cmf.db.name=scm
	com.cloudera.cmf.db.user=root
	com.cloudera.cmf.db.setupType=EXTERNAL
	com.cloudera.cmf.db.password=jimmyrekso123
