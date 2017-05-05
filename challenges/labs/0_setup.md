
List the cloud provider you are using (AWS, GCE, Azure, other)

        Using Google Compute
List the nodes you are using by IP address and name
<center> <img src="https://github.com/jimmyrekso/SEBC/blob/master/challenges/labs/images/ip_vm.png"/> </center>
List the Linux release you are using
    
    [root@mycloudera1 ~]# rpm --query centos-release
    centos-release-7-3.1611.el7.centos.x86_64
    [root@mycloudera1 ~]#
Demonstrate the disk capacity available on each node is >= 30 GB

    [root@mycloudera1 ~]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/sda1        30G  3.1G   27G  11% /
	devtmpfs        4.9G     0  4.9G   0% /dev
	tmpfs           4.9G     0  4.9G   0% /dev/shm
	tmpfs           4.9G  8.3M  4.9G   1% /run
	tmpfs           4.9G     0  4.9G   0% /sys/fs/cgroup
	tmpfs          1001M     0 1001M   0% /run/user/1000
	[root@mycloudera1 ~]#
List the command and output for yum repolist enabled
  
      [root@mycloudera1 
	[root@mycloudera1 ~]# yum repolist enabled
	Loaded plugins: fastestmirror
    Loading mirror speeds from cached hostfile
     * base: mirror.chpc.utah.edu
     * epel: mirror.hmc.edu
     * extras: mirror.tocici.com
     * updates: mirror.scalabledns.com
    repo id                 repo name                                         status
    base/7/x86_64           CentOS-7 - Base                                    9,363
    epel/x86_64             Extra Packages for Enterprise Linux 7 - x86_64    11,584
    extras/7/x86_64         CentOS-7 - Extras                                    337
    google-cloud-compute    Google Cloud Compute                                   4
    google-cloud-sdk        Google Cloud SDK                                       8
    updates/7/x86_64        CentOS-7 - Updates                                 1,577
    repolist: 22,873
    [root@mycloudera1 ~]#

	
Add the following Linux accounts to all nodes
User cate with a UID of 2300
User jemaine with a UID of 2900
Create the group kiwis and add jemaine to it
Create the group aussies and add cate to it



List the /etc/passwd entries for cate and jemaine

	cate:x:2300:1004::/home/cate:/bin/bash
	jemaine:x:2900:1005::/home/jemaine:/bin/bash
	[root@mycloudera1 ~]#
<center> <img src="https://github.com/jimmyrekso/SEBC/blob/master/challenges/labs/images/user.png"/> </center>
List the /etc/group entries for kiwis and aussies
	kiwis:x:1006:jemaine
	aussies:x:1007:cate
	[root@mycloudera3 ~]#
<center> <img src="https://github.com/jimmyrekso/SEBC/blob/master/challenges/labs/images/group.png"/> </center>




Create the Issue Install CM
Assign yourself to the Issue and label it started
Install Cloudera Manager on the first node listed in 0_setup.md
Configure the CM repo to install the latest release
    List the command and output for ls /etc/yum.repos.d in challenges/labs/2_cm.md
    Copy the cloudera-manager.repo file to challenges/labs/2_cloudera-manager.repo.md
Configure Cloudera Manager
    Use the scm_prepare_database.sh script to write your db.properties file
        List the full command line in 2_cm.md
Start the Cloudera Manager server. Then in challenges/labs/2_db.properties.md:
    Add the complete first line from your server log
    Add the complete line that contains the phrase "Started Jetty server"
    Add the full contents of your db.properties file
Push these changes to your GitHub repo and label the Issue 'review`
    Assign the issue to both instructors

*List /etc/yum.repos.d
	[root@mycloudera1 yum.repos.d]# ls
	CentOS-Base.repo       CentOS-Media.repo      epel.repo
	CentOS-CR.repo         CentOS-Sources.repo    epel-testing.repo
	CentOS-Debuginfo.repo  CentOS-Vault.repo      google-cloud.repo
	CentOS-fasttrack.repo  cloudera-manager.repo
	[root@mycloudera1 yum.repos.d]#
		


	
