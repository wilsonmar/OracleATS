The name of this repo (OracleATS) is taken from the default folder name where the product is installed.
The product is also referred to as **OATS** (Oracle Application Testing Suite).

* <a href="#Purpose"> Purpose</a>
* <a href="#History"> History</a>
* <a href="#SocialMedia"> Social Media</a>
* <a href="#Installers"> Installers by Version</a>
* <a href="#CertificationExams"> Certification Exams</a>
* <a href="#SkillsToLearn"> Skills To Learn</a>
* <a href="#OracleDocs"> Oracle's Documents</a>
* <a href="#Alternatives"> Alternatives to OATS</a>
* <a href="#Distinctions"> Distinctions</a>

## <a name="Purpose"> Purpose</a>

OATS enables functional and performance testing of Oracle applications.

* <a name="History"> History</a>

OATS began as commercial product e-Test from Empirix, which Oracle acquired March, 2008. See
http://www.oracle.com/us/corporate/Acquisitions/empirix/index.html
http://www.oracle.com/us/corporate/press/015619_EN

## <a name="SocialMedia"> Social Media</a>

Oracle's marketing home page is at
http://www.oracle.com/technetwork/oem/app-test/etest-101273.html

Mikael Fries (@MikaelFries in Munich, Germany) 
is Director Product Management at Oracle Responsible for Oracle's application testing products. 

* Product Twitter: #OracleATS
* Product Facebook?
* Product Wikipedia page?

LinkedIn groups:
* https://www.linkedin.com/groups/Oracle-Application-Testing-Suite-OATS-2008546
  was created by Infosys consultant Prasad Prabhakaran

* https://www.linkedin.com/grp/home?gid=6610481
  was created by Shrawan Shekar.

StackOverflow on OATS: http://stackoverflow.com/search?q=oats
	does not have much responses.

Oracle Forums on OATS content:
https://community.oracle.com/search.jspa?q=oats&place=%2Fplaces%2F1284&depth=ALL&customTheme=otn



## <a name="Installers"> Installers by Version</a>

Versions are aligned with Oracle apps:

[12.5.0.2.0](Install_12.5.2.md) (current) http://www.oracle.com/technetwork/oem/downloads/index-084446.html
out May 5, 2015.

[12.5.0.1.0](Install_12.5.1.md) http://www.oracle.com/technetwork/oem/downloads/index-084446.html

12.4.0.2.0 http://www.oracle.com/technetwork/oem/downloads/apptesting-downloads-1983826.html

12.3.0.1.0 http://www.oracle.com/technetwork/oem/downloads/app-testing-download-2199741.html

The installer generates a password for a specific user during installation.

Trial allows up to 20 vusers to be run.

### <a id="ChangeMgmt"> Change / Patch Management</a>
QUESTION: When the system changes, all scripts need to be re-recorded?

QUESTION: Oracle Application Change Management Pack v3 - how does that integrate with





## <a name="CertificationExams"> Certification Exams</a>

Oracle has a OATS certification Exam 1z0-529 
Oracle Enterprise Manager 11g Application Quality Management Essentials
http://education.oracle.com/pls/web_prod-plq-dad/db_pages.getpage?page_id=5001&get_params=p_exam_id:1Z0-529&p_org_id=&lang=

1. [Pay $245 for a voucher](http://education.oracle.com/pls/web_prod-plq-dad/db_pages.getpage?page_id=609&p_org_id=1001&lang=US&get_params=dc:D85847,p_preview:N)
2. Look for a test center near you at https://wsr.pearsonvue.com/testtaker/registration/SelectTestCenterProximity/ORACLE/489836
2. Schedule an exam time at http://pearsonvue.com/oracle/
3. Show up and answer 76% of 70 multiple choice questions correctly within 120 minutes.

### <a name="SkillsToLearn"> Skills To Learn</a>

Application Testing Suite (ATS)

*    Describe ATS use-cases
*    Implement and Configure ATS 
*    Configure, use and describe Oracle Load Testing 
*    Configure, use and describe Oracle Test Manager 
*    Configure and implement OpenScript 
*    Create, edit and use test scripts with OpenScript 
*    Describe OFT installation, licensing and component architecture 
*    Analyze platform requirements for OFT

Real Application Testing

*    Describe Real Application Testing (RAT) components 
*    Configure, use and describe SQL Performance Analyzer (SPA) 
*    Configure, use and describe Database Replay 

Data Masking

 *   Analyze scenarios for using Data Masking
 *   Implement Data Masking 
 *   Install and license Data Masking Pack 
 *   Describe the components and features of Data Masking


## <a name="OracleDocs"> Oracle's Documents</a>

The booklist for version 12.x are not online.
The latest I've found on internet is version 9.0 for Windows 32-bit (E15487-01, September 2009)
https://docs.oracle.com/cd/E25291_01/nav/portal_booklist.htm
and Oracle's Release Notes for OATS 9.20 (E17387-03, November 2010) is at
	https://docs.oracle.com/cd/E25294_01/doc.920/e17387/toc.htm#BEGIN

But documents are in the docs folder after folder OracleATS is installed
(listed in the order I recommend you read them):

* OATSReleaseNotes.pdf and readme.htm web page - Oracle Application Testing Suite Release Notes

* OATSInstallationGuide.pdf - Installation Guide

* OATSGettingStartedGuide.pdf and web page OATSInstallationGuide.htm

* OLTLoadTestingUsersGuide.pdf - Oracle Load Testing for Web Applications Load Testing User’s Guide

* OLTLoadTestingServerStatsGuide.pdf - ServerStats User Guid

* OpenScriptUsersGuide.pdf - Oracle Functional Testing for Web Applications Functional Testing User’s Guide

* OpenScriptProgammersReference.pdf - Oracle Functional Testing for Web Applications Application Programming Interface
Reference

* OTMTestManagerUsersGuide.pdf - Oracle Test Manager for Web Applications Test Manager User’s Guide

Where are these?
* Oracle Functional Testing for Web Applications Job Scheduler User’s Guide
* Oracle Functional Testing for Web Applications Navigation Editor User’s Guide
* Oracle Functional Testing for Web Applications Result Objects Reference



## <a name="Alternatives"> Alternatives to OATS</a>

Oracle also has PTF (Peopltools Testing Framework) for functional testing only
(no performance testing capability). 
It does not invoke URLs but internal objects.

The TurnKey Solutions PeopleSoft Accelerator
http://www.turnkeysolutions.com/PeopleSoft-accelerator.php
is based on cFactory™ which Business Process Testing (BPT) objects stored within HP ALM servers.

HP QTP/Unified Functional Testing

## <a name="Distinctions"> Distinctions</a>

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

