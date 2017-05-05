
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

	
