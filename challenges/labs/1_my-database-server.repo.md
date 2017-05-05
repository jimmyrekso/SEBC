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



	
