#Secure Web Gateway (en) Secure Web Gateway Atom feed

Secure Web Gateway

Home
Get Started
Configuration
How To
Whats New
FAQs
View source
History

Log in

Setup Reporting Module

Contents

  * 1 Advantages of Reporting Module over the default Dashboard:
  * 2 Install Module
  * 3 Generate Reports
  * 4 View Reports

Advantages of Reporting Module over the default Dashboard:

  * Reduced Data Processing time
  * More detailed reports
  * Hour-wise reports
  * More filtering options
  * Deeper data analysis
  * An automated data mining engine
  * Exportable reports to PDF and Excel formats

Install Module

Navigate to src folder by running

cd /usr/local/src

Now download the tarball as

wget
http://downloads.safesquid.net/contrib/report/reporting_latest.tar.gz

Untar it by running the below command

tar -xvzf reporting_latest.tar.gz

Change directory to report

cd report

Now run the setup file

./setup.sh

Generate Reports

On successfull installtion, change directory to
/usr/local/safesquid/api

cd /usr/local/safesquid/api

Run the below command to generate reports for a particular day

./app_handler.py -d <date>

Eg: ./app_handler.py -d 20.05.2017

Run the below command to generate reports between a date range

./app_handler.py -s <start date> -e <end date>

Eg: ./app_handler.py -s 05.05.2017 -e 20.05.2017

Note: Date format should be in dd.mm.yyyy

Eg : 03.08.1990

View Reports

Open your favourite browser and set SafeSquid, for which you generated
the reports in step 2, as the proxy.

Now open the URL http://safesquid.cfg/report/index.html

Now, you are looking at today’s reports.

If reports for today were not generated in the step 2, the reports page
will be blank.

So use the date picker to view the reports that were generated in the
step 2.
Retrieved from
"https://docs.safesquid.com/index.php?title=Setup_Reporting_Module&oldi
d=2227"
Category:
  * How To

Tools
What links here
Related changes
Special pages
Printable version
Permanent link
Page information
This page was last edited on 25 July 2021, at 00:31.
This page has been accessed 1,106 times.
Privacy policy
About Secure Web Gateway
Disclaimers
Visible links:
https://docs.safesquid.com/opensearch_desc.php
https://docs.safesquid.com/index.php?title=Special:RecentChanges&feed=atom
https://docs.safesquid.com/wiki/Documentation
https://docs.safesquid.com/wiki/Documentation
https://docs.safesquid.com/wiki/Getting_Started
https://docs.safesquid.com/wiki/Configuration
https://docs.safesquid.com/wiki/How_To
https://docs.safesquid.com/wiki/Whats_New
https://docs.safesquid.com/wiki/FAQ
https://docs.safesquid.com/index.php?title=Setup_Reporting_Module&action=edit
https://docs.safesquid.com/index.php?title=Setup_Reporting_Module&action=history
https://docs.safesquid.com/index.php?title=Special:UserLogin&returnto=Setup+Reporting+Module
https://docs.safesquid.com/wiki/Setup_Reporting_Module#mw-navigation
https://docs.safesquid.com/wiki/Setup_Reporting_Module#p-search
https://docs.safesquid.com/wiki/Setup_Reporting_Module#Advantages_of_Reporting_Module_over_the_default_Dashboard:
https://docs.safesquid.com/wiki/Setup_Reporting_Module#Install_Module
https://docs.safesquid.com/wiki/Setup_Reporting_Module#Generate_Reports
https://docs.safesquid.com/wiki/Setup_Reporting_Module#View_Reports
http://downloads.safesquid.net/contrib/report/reporting_latest.tar.gz
http://safesquid.cfg/report/index.html
https://docs.safesquid.com/index.php?title=Setup_Reporting_Module&oldid=2227
https://docs.safesquid.com/wiki/Special:Categories
https://docs.safesquid.com/index.php?title=Category:How_To&action=edit&redlink=1
https://docs.safesquid.com/wiki/Setup_Reporting_Module
https://docs.safesquid.com/wiki/Special:WhatLinksHere/Setup_Reporting_Module
https://docs.safesquid.com/wiki/Special:RecentChangesLinked/Setup_Reporting_Module
https://docs.safesquid.com/wiki/Special:SpecialPages
javascript:print();
https://docs.safesquid.com/index.php?title=Setup_Reporting_Module&oldid=2227
https://docs.safesquid.com/index.php?title=Setup_Reporting_Module&action=info
https://docs.safesquid.com/wiki/SafeSquid_Docs:Privacy_policy
https://docs.safesquid.com/wiki/SafeSquid_Docs:About
https://docs.safesquid.com/wiki/SafeSquid_Docs:General_disclaimer

Hidden links:
https://docs.safesquid.com/wiki/Setup_Reporting_Module
https://docs.safesquid.com/wiki/Setup_Reporting_Module