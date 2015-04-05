OATS (Oracle Application Testing Suite)
enables functional and performance testing of Oracle applications.

* auto-gen TOC:
{:toc}

Its marketing home page is at
http://www.oracle.com/technetwork/oem/app-test/etest-101273.html

## <a id="Installers"></a> Installers by Version

Versions are aligned with Oracle apps:

[12.5.0.1.0](#OATS12.5) (current) http://www.oracle.com/technetwork/oem/downloads/index-084446.html

12.4.0.2.0 http://www.oracle.com/technetwork/oem/downloads/apptesting-downloads-1983826.html

12.3.0.1.0 http://www.oracle.com/technetwork/oem/downloads/app-testing-download-2199741.html

The installer generates a password for a specific user during installation.

Trial allows up to 20 vusers to be run.

## <a id="History"></a> History

OATS began as commercial product e-Test from Empirix, which Oracle acquired March, 2008. See
http://www.oracle.com/us/corporate/Acquisitions/empirix/index.html
http://www.oracle.com/us/corporate/press/015619_EN

## <a id="Distinctions"></a> Distinctions

Unlike offerings from HP, SOASTA, etc. that can test a wide variety of systems,
OATS is focused on Oracle apps only and uses only Oracle technologies:

	* Oracle XE (eXpress Edition) Database version 11g Release 2 http://www.oracle.com/technetwork/database/database-technologies/express-edition/overview/index.html
	* Standard WebLogic Server version 10.3.5.0 (with JRocketJDK), not 1035_generic.jar.

Oracle has created **Accelerators** for Oracle Packaged Applications:

	* eBS/FORMS (Oracle e-Business Suite)
	* Siebel
	* JDEEOne
	* Hyperion
	* [Fusion/ADF](http://www.oracle.com/technetwork/developer-tools/adf/overview/index.html)
	* Peoplesoft
	* AdobeFlex

The experienced labor pool is likely to be smaller and thus more expensive
than with HP or other tools.

The download
http://www.oracle.com/technetwork/oem/downloads/index-084446.html
is **for Windows and Linux only**.

	* **Oracle OpenScript for Windows** is also called 
		**Oracle Functional Testing** scripts written in Java using Eclipse IDE.
	* **Oracle Test Manager (OTM)** organizes and manages the testing process.
	* **Oracle Load Testing (OLT)** also includes server side monitoring and reporting
	* **Load Testing Agent** installs also on 32 & 64 bit Windows 2008 R2 and Oracle Enterprise Linux 5 (not Windows 8).

There are several videos in the Oracle Learning Library YouTube channel
by Yukata Takatsu, ATS Group Product Manager (from Japan)
https://www.linkedin.com/pub/yutaka-takatsu/14/564/335

	* [Oracle Application Testing Suite 12c: OpenScript Functional Testing Overview Aug. 26, 2012](https://www.youtube.com/watch?v=2cDsBd8Kkbo)

	* [Introduction to Oracle Application Testing Suite 12.x Mar 2, 2013](https://www.youtube.com/watch?v=1GcEDCB4yno)

	* [Oracle Application Testing Suite 12c: Oracle Load Testing Overview](https://www.youtube.com/watch?v=uZ6w8O9O5Uc)

	* [Oracle Application Testing Suite 12c: Test Manager Overview Aug. 31, 2012](https://www.youtube.com/watch?v=ZKjcLYOMCkk) by Karilyn Kao, Sr. Product Manager

	* Troubleshooting your Load Testing Script Oct. 30, 2012](https://www.youtube.com/watch?v=s-Ylw9PdNXU)

	* [Oracle Application Testing Suite 12: Oracle Flow Builder Demo: Create a End to End Test Flow (OEM) Mar. 26, 2014](https://www.youtube.com/watch?v=Cx1oVvIBPBU)
	
	* Technical White Paper: 25 Tips for Creating Effective Load Test Scripts using Oracle Load Testing for E-Business Suite and Fusion Applications: http://www.oracle.com/technetwork/oem/app-quality-mgmt/wp-25tips-oltscripts-2287467.pdf


Videos from Chad Thompson http://chadthompson.me at Zirous Inc.

	* [First Steps: OATS and Oracle OpenScript Sep 24/25, 2012](https://www.youtube.com/watch?v=6Wnmh1HHY4Y)

Promo videos for Karthik's elearn paid seminars at http://www.itelearn.com/live-training/ :

	* [Oracle Application Testing Suit Day 01 Demo.wmv May 16, 2014](https://www.youtube.com/watch?v=fMIyCv7oK3Q)

	* [Oracle Application Testing Suite. What is OATS and Oracle Testing Training Tutorials overview May 7, 2014](https://www.youtube.com/watch?v=mom1ssaoU-c)

From Acolate Consulting (in Australia):

	* https://www.youtube.com/watch?v=srB2icE6Xf8

From Mayur Palta (Oracle Technical Consultant):

	* Application Performance Classroom http://www.slideshare.net/oracleonthebrain/application-testing-suite-3411757
		provides an introduction to What is testing, Business Impact of Application Quality,  



## <a id="OpenScripting"></a> Recording and Script Generation within internet browsers

CAUTION: OATS is usually behind in support of browser levels.
This means that specific older versions of browsers need to be installed,
with automatic updates turned OFF.

Support by OATS 12.1 for Firefox 6 with:

	* OpenScript WebDOM Extension

Support by OATS 12.1 for Internet Explorer 9 with add-on:

	* OpenScript Tool Bar (under IE Alt+View menu Toolbars)
	* OpenScript BHO
 
XPath is used by scripts to identify UI elements.

For maintainability, code from Master scripts are separated into Child script assets called by the master.

## <a id="ScriptCorrelation"></a> Script Correlation

## <a id="ScriptParam"></a> Script Parametization to Vary Data Values

## <a id="ChangeMgmt"></a> Change / Patch Management
QUESTION: When the system changes, all scripts need to be re-recorded?

QUESTION: Oracle Application Change Management Pack v3 - how does that integrate with

