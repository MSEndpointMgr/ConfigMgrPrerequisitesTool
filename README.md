# ConfigMgr Prerequisites Tool
ConfigMgr Prerequisites Tool is design to help administrators prepare their infrastructure and systems when about to install Configuration Manager.

Preparing your environment for a successful deployment of System Center Configuration Manager should not be an obstacle or time consuming. Many of the issues that might occur during the initial installation process can often be resolved by making sure that the correct prerequisites are in place.
The ConfigMgr Prerequisites Tool will help you to successfully prepare your environment allowing you to install the required software and Windows features.

### Prepare for an installation of the following Site types:

- Central Administration Site
- Primary Site
- Secondary Site

### And the following Site System roles:

- Management Point
- Distribution Point
- Software Update Point
- State Migration Point
- Application Catalog
- Enrollment Point
- Enrollment Proxy Point
- Certificate Registration Point

### In addition to what’s mentioned above, the tool will also allow you to:

- Configuration Manager configuration:
  - Download prerequisite files for Configuration Manager setup
  - Download and install Windows Assessment and Deployment Kit (ADK)
  - Create NO_SMS_ON_DRIVE.SMS files to prevent unwanted volumes to be used by Configuration Manager
- Active Directory configuration:
  - Extend Active Directory schema
  - Create System Management container in Active Directory
  - Configure permissions on System Management container
- SQL Server configuration:
  - Configure SQL Server memory usage settings
  - Validate SQL Server collation
  - Pre-create the Configuration Manager database
  - Configure SSRS database file size settings

# Documentation
Read the attached PDF file for more details about the ConfigMgr Prerequisites Tool and the functionality it has.

# Updates

## 2019-10-16
Version 3.0.5 includes a bug fix where the old method of using ping to determine internet connectivity has been replaced with WebClient instead to work in restricted network environments that don’t allow ping outbound. Also changed the lookup URL for connectivity to 'http://www.msftconnecttest.com/connecttest.txt' instead of 'developer.microsoft.com.
## 2019-01-04
Version 3.0.4 includes enhancements to work around the changes that came in Windows 10 ADK version 1809 (and assumingly onwards) where the tool has been updated to support both installation files to also download and install the WinPE add-on. Offline installation for Windows 10 ADK has also been updated with a new drop-down menu to specify the type of installer to ensure that the correct silent installation parameters are being used. 
## 2018-05-18
Version 3.0.3 released with a new method of detecting Windows ADK versions. From this version it now reads a XML feed hosted on www.msendpointmgr.com.
## 2018-02-19
Version 3.0.2 released including fixes again for loading Windows ADK versions from the newly moved web page.
## 2017-10-27
Version 3.0.1 released including fixes for loading Windows ADK versions from the new Windows Hardware Dev Center.
## 2017-08-09
Version 3.0.0 released ported from PowerShell to C# and with new functionality for remote actions, SQL Server and alternative credential or source locations. See the attached documentation in the download for more details.
## 2017-02-13
Version 2.0.1 released with fix for a bug that prevented the tool from launching when placed inside a folder structure containing spaces.
## 2016-09-13
Version 2.0.0 released.
## 2016-01-16
Version 1.4.2 with minor changes in the code has been released. No new features in this release.
## 2015-08-18
Version 1.4.1 has been released. Includes options to choose various version of Windows ADK to install.
## 2015-06-15
Version 1.4.0 has been released. The tool is now called ConfigMgr Prerequisites Tool.
## 2014-11-21
A bug in the code that checks if the tool has been launched elevated is now fixed. Instead of checking for 'Administrators' it's now checking for the well known SID of the local administrators group.
## 2014-10-07
Corrected a small bug where you were'nt able to select the Enrollment Proxy point.
## 2014-06-19
Fixed an issue when you choose to download the prerequisite files and selects a folder containing spaces in the name, the setupdl.exe parameters would throw an error.
## 2014-05-21
Fixed a bug where when you select SQL under Install WSUS, the textboxes would not be enabled.
## 2014-05-20
Fixed some small bugs when using Windows ADK in offline mode 
Corrected another bug when the System Management container was already created, it would not add the group