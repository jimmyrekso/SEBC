*List /etc/yum.repos.d
	[jimmyrekso123@mycloudera1 yum.repos.d]# ls
	CentOS-Base.repo       CentOS-Media.repo      epel.repo
	CentOS-CR.repo         CentOS-Sources.repo    epel-testing.repo
	CentOS-Debuginfo.repo  CentOS-Vault.repo      google-cloud.repo
	CentOS-fasttrack.repo  cloudera-manager.repo
	[jimmyrekso123@mycloudera1 yum.repos.d]# sudo yum install cloudera-manager-daemons cloudera-manager-server
	Loaded plugins: fastestmirror
	cloudera-manager                                         |  951 B     00:00
	Loading mirror speeds from cached hostfile
	* base: mirror.chpc.utah.edu
	* epel: mirror.hmc.edu
	* extras: mirror.tocici.com
	* updates: mirror.scalabledns.com
	Resolving Dependencies
	--> Running transaction check
	---> Package cloudera-manager-daemons.x86_64 0:5.11.0-1.cm5110.p0.101.el7 will be installed
	---> Package cloudera-manager-server.x86_64 0:5.11.0-1.cm5110.p0.101.el7 will be installed
	--> Finished Dependency Resolution
	
	Dependencies Resolved
	
	================================================================================
	Package               Arch   Version                    Repository        Size
	================================================================================
	Installing:
	cloudera-manager-daemons
						x86_64 5.11.0-1.cm5110.p0.101.el7 cloudera-manager 610 M
	cloudera-manager-server
						x86_64 5.11.0-1.cm5110.p0.101.el7 cloudera-manager 8.5 k
	
	Transaction Summary
	================================================================================
	Install  2 Packages
	
	Total download size: 610 M
	Installed size: 785 M
	Is this ok [y/d/N]: y
	Downloading packages:
	(1/2): cloudera-manager-server-5.11.0-1.cm5110.p0.101.el7. | 8.5 kB   00:00
	(2/2): cloudera-manager-daemons-5.11.0-1.cm5110.p0.101.el7 | 610 MB   00:10
	--------------------------------------------------------------------------------
	Total                                               60 MB/s | 610 MB  00:10
	Running transaction check
	Running transaction test
	Transaction test succeeded
	Running transaction
	Installing : cloudera-manager-daemons-5.11.0-1.cm5110.p0.101.el7.x86_64   1/2
	Installing : cloudera-manager-server-5.11.0-1.cm5110.p0.101.el7.x86_64    2/2
	Verifying  : cloudera-manager-server-5.11.0-1.cm5110.p0.101.el7.x86_64    1/2
	Verifying  : cloudera-manager-daemons-5.11.0-1.cm5110.p0.101.el7.x86_64   2/2
	
	Installed:
	cloudera-manager-daemons.x86_64 0:5.11.0-1.cm5110.p0.101.el7
	cloudera-manager-server.x86_64 0:5.11.0-1.cm5110.p0.101.el7
	
	Complete!
	[jimmyrekso123@mycloudera1 yum.repos.d]#
	
	
	
	[jimmyrekso123@mycloudera1 mysql-connector-java-5.1.41]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql scm root jimmyrekso123
	JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
	Verifying that we can write to /etc/cloudera-scm-server
	Creating SCM configuration file in /etc/cloudera-scm-server
	Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
	[                          main] DbCommandExecutor              INFO  Successfully connected to database.
	All done, your SCM database is configured correctly!
	[jimmyrekso123@mycloudera1 mysql-connector-java-5.1.41]$



	
	