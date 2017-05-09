______________________________________________________________________________

		                  README
______________________________________________________________________________

Assignment1:
--> In this assignment1 the main purpose is to configure MRTG.And simulataneously we develop a tool which works similar to MRTG,where the results are presented through a web dashboard.

--> This document describes the information about the various files in this folder, modules/software needed and steps to run this assignment.

________________________________________________________________________________

--> This folder consists of 14 files in total:

 1)a.jpg
 2)backend.pl
 3)backend.sh
 4)bootstrap.min.css
 5)bootstrap-theme.min.css
 6)device.php
 7)fpassthru_unlink.php
 8)home_table.php
 9)index.php
 10)mrtgconf.pl
 11)readme.txt
 12)split.php
 13)RRD files folder
 14)report.pdf

______________________________________________________________________________

--> Software Requirements:

1) Operating System: Ubuntu 14.04 LTS.

2) You need to install Apache web server, MySQL and PHP.

3) Modules which are needed to be installed from CPAN are:
	 
         Data::Dumper
	 DBI
         Cwd
         Net::SNMP
         RRD::simple
 
______________________________________________________________________________

--> Steps to run this assignment:

1) Go to the terminal and move to the directory where this folder is present, say, /var/www/html/et2536-vibi15/assignment1/ 
   (It is assumed that the working directory configured in the apache server is /var/www/html/, change the path accordingly) 

2) To configure MRTG, Run the perl script "mrtgconf.pl" in the terminal with the command "sudo perl mrtgconf.pl".

3) To view the MRTG statistics, use the URL:
   http://localhost/mrtg/

4) To run the developed tool, run the perl script "sh backend.sh" in the terminal with the command "sh backend.sh".

5) Now, open a web browser and type the following URL: (It is assummed that the folder is in /var/www/html/.
	 http://localhost/et2536-vibi15/assignment1/index.php

6) Choose the desired device to view the graphs and statistics.

______________________________________________________________________________

--> NOTE:

1) Make sure to create "DEVICES" table in the MySQL database prior for running the backend script in the terminal. 
	 It can be created by following the steps in the major readme.txt file, for all the 4 assignments.

2) Add the following lines to the file "apache2.conf" before configuring the MRTG.
   The path for file is "/etc/apache2/apache2.conf";

Alias /mrtg "/var/www/mrtg/"
 
<Directory "/var/www/mrtg/">
        Options None
        AllowOverride None
        Require all granted
</Directory>

ServerName localhost:80

3) Restart Apache after adding the above lines to apache2.conf
   sudo service apache2 restart

