_________________________________________________________________________________
				
                                    README
_____________________________________________________________________________________________

 assignment2:
--> In this assignment2 the main purpose is to find the correlation between servers and network elements. The results are presented through a web dashboard.

--> This document also describes about the information of various files in this folder, modules/software needed and steps to run for this assignment2.

______________________________________________________________________________

--> This folder consists of 13 files in total:

 1)a.JPG.
 2)add_plot.php
 3)backend.sh
 4)backend_devices_osr.pl
 5)backend_servers_osr.pl
 6)bootstrap.min.css
 7)bootstrap-theme.min.css
 8)compare.php
 9)index.php
 10)plot.php
 11)readme.txt
 12)split.php
 13)RRD files folder

______________________________________________________________________________

--> Software Requirements:


1) Operating System: Ubuntu 14.04 LTS.

2) You need to install Apache server, MySQL and PHP.

3) Modules which are needed to be installed from CPAN are:
	
         Data::Dumper
	 DBI
         Cwd
         Net::SNMP
         RRD::simple
         LWP::Simple
 

______________________________________________________________________________
 
--> Steps to run this assignment:

1) Go to the terminal in move to the directory where this folder is present, say, /var/www/html/et2536-vibi15/assignment2/ 
   (It is assumed that the working directory configured in the apache server is /var/www/html/, change the path accordingly) 

2) Run the shell script "backend" in the terminal with the command "sh backend.sh".

3) Now, open a web browser and type the following URL: (It is assummed that the folder is in /var/www/html/.
	 http://localhost/et2536-vibi15/assignment2/index.php

4) Choose the desired options to view the server and device metrics.

_____________________________________________________________________________

--> NOTE:

1)It is advised to first add the device and server credentials through the front end.

2)This script by default probes the SNMP devices whose credentials are entered.

3)The user can delete these devices information through web GUI, and insert the devices he wishes to probe.

