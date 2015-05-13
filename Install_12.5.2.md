## <a id="OATS12.5"></a> OATS 12.5 Installation

1. Website
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

### Services installed

Oralce ATS Agent - Launch requested load agents and monitor process health.
	Started automatically from
	C:\OracleATS\agentmanager\bin\AgentManagerService.exe -s C:\OracleATS\agentmanager\bin\\AgentManagerService.conf
	
Oracle ATS Helper - Query helpers launched by OpenScript/JavaAgent and reuse them.
	Started automatically from 
	C:\OracleATS\helperService\bin\wrapper.exe -s C:\OracleATS\helperService\conf\wrapper.conf
	
Oracle ATS Server at C:\ORACLE~1\wls\wlserver\server\bin\beasvc.exe

