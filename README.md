# MySQL-5.7-Offline-Installation
MySQL 5.7 Offline Installation

Prerequisite :

1. Loacl repo of the centos or redhat 7 for the installtion of the createrepo

2. mysql-5.7.31-1.el7.x86_64.rpm-bundle.tar bundle

Installtion Steps :

Step 1 : Wget https://cdn.mysql.com//Downloads/MySQL-5.7/mysql-5.7.31-1.el7.x86_64.rpm-bundle.tar

step 2 : tar -xvf mysql-5.7.31-1.el7.x86_64.rpm-bundle.tar

step 3 : cd mysql-5.7.31-1.el7.x86_64.rpm-bundle

step 4 : yum install createrepo

step 5 : createrepo ./

step 6 : vim /etc/yum.repos.d/mysqllocal.repo

Copy  and past below line and save file

[Mysqllocalrepo]
name=mysql 5.7.31 local repo
baseurl=file:///path of the mysql-5.7.31-1.el7.x86_64.rpm-bundle
enabled=1
gpgcheck=0

step 7 : yum --enablerepo=Mysqllocalrepo install mysql-community-server
