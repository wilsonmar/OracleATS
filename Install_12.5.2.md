## OATS 12.5.0.2 Installation

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

### <a name="OATS_Uninstall"> Uninstall Oracle XE Database</a>

There is no uninstaller. Lame, I know. 
But it's more "manly" to uninstall manually.

http://www.oracle.com/technetwork/database/database-technologies/express-edition/overview/index.html

1. Uninstall all Oracle components using the Oracle Universal Installer (OUI)
	from http://www.oracle.com/technetwork/database/10204-winx64-vista-win2k8-082253.html
  I skip this.

2. Run a Command, regedit.exe and delete the HKEY_LOCAL_MACHINE/SOFTWARE/Oracle key. 
This contains registry entires for all Oracle products.

3. Delete any references to Oracle services left behind in the following part of the registry:
  HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/services/Ora*
  (OracleATSAgent, OracleATSHelper, OracleATSServer, OracleJobSchedulerXE, OracleMTSRecoveryService, 
  OracleServiceXE, OracleXEClrAgent, OracleXENSListener)

4. Reboot your machine.

5. Delete the "C:\OracleATS" directory, or whatever directory is your ORACLE_BASE.
6. Delete the "C:\Program Files\Oracle" directory.
7. Empty the contents of your "c:\temp" directory.
8. Empty Recycle Bin.

### <a name="ServicesInstalled"> Services installed</a>

* **Oralce ATS Agent** - Launch requested load agents and monitor process health.
	Started automatically from
	C:\OracleATS\agentmanager\bin\AgentManagerService.exe -s C:\OracleATS\agentmanager\bin\\AgentManagerService.conf
	
* **Oracle ATS Helper** - Query helpers launched by OpenScript/JavaAgent and reuse them.
	Started automatically from 
	C:\OracleATS\helperService\bin\wrapper.exe -s C:\OracleATS\helperService\conf\wrapper.conf
	
* **Oracle ATS Server** at C:\ORACLE~1\wls\wlserver\server\bin\beasvc.exe

