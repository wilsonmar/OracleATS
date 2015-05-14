## OATS 12.5.0.2 Installation


* <a href="#InstallSteps">Installation Steps</a>
* <a href="#EnvVars">Environment Variables created</a>
* <a href="#FoldersCreated"> Folders Created</a>
* <a href="#AppData"> Application Data</a>
* <a href="#WindowsStart">Windows Start menu</a>
* <a href="#ServicesInstalled">Services installed</a>
* <a href="#WindowsRegistry">Windows Registry</a>
* <a href="#Uninstall"> Uninstall Steps</a>

### <a name="InstallSteps">Installation Steps</a>

1. Uninstall the previous OATS.
2. Click to download file oats-win64-full-12.5.0.1.287.zip  (1,635,871 KB). This took over an hour over my 3MB/sec line. 
3. Expand zip file. Folders:

	* bin - binary Windows .bat batch and Linux .sh shell scripts
  	* docs - documents (pdf and web HTML files) in english and japanese.
	* inventory
	* jre - java runtime environment
	* lib - 
	* oxe
	* oui
	* stage
	* wls - weblogic server

4. Click on the **setup.bat** file to invoke the installer.
5. In Windows Explorer, right-click on **setup.bat** to Run as Administrator.
6. Click Install.
7. Confirm default folder **C:\OracleATS**. 
8. Errors 
9. Right-click on the folder. It's 1.77 GB.

### <a name="EnvVars">Environment Variables Created</a>

	* DB_HOST
	* DB_HOSTNAME
	* DB_PASS
	* DB_PORT
	* DB_URL
	* DB_USER

* $HELPER_SERVICE = 7979
* $MW_HOME = C:\OracleATS\wls
* $OATS_AGENT_PASS
* $OATS_HOME = C:\OracleATS
* $Path = C:\OracleATS\oxe\app\oracle\product\10.2.0\server\bin;....
* $WL_HOME = C:\OracleATS\wls\wlserver
* $WLS_PASS
* $PATH  added?

(Acronymn WL = WebLogic and WLS = WebLogic Server, the middleware product Oracle got when it acquired BEA).

### <a name="FoldersCreated"> OracleATS Folders Created</a>

What's in each folder:

* agent
* agentmaster
* bin - binary Windows .bat batch and Linux .sh shell scripts
* config - 
* data -
* DataCollector -
* docs - documents (pdf and web HTML files) in english and japanese.
* FormsFT
* helperService
* jdk (java development kit)
* lib - 
* logs
* oats
* OFT (where OpenScripts go)
* openScript
* oxe - Oracle XE database
* tmp
* uninstall/jre
* wls - weblogic server


### <a name="AppData"> Application Data</a>
Within folder C:\OracleATS\oxe\oradata\XE
* CONTROL.DBF
* SYSAUX.DBF
* SYSTEM.DBF
* TEMP.DBF
* UNDO.DBF
* USERS.DBF

## <a name="WindowsStart">Windows Start menu</a>
1. Click Start orb
2. Click All Programs
3. Under Oracle Application Testing Suite:

* Administrator - Shortcut To http://localhost:8088/admin (does not support IE 11)
* OpenScript - C:\OracleATS\openScript\OpenScript.exe -configuration openscript_configuration -vm C:\OracleATS\openScript\jre\bin\javaw.exe -vmargs -Xmx512m -XX:MaxPermSize=256m
* Oracle Load Testing - Shortcut To http://localhost:8088/olt/
* Oracle Test Manager - Shortcut To http://localhost:8088/otm/
* Release Notes - C:\OracleATS\docs\en\readme.htm
* Uninstall OATS - C:\OracleATS\uninstall\bin\uninstall.bat
* Documentation (dated July, 2014)
	* ATS Installation Guide - C:\OracleATS\docs\en\OATSInstallationGuide.pdf
	* Getting Started Guide - C:\OracleATS\docs\en\OATSGettingStartedGuide.pdf
	* Load Testing ServerStats Guide - C:\OracleATS\docs\en\OLTLoadTestingServerStatsGuide.pdf
	* Load Testing User's Guide - C:\OracleATS\docs\en\OLTLoadTestingUsersGuide.pdf
	* OpenScript Programmer's Reference - C:\OracleATS\docs\en\OpenScriptProgammersReference.pdf
	* OpenScript User's Guide - C:\OracleATS\docs\en\OpenScriptUsersGuide.pdf
	* Test Manager User's Guide - C:\OracleATS\docs\en\OTMTestManagerUsersGuide.pdf
* Samples
	* Start MedRec creates a window to http://localhost:7011/medrec/
	* Stop MedRec stops the Windows service.
* Tools
	* About OATS - C:\OracleATS\docs\en\about_oats.htm
	* Create Support Package - C:\OracleATS\bin\oats_support.bat
	* Oracle Application Testing Database Configuration - C:\OracleATS\bin\DbConfig.bat
	* Oracle Load Testing Agent Authorization Manager - C:\OracleATS\jdk\jre\bin\javaw.exe -jar C:\OracleATS\agentmanager\AMAuthManager.jar
	* Restart Oracle Application Testing - target C:\OracleATS\bin\restartSvc.bat "Oracle ATS Server"
	* Stop Oracle Application Testing - target C:\OracleATS\bin\stopSvc.bat "Oracle ATS Server"


### <a name="ServicesInstalled"> Services Installed</a>
Listed alphabetically, as shown in the Windows Services dialog:

* **Oracle ATS Agent** - Launch requested load agents and monitor process health.
	Started automatically from
	C:\OracleATS\agentmanager\bin\AgentManagerService.exe -s C:\OracleATS\agentmanager\bin\\AgentManagerService.conf
	
* **Oracle ATS Helper** - Query helpers launched by OpenScript/JavaAgent and reuse them.
	Started automatically from 
	C:\OracleATS\helperService\bin\wrapper.exe -s C:\OracleATS\helperService\conf\wrapper.conf
	
* **Oracle ATS Server** at C:\ORACLE~1\wls\wlserver\server\bin\beasvc.exe

* **OracleServiceXE** -
	Auto started at c:\oracleats\oxe\app\oracle\product\10.2.0\server\bin\ORACLE.EXE XE

* **OracleJobSchedulerXE** - Disabled at c:\oracleats\oxe\app\oracle\product\10.2.0\server\Bin\extjob.exe XE

* **OracleXEClrAgent** - Manually started from C:\OracleATS\oxe\app\oracle\product\10.2.0\server\bin\OraClrAgnt.exe agent_sid=CLRExtProc max_dispatchers=2 tcp_dispatchers=0 max_task_threads=6 max_sessions=25

* **OracleXETNSListener** - 
	Started automatically at C:\OracleATS\oxe\app\oracle\product\10.2.0\server\BIN\tnslsnr.exe


### <a name="WindowsRegistry">Windows Registry</a>

* **HKEY_LOCAL_MACHINE/SOFTWARE/Oracle**. 

* Within **HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/services/**
  
	* OracleATSAgent, 
	* OracleATSHelper, 
	* OracleATSServer, 
	* OracleJobSchedulerXE, 
	* OracleMTSRecoveryService, 
	* OracleServiceXE, 
	* OracleXEClrAgent, 
	* OracleXENSListener


### <a name="Uninstall"> Uninstall Steps</a>

There is no uninstaller. Lame, I know. 
But it's more "manly" to uninstall manually. ;)

QUESTION:
In http://www.oracle.com/technetwork/database/10204-winx64-vista-win2k8-082253.html
there is a mention of using some **Oracle Universal Installer (OUI)**
to uninstall all Oracle components. But I can't find it
http://www.oracle.com/technetwork/database/database-technologies/express-edition/overview/index.html

#### Stop services running:
1. Press the Windows Start key or click the Windows Start orb.
2. Type **Services** and press Enter for the Component Services dialog.
3. Click on **Services(Local)** for the list of services.
3. Click on one of the services under the Name column heading and press O.
4. Right-click on each Oracle service and select Stop.
5. Click the red X at the upper-right corner of the window to dismiss the window.

After removing Windows Registry entries for Oracle, services installed no longer appears.

#### Remove Oracle Windows Registry Entries:
1. Open a Run window as Administrator.
2. Invoke **regedit.exe** 
3. Right-click 
4. Click to navigate to each <a href="#WindowsRegistry">Oracle Window Registry</a>,
	except "Oracle VM Virtualbox" which is unrelated to OATS.
5. select Delete
6. Repeat until all gone.
7. Reboot machine.

8. Delete the "C:\OracleATS" directory, or whatever directory is your ORACLE_BASE.
9. Delete the "C:\Program Files\Oracle" directory.
10. Empty the contents of your "c:\temp" directory.
11. Empty Recycle Bin.
